---
description: Ключевое слово ссылки MOF описывает путь к объекту и сопоставляется с \_ типом автоматизации VT BSTR.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Ссылки (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911204"
---
# <a name="references-wmi"></a><span data-ttu-id="1d20e-103">Ссылки (WMI)</span><span class="sxs-lookup"><span data-stu-id="1d20e-103">References (WMI)</span></span>

<span data-ttu-id="1d20e-104">Ключевое слово **ссылки** MOF описывает путь к объекту и сопоставляется с \_ типом автоматизации VT BSTR.</span><span class="sxs-lookup"><span data-stu-id="1d20e-104">The MOF **ref** key word describes an object path and maps to a VT\_BSTR Automation type.</span></span> <span data-ttu-id="1d20e-105">Путь к объекту может быть либо полным путем к серверу, либо пространством имен, либо относительным путем к другому объекту в том же пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="1d20e-105">The object path can be either a full path to a server and namespace, or a relative path to another object in the same namespace.</span></span> <span data-ttu-id="1d20e-106">Чтобы связать два или несколько классов вместе, можно использовать ключевое слово **ref** .</span><span class="sxs-lookup"><span data-stu-id="1d20e-106">You can use a **ref** key word to link two or more classes together.</span></span> <span data-ttu-id="1d20e-107">Инструментарий WMI поддерживает два типа путей к объектам, которые используются для определения общих или определенных путей в WMI.</span><span class="sxs-lookup"><span data-stu-id="1d20e-107">WMI supports two types of object paths, which use to define general or specific paths within WMI.</span></span>

<span data-ttu-id="1d20e-108">Основное назначение ключевого слова **ref** заключается в сокращении времени транспорта и кодирования между объектами, которые находятся полностью в пределах репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="1d20e-108">The main purpose of the **ref** key word is to reduce transport time and encoding between objects that exist entirely within the WMI repository.</span></span> <span data-ttu-id="1d20e-109">Можно также использовать ключевое слово **ref** , чтобы создать ассоциацию между двумя классами.</span><span class="sxs-lookup"><span data-stu-id="1d20e-109">You can also use the **ref** key word to create an association between two classes.</span></span> <span data-ttu-id="1d20e-110">Дополнительные сведения см. в разделе [объявление класса ассоциации](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="1d20e-110">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span> <span data-ttu-id="1d20e-111">Если элемент, на который указывает ссылка, находится в том же MOF-файле, используйте псевдоним для инициализации значения **ref** .</span><span class="sxs-lookup"><span data-stu-id="1d20e-111">If the referenced item is located within the same MOF file, use an alias to initialize the **ref** value.</span></span> <span data-ttu-id="1d20e-112">Дополнительные сведения см. в разделе [Создание псевдонима](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="1d20e-112">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

> [!Note]  
> <span data-ttu-id="1d20e-113">При применении ключевого слова **ref** к свойству ключа можно отличать ссылки на объект по значению строки объекта, а не по значению разыменования.</span><span class="sxs-lookup"><span data-stu-id="1d20e-113">When a **ref** key word is applied to a key property, you can distinguish object references by the object string value instead of by the dereferenced value.</span></span>

 

<span data-ttu-id="1d20e-114">MOF поддерживает концепцию слабо типизированного и строго типизированного пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="1d20e-114">MOF supports the concept of a weakly typed and strongly typed object path.</span></span> <span data-ttu-id="1d20e-115">Слабо типизированный путь к объекту указывает на объект неопределенного класса и использует ключевое слово **ref** с ключевым словом [Object](object.md) .</span><span class="sxs-lookup"><span data-stu-id="1d20e-115">A weakly typed object path points to an object of an unspecified class and uses the **ref** key word with the [OBJECT](object.md) keyword.</span></span> <span data-ttu-id="1d20e-116">Строго типизированный объект указывает на объект определенного класса и использует **ref** с именем класса.</span><span class="sxs-lookup"><span data-stu-id="1d20e-116">A strongly typed object points to an object of a specific class and uses **ref** with the class name.</span></span> <span data-ttu-id="1d20e-117">В следующем примере описывается слабо типизированная ссылка **рефтоаникласс** , которая может указывать на любой класс или экземпляр класса, и ссылку **рефтокласскс** , которая может указывать только на класс или экземпляр **класскс** :</span><span class="sxs-lookup"><span data-stu-id="1d20e-117">The following example describes a weakly typed **RefToAnyClass** reference that can point to any class or class instance, and a **RefToClassX** reference that can point only to a **ClassX** class or instance:</span></span>

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

<span data-ttu-id="1d20e-118">В следующем примере описываются два экземпляра и объект Association, который ссылается на предыдущие экземпляры:</span><span class="sxs-lookup"><span data-stu-id="1d20e-118">The following example describes two instances and an association object that references the previous instances:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



