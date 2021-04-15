---
description: Вы можете объявить базовый экземпляр класса в службе управления Windows с помощью MOF-файл (MOF). Можно также переопределить значения по умолчанию для экземпляра. Дополнительные сведения см. в разделе Установка значения свойства экземпляра.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Создание экземпляра с помощью MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702079"
---
# <a name="creating-an-instance-using-mof"></a><span data-ttu-id="a3fff-105">Создание экземпляра с помощью MOF</span><span class="sxs-lookup"><span data-stu-id="a3fff-105">Creating an Instance Using MOF</span></span>

<span data-ttu-id="a3fff-106">Вы можете объявить базовый экземпляр класса в службе управления Windows с помощью MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a3fff-106">You can declare a basic instance of a class in the Windows Management service using Managed Object Format (MOF).</span></span> <span data-ttu-id="a3fff-107">Можно также переопределить значения по умолчанию для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a3fff-107">You can also override the default values for an instance.</span></span> <span data-ttu-id="a3fff-108">Дополнительные сведения см. в разделе [Установка значения свойства экземпляра](#setting-an-instance-property-value).</span><span class="sxs-lookup"><span data-stu-id="a3fff-108">For more information, see [Setting an Instance Property Value](#setting-an-instance-property-value).</span></span>

<span data-ttu-id="a3fff-109">В следующей процедуре описывается объявление базового экземпляра класса с помощью MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a3fff-109">The following procedure describes how to declare a basic instance of a class using MOF code.</span></span>

<span data-ttu-id="a3fff-110">**Объявление базового экземпляра класса с помощью MOF-кода**</span><span class="sxs-lookup"><span data-stu-id="a3fff-110">**To declare a basic instance of a class using MOF code**</span></span>

1.  <span data-ttu-id="a3fff-111">Используйте **экземпляр** ключевых слов, за которым следует имя класса, фигурные скобки и точку с запятой.</span><span class="sxs-lookup"><span data-stu-id="a3fff-111">Use the **Instance of** keywords followed by the class name, curly braces, and a semicolon.</span></span>

    <span data-ttu-id="a3fff-112">В следующем примере кода показано, как объявить экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="a3fff-112">The following code example shows how to declare an instance of a class.</span></span>

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  <span data-ttu-id="a3fff-113">По завершении вставьте MOF-код в репозиторий WMI с помощью компилятора MOF.</span><span class="sxs-lookup"><span data-stu-id="a3fff-113">When finished, insert your MOF code into the WMI repository using the MOF compiler.</span></span>

    <span data-ttu-id="a3fff-114">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="a3fff-114">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="a3fff-115">Экземпляр класса включает все свойства класса.</span><span class="sxs-lookup"><span data-stu-id="a3fff-115">An instance of a class includes all of the properties of the class.</span></span> <span data-ttu-id="a3fff-116">Если класс является производным классом, то экземпляры включают свойства, относящиеся ко всем классам, находящихся выше в иерархии.</span><span class="sxs-lookup"><span data-stu-id="a3fff-116">If the class is a derived class, instances include the properties belonging to all of the classes higher in the hierarchy.</span></span> <span data-ttu-id="a3fff-117">Каждый класс, на основе которого создается экземпляр, имеет одно или несколько ключевых свойств.</span><span class="sxs-lookup"><span data-stu-id="a3fff-117">Each class that an instance is created from has one or more key properties.</span></span> <span data-ttu-id="a3fff-118">Нельзя создать экземпляр с более чем 256 ключами.</span><span class="sxs-lookup"><span data-stu-id="a3fff-118">You cannot create an instance with more than 256 keys.</span></span>

## <a name="setting-an-instance-property-value"></a><span data-ttu-id="a3fff-119">Установка значения свойства экземпляра</span><span class="sxs-lookup"><span data-stu-id="a3fff-119">Setting an Instance Property Value</span></span>

<span data-ttu-id="a3fff-120">Так как WMI строго типизированные свойства, изменять типы свойств нельзя.</span><span class="sxs-lookup"><span data-stu-id="a3fff-120">Because WMI strongly types properties, you cannot modify property types.</span></span> <span data-ttu-id="a3fff-121">Однако значения свойств можно задавать в экземплярах.</span><span class="sxs-lookup"><span data-stu-id="a3fff-121">You can, however, set property values in instances.</span></span> <span data-ttu-id="a3fff-122">Когда класс присваивает свойству значение по умолчанию, Инструментарий WMI присваивает каждому экземпляру значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3fff-122">When a class assigns a default value to a property, WMI assigns the default value to each instance.</span></span> <span data-ttu-id="a3fff-123">Это значение можно переопределить в объявлении экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a3fff-123">You can override this value in your instance declaration.</span></span>

<span data-ttu-id="a3fff-124">Следующая процедура описывает, как задать значение свойства или перезаписать значение по умолчанию с помощью MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a3fff-124">The following procedure describes how to set a property value or overwrite a default value using MOF code.</span></span>

<span data-ttu-id="a3fff-125">**Установка значения свойства или перезапись значения по умолчанию с помощью MOF-кода**</span><span class="sxs-lookup"><span data-stu-id="a3fff-125">**To set a property value or overwrite a default value using MOF code**</span></span>

1.  <span data-ttu-id="a3fff-126">Поместите оператор присваивания между фигурными скобками объявления экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a3fff-126">Place an assignment statement between the curly braces of the instance declaration.</span></span>

    <span data-ttu-id="a3fff-127">В следующем примере кода показано, как задать значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a3fff-127">The following code example shows how to set a property value.</span></span>

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    <span data-ttu-id="a3fff-128">Инструментарию WMI не требуется задавать какое бы то ни было свойство во время создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a3fff-128">WMI does not require that you set any property during instance creation.</span></span> <span data-ttu-id="a3fff-129">Исключением является любое свойство, помеченное квалификатором [**ключа**](key-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="a3fff-129">The exception is any property marked with the [**Key**](key-qualifier.md) qualifier.</span></span> <span data-ttu-id="a3fff-130">Так как инструментарий WMI использует ключевые свойства для уникальной идентификации экземпляров, необходимо задать все ключевые свойства в том виде, в котором они встречаются.</span><span class="sxs-lookup"><span data-stu-id="a3fff-130">Because WMI uses key properties to uniquely identify instances, you must set all key properties as you encounter them.</span></span> <span data-ttu-id="a3fff-131">В отличие от этого, не следует задавать системное свойство в объявлении экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a3fff-131">In contrast, you must not set a system property in an instance declaration.</span></span> <span data-ttu-id="a3fff-132">Вместо этого при необходимости Инструментарий WMI присваивает соответствующие значения системному свойству.</span><span class="sxs-lookup"><span data-stu-id="a3fff-132">Instead, WMI assigns the appropriate values to a system property when necessary.</span></span>

2.  <span data-ttu-id="a3fff-133">По завершении вставьте код MOF в репозиторий WMI, вызвав компилятор MOF.</span><span class="sxs-lookup"><span data-stu-id="a3fff-133">When finished, insert your MOF code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="a3fff-134">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="a3fff-134">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="a3fff-135">В следующем примере кода показано, как экземпляр задает данные для свойств, определенных классом.</span><span class="sxs-lookup"><span data-stu-id="a3fff-135">The following code examples show how an instance specifies data for properties defined by a class.</span></span>

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

<span data-ttu-id="a3fff-136">В предыдущем примере класс определяет три свойства: строку символов, 32-разрядное целое число со знаком и 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a3fff-136">In the preceding example, the class defines three properties: a character string, a 32-bit signed integer, and a 32-bit unsigned integer.</span></span> <span data-ttu-id="a3fff-137">Экземпляр предоставляет значения данных для каждого из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="a3fff-137">The instance provides data values for each of these properties.</span></span>

 

 



