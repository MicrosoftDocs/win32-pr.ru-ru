---
description: Массив — это индексированный список значений данных, имеющих один и тот же тип данных, на которые можно ссылаться. Помимо строковых и числовых массивов, MOF поддерживает массивы внедренных объектов и ссылок.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Массивы MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1231b89302e15d5a7467ab7ff99d23b200badd67e6c5c95054c90b84554548d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992804"
---
# <a name="mof-arrays"></a>Массивы MOF

Массив — это индексированный список значений данных, имеющих один и тот же тип данных, на которые можно ссылаться. Помимо строковых и числовых массивов, MOF поддерживает массивы внедренных объектов и ссылок.

В следующих правилах определяется MOF-массив:

-   Скобки, используемые после идентификатора свойства, задают массив в определении класса.

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   Все массивы должны быть одномерными.
-   Массивы могут быть неограниченными или иметь явный размер.

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    Инструментарий WMI реализует ограниченные и неограниченные массивы как структуры **SAFEARRAY** , что позволяет инструментарию WMI изменять измерения массива во время выполнения. При объявлении массива с явно заданным размером WMI сохраняет размер как квалификатор и обрабатывает его как рекомендуемый максимальный размер. Однако при необходимости Инструментарий WMI может расширить размер. Изменение явного размера не влияет на реальные данные.

-   Массивы инициализируются путем указания значений соответствующего типа в списке с разделителями-запятыми.

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   Массив ссылок объявляется как массив строк пути к объекту.

    При объявлении строки пути к объекту не размещайте пробелы между элементами пути к объекту. В следующем примере показано, как объявить ссылку на путь к объекту.

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   Массив можно использовать в качестве параметра для метода, но не в качестве возвращаемого значения входного или входного параметра.
-   Все элементы массива создаются как значения одного типа.

    Если элементы массива имеют тип **объекта** , можно поместить любой тип объекта в массив. С другой стороны, при объявлении определенного типа объекта WMI разрешает только объекты этого класса или подкласса в массиве. В следующих примерах показаны объявления массивов, включающие использование типа **объекта** .

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



