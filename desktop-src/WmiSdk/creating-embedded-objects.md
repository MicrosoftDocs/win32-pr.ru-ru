---
description: При создании экземпляра с внедренными объектами выполните следующие задачи.
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Создание внедренных объектов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2e54e16005669ebd77b0bc08e5d3174f7aa5fadee2a47477920e91aaa2ae155b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464174"
---
# <a name="creating-embedded-objects"></a>Создание внедренных объектов

При создании экземпляра с внедренными объектами выполните следующие задачи.

-   Внедренный объект необходимо объявить строго типизированным или слабо типизированным.

    Строго типизированный объект указывает на объект определенного класса и использует имя класса. Слабо типизированный объект указывает на объект неопределенного класса и использует ключевое слово **Object** . Оба объекта сопоставляются с **\_ неизвестным типом VT** .

-   Значение **null** можно использовать для значений по умолчанию для внедренных объектов и путей в инициализации и объявлениях.
-   При внедрении пути к объекту не размещайте пробелы между элементами внедренного пути. Например, путь к объекту "Class1Index = 3;" не содержит пробелов между именем свойства "Class1index" и присваиваемым ему значением "3".

В следующем объявлении класса показано, как объявить строго типизированные и слабо типизированные внедренные объекты.

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

В следующих примерах описывается объявление внедренных объектов в объявлении класса.

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

В следующем примере описывается инициализация одного свойства, которое является строго типизированным объектом, и еще одно свойство, которое является массивом слабо типизированных объектов.

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



