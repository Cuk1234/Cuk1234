from sympy import symbols, Eq, solve

# визначаємо символи
m_Al, m_Cu = symbols('m_Al m_Cu')

# відомі значення
c_Al = 0.897  # J/g°C
c_Cu = 0.385  # J/g°C
c_w = 4.186  # J/g°C
c_c = 0.897  # J/g°C
m_w = 250  # г
m_c = 500  # г
t_1 = 19  # °C
t_2 = 127  # °C
t = 27  # °C

# рівняння
eq1 = Eq((m_Al*c_Al + m_Cu*c_Cu)*(t_2 - t), (m_w*c_w + m_c*c_c)*(t - t_1))
eq2 = Eq(m_Al + m_Cu, 180)

# розв'язуємо систему рівнянь
solution = solve((eq1, eq2), (m_Al, m_Cu))

print(f"m_Al = {solution[m_Al]} г")
print(f"m_Cu = {solution[m_Cu]} г")


<!---
Cuk1234/Cuk1234 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
