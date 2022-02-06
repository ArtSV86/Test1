## Отчёт о тестировании приложения "Bonus"

### Краткое описание


Проведен тест созданной формулы для расчета итогового бонуса клиентам (float totalBonus = cost * bonus), расчет производится от коэффициента (float bonus = 0.05F, где 0.05 = 1/20 (1 миля за каждые 20 рублей) и стоимости самого билета (float cost = 3000F, в данном случае 3000 рублей), воспроизведенной в java, где в качестве type=float:

```java
public class Main {
    public static void main(String[] args) {
        float bonus = 0.05F;
        float cost = 3000F;
        float totalBonus = cost * bonus;
        System.out.println(totalBonus);
    }
}
```

Результат обработки:
```
150.0
```


### Описание тестов

Проводилось  функциональное, санитарное тестирование.

### Результаты
Дефекты не выявлены.

   

### Общие рекомендации

Можно было сделать формулу через type=int: 
```java
public class Main {
    public static void main(String[] args) {
        int bonus = 0_05;
        int cost = 3000;
        int totalBonus = cost * bonus/100;
        System.out.println(totalBonus);
    }
}
```
Результат обработки:
```
150
```