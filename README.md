# Mycalculator-
import streamlit as st

st.title("ماشین‌حساب ساده")

num1 = st.number_input("عدد اول")
num2 = st.number_input("عدد دوم")
operation = st.selectbox("عملیات", ["جمع", "تفریق", "ضرب", "تقسیم"])

if st.button("محاسبه"):
    if operation == "جمع":
        result = num1 + num2
    elif operation == "تفریق":
        result = num1 - num2
    elif operation == "ضرب":
        result = num1 * num2
    elif operation == "تقسیم":
        if num2 != 0:
            result = num1 / num2
        else:
            result = "خطا: تقسیم بر صفر"
    st.write(f"نتیجه: {result}")
    
