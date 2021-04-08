---
description: Как и многие другие методы MOF-файл (MOF), применение квалификатора к коду является относительно простым процессом.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Применение квалификатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819393"
---
# <a name="applying-a-qualifier"></a><span data-ttu-id="727a1-103">Применение квалификатора</span><span class="sxs-lookup"><span data-stu-id="727a1-103">Applying a Qualifier</span></span>

<span data-ttu-id="727a1-104">Как и многие другие методы MOF-файл (MOF), применение квалификатора к коду является относительно простым процессом.</span><span class="sxs-lookup"><span data-stu-id="727a1-104">Like many other techniques in Managed Object Format (MOF), applying a qualifier to your code is a relatively simple process.</span></span>

<span data-ttu-id="727a1-105">Единственная реальная сложность заключается в том, что в соглашениях об именовании, применяемых WMI, действуют следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="727a1-105">The only real challenges are the following restrictions in naming conventions that WMI enforces:</span></span>

-   <span data-ttu-id="727a1-106">Квалификатор может описывать класс, экземпляр, свойство, метод или параметр метода.</span><span class="sxs-lookup"><span data-stu-id="727a1-106">A qualifier can describe a class, instance, property, method, or method parameter.</span></span>
-   <span data-ttu-id="727a1-107">Имена квалификаторов не могут начинаться или заканчиваться символами подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="727a1-107">Qualifier names cannot have either leading or trailing underscores.</span></span>
-   <span data-ttu-id="727a1-108">Имя квалификатора не может начинаться с цифры.</span><span class="sxs-lookup"><span data-stu-id="727a1-108">A qualifier name cannot begin with a digit.</span></span>
-   <span data-ttu-id="727a1-109">Имя квалификатора не может содержать специальные символы, такие как & \* @!</span><span class="sxs-lookup"><span data-stu-id="727a1-109">A qualifier name cannot contain special characters such as & \* @ !</span></span><span data-ttu-id="727a1-110"> ~ \\ /.</span><span class="sxs-lookup"><span data-stu-id="727a1-110"> ~ \\ /.</span></span>
-   <span data-ttu-id="727a1-111">Все имена квалификаторов не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="727a1-111">All qualifier names are case-insensitive.</span></span>
-   <span data-ttu-id="727a1-112">Нельзя переопределить стандартные квалификаторы WMI или квалификаторы, описанные в спецификации CIM DMTF.</span><span class="sxs-lookup"><span data-stu-id="727a1-112">You cannot redefine the standard WMI qualifiers or any qualifiers described in the DMTF CIM specification.</span></span>
-   <span data-ttu-id="727a1-113">Типы квалификаторов не объявляются явным образом.</span><span class="sxs-lookup"><span data-stu-id="727a1-113">Qualifier types are not explicitly declared.</span></span>

    <span data-ttu-id="727a1-114">Если не объявляется тип квалификатора, WMI предполагает тип как логический со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="727a1-114">If you do not declare a qualifier type, WMI assumes the type as Boolean with a value of **TRUE**.</span></span> <span data-ttu-id="727a1-115">В противном случае квалификаторы типов WMI основываются на объявленных значениях квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="727a1-115">Otherwise, WMI types qualifiers based on the qualifier values you declare.</span></span>

-   <span data-ttu-id="727a1-116">При создании собственных квалификаторов необходимо добавить имя вашей схемы в имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="727a1-116">When creating your own qualifiers, you should prefix your schema name to your qualifier name.</span></span>

    <span data-ttu-id="727a1-117">Назначение этого правила заключается в предотвращении путаницы с новыми квалификаторами.</span><span class="sxs-lookup"><span data-stu-id="727a1-117">The purpose of this rule is to avoid confusion with new qualifiers.</span></span>

-   <span data-ttu-id="727a1-118">Можно создавать однородные массивы квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="727a1-118">You can create homogeneous arrays of qualifiers.</span></span>

    <span data-ttu-id="727a1-119">В следующем примере кода показано, как массивы квалификаторов указываются с фигурными скобками, окружающими значения.</span><span class="sxs-lookup"><span data-stu-id="727a1-119">The following code example shows how qualifier arrays are specified with curly braces that surround the values.</span></span>

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   <span data-ttu-id="727a1-120">Инструментарий WMI не поддерживает типы автоматизации, не указанные в ссылке, например VT \_ null.</span><span class="sxs-lookup"><span data-stu-id="727a1-120">WMI does not support automation types not listed in the reference, such as VT\_NULL.</span></span> <span data-ttu-id="727a1-121">Дополнительные сведения см. в разделе [типы данных MOF](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="727a1-121">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

<span data-ttu-id="727a1-122">Следующая процедура позволяет использовать C++ для добавления квалификатора к свойству.</span><span class="sxs-lookup"><span data-stu-id="727a1-122">The following procedure helps you to use C++ to add a qualifier to a property.</span></span>

<span data-ttu-id="727a1-123">**Применение квалификатора с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="727a1-123">**To apply a qualifier using C++**</span></span>

-   <span data-ttu-id="727a1-124">Примените квалификатор с помощью вызова метода [**ивбемкуалифиерсет::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="727a1-124">Apply the qualifier with a call to the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="727a1-125">Можно использовать другие методы [**ивбемкуалифиерсет**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) для извлечения или удаления существующих квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="727a1-125">You can use other methods of [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) to retrieve or delete existing qualifiers.</span></span>

<span data-ttu-id="727a1-126">Следующая процедура позволяет применить квалификатор в MOF-файлах.</span><span class="sxs-lookup"><span data-stu-id="727a1-126">The following procedure helps you to apply a qualifier in MOF files.</span></span>

<span data-ttu-id="727a1-127">**Описание ключевого слова или идентификатора с квалификатором с помощью MOF**</span><span class="sxs-lookup"><span data-stu-id="727a1-127">**To describe a keyword or identifier with a qualifier using MOF**</span></span>

-   <span data-ttu-id="727a1-128">Поместите квалификатор в квадратные скобки перед ключевым словом или идентификатором, описанным квалификатором.</span><span class="sxs-lookup"><span data-stu-id="727a1-128">Place a qualifier in brackets before the keyword or identifier described by the qualifier.</span></span>

    <span data-ttu-id="727a1-129">В следующем примере кода показано, как используются квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="727a1-129">The following code example shows how qualifiers are used.</span></span>

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    <span data-ttu-id="727a1-130">В следующем примере описывается правильное размещение квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="727a1-130">The following example describes the proper placement of qualifiers.</span></span>

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



