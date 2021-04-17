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
ms.openlocfilehash: a76a70fa0e01068622a4f4cdbbbfb6c992b67f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702837"
---
# <a name="creating-embedded-objects"></a><span data-ttu-id="58607-103">Создание внедренных объектов</span><span class="sxs-lookup"><span data-stu-id="58607-103">Creating Embedded Objects</span></span>

<span data-ttu-id="58607-104">При создании экземпляра с внедренными объектами выполните следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="58607-104">When creating an instance with embedded objects, perform the following tasks:</span></span>

-   <span data-ttu-id="58607-105">Внедренный объект необходимо объявить строго типизированным или слабо типизированным.</span><span class="sxs-lookup"><span data-stu-id="58607-105">You must declare an embedded object as strongly typed or weakly typed.</span></span>

    <span data-ttu-id="58607-106">Строго типизированный объект указывает на объект определенного класса и использует имя класса.</span><span class="sxs-lookup"><span data-stu-id="58607-106">A strongly typed object points to an object of a specific class and uses the class name.</span></span> <span data-ttu-id="58607-107">Слабо типизированный объект указывает на объект неопределенного класса и использует ключевое слово **Object** .</span><span class="sxs-lookup"><span data-stu-id="58607-107">A weakly typed object points to an object of an unspecified class and uses the **object** keyword.</span></span> <span data-ttu-id="58607-108">Оба объекта сопоставляются с **\_ неизвестным типом VT** .</span><span class="sxs-lookup"><span data-stu-id="58607-108">Both objects map to the **VT\_UNKNOWN** type.</span></span>

-   <span data-ttu-id="58607-109">Значение **null** можно использовать для значений по умолчанию для внедренных объектов и путей в инициализации и объявлениях.</span><span class="sxs-lookup"><span data-stu-id="58607-109">You can use **NULL** for the default value of embedded objects and paths in initializations and declarations.</span></span>
-   <span data-ttu-id="58607-110">При внедрении пути к объекту не размещайте пробелы между элементами внедренного пути.</span><span class="sxs-lookup"><span data-stu-id="58607-110">When embedding an object path, do not place white space between the elements of the embedded path.</span></span> <span data-ttu-id="58607-111">Например, путь к объекту "Class1Index = 3;" не содержит пробелов между именем свойства "Class1index" и присваиваемым ему значением "3".</span><span class="sxs-lookup"><span data-stu-id="58607-111">For example, the object path "Class1Index=3;" contains no space between the property name "Class1index" and the value being assigned, which is "3".</span></span>

<span data-ttu-id="58607-112">В следующем объявлении класса показано, как объявить строго типизированные и слабо типизированные внедренные объекты.</span><span class="sxs-lookup"><span data-stu-id="58607-112">The following class declaration shows you how to declare strongly typed and weakly typed embedded objects.</span></span>

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

<span data-ttu-id="58607-113">В следующих примерах описывается объявление внедренных объектов в объявлении класса.</span><span class="sxs-lookup"><span data-stu-id="58607-113">The following examples describe how to declare embedded objects within a class declaration.</span></span>

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

<span data-ttu-id="58607-114">В следующем примере описывается инициализация одного свойства, которое является строго типизированным объектом, и еще одно свойство, которое является массивом слабо типизированных объектов.</span><span class="sxs-lookup"><span data-stu-id="58607-114">The following example describes the initialization of one property that is a strongly typed object and another property that is an array of weakly typed objects.</span></span>

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

 

 



