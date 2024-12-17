# АНАЛИЗ ДАННЫХ В РАЗРАБОТКЕ ИГР  
## ЛАБОРАТОРНАЯ РАБОТА 4 [in GameDev]

**Отчет по лабораторной работе #4 выполнила:**  
Жолдубаева Жанара Мирланбековна  
РИ230911  



---


### **Данные о работе**  
Проект: лабораторная работа #4 "Перцептрон в Unity".  
Выполнила: Жолдубаева Жанара Мирланбековна, РИ230911.  

---

## **Цель работы:**  
Создать простой перцептрон в Unity и привязать его к игровому объекту с использованием скрипта на C#.  

---

## **Ход выполнения работы**  

### **Задание 1. Создание нового проекта Unity**  

1. Открыть **Unity Hub**.  
2. Создать **новый 3D проект**. Дать проекту имя (*PerceptronLab4*).  

![image](https://github.com/user-attachments/assets/1a54bf4c-2803-4078-84cf-85d5966b3240)
 

---

### **Задание 2. Создание пустого GameObject "Perceptron"**  

1. Открыть созданный проект.  
2. В сцене **Scene** выбрать **Create > Empty GameObject**.  
3. Переименовать GameObject в `Perceptron`.  

![image](https://github.com/user-attachments/assets/80b191a9-5cc0-43d0-b4d7-7676dd80caca)


---

### **Задание 3. Создание скрипта Perceptron.cs**  

1. В окне **Assets** правой кнопкой мыши выбрать **Create > C# Script**.  
2. Назвать файл `Perceptron.cs`.  
3. Привязать скрипт к объекту `Perceptron` через перетаскивание.  

![image](https://github.com/user-attachments/assets/baf08fd8-39f4-4bc7-8e37-1da5203f535e)

---

### **Задание 4. Добавление кода в Perceptron.cs**  


```csharp
using System.Collections;
using UnityEngine;

public class Perceptron : MonoBehaviour
{
    public float input1;
    public float input2;
    public float weight1 = 0.5f;
    public float weight2 = 0.5f;
    public float threshold = 1.0f;

    void Start()
    {
        float result = CalculateOutput(input1, input2);
        Debug.Log("Perceptron Output: " + result);
    }

    float CalculateOutput(float i1, float i2)
    {
        float sum = (i1 * weight1) + (i2 * weight2);
        return sum >= threshold ? 1 : 0;
    }
}
```

![image](https://github.com/user-attachments/assets/bdd99c06-b115-41df-86a8-c512d8211459)


---

## **Выводы**  
В ходе выполнения лабораторной работы был создан простой перцептрон и реализовано его подключение к игровому объекту в Unity.
