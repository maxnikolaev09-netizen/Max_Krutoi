## Задача 1
**Дано:** $\overline{(X > 2) \vee (X < 2)} \vee (X > 4)$, $X = 1$.
**Решение:**
- $X > 2 \Rightarrow 1 > 2 \Rightarrow \text{ложь}$;
- $X < 2 \Rightarrow 1 < 2 \Rightarrow \text{истина}$;
- $\text{ложь} \vee \text{истина} = \text{истина}$, с чертой сверху: $\overline{\text{истина}} = \text{ложь}$;
- $X > 4 \Rightarrow 1 > 4 \Rightarrow \text{ложь}$;
- $\text{ложь} \vee \text{ложь} = \text{ложь}$.
**Ответ:** $0$.

---

## Задача 2
**Дано:** «Если в треугольнике любая его медиана не является высотой и биссектрисой, то этот треугольник не равнобедренный и не равносторонний».
**Решение:**
- Обозначим: $A$ — «любая медиана не является высотой и биссектрисой», $B$ — «треугольник равнобедренный», $C$ — «треугольник равносторонний»;
- Формула: $A \rightarrow (\overline{B} \wedge \overline{C})$;
- В равнобедренном треугольнике медиана к основанию является высотой и биссектрисой, поэтому если такой медианы нет, треугольник не равнобедренный, а значит и не равносторонний;
- Следовательно, высказывание является истинным.
**Ответ:** $A \rightarrow (\overline{B} \wedge \overline{C})$, утверждение истинно.

---

## Задача 3
**Дано:** $(\overline{Y} \wedge (\overline{X} \wedge Z)) \rightarrow ((Z \wedge \overline{X}) \vee Y)$.
**Решение:**
- $A \rightarrow B = \overline{A} \vee B$;
- $\overline{\overline{Y} \wedge \overline{X} \wedge Z} \vee (Z \wedge \overline{X}) \vee Y = Y \vee X \vee \overline{Z} \vee (Z \wedge \overline{X}) \vee Y$;
- $\overline{Z} \vee (Z \wedge \overline{X}) = \overline{Z} \vee \overline{X}$;
- $Y \vee X \vee \overline{Z} \vee \overline{X} = Y \vee (X \vee \overline{X}) \vee \overline{Z} = Y \vee 1 \vee \overline{Z} = 1$.
**Ответ:** $1$ (тождественно истинно).

---

## Задача 4
**Дано:** $(B \vee \overline{A}) \wedge (\overline{B} \vee A) \wedge \overline{B}$.
**Решение:**
- Раскрываем: $(B \vee \overline{A}) \wedge \overline{B} = (B \wedge \overline{B}) \vee (\overline{A} \wedge \overline{B})$;
- $B \wedge \overline{B} = 0 \Rightarrow \overline{A} \wedge \overline{B}$;
- $(\overline{A} \wedge \overline{B}) \wedge (\overline{B} \vee A) = (\overline{A} \wedge \overline{B} \wedge \overline{B}) \vee (\overline{A} \wedge A \wedge \overline{B}) = \overline{A} \wedge \overline{B}$.
**Ответ:** $\overline{A} \wedge \overline{B}$.

---

# Задача 5: построение таблицы истинности

**Дано:** $((\overline{X} \wedge \overline{Y}) \vee (X \wedge \overline{X})) \vee \overline{(X \rightarrow Y)}$

| $X$ | $Y$ | $\overline{X}$ | $\overline{Y}$ | $\overline{X} \wedge \overline{Y}$ | $X \wedge \overline{X}$ | $X \rightarrow Y$ | $\overline{X \rightarrow Y}$ | Результат |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0 | 0 | 1 | 1 | 1 | 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 | 0 | 0 | 1 | 0 | 0 |
| 1 | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 | 1 | 0 | 0 |

**Упрощение:**
- $X \wedge \overline{X} = 0$;
- $\overline{X \rightarrow Y} = \overline{\overline{X} \vee Y} = X \wedge \overline{Y}$;
- $(\overline{X} \wedge \overline{Y}) \vee (X \wedge \overline{Y}) = \overline{Y} \wedge (\overline{X} \vee X) = \overline{Y}$.


**Финальный ответ:** выражение не является тождественно истинным (принимает значение 0 при $Y=1$), упрощённый вид: $\overline{Y}$.