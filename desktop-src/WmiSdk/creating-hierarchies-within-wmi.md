---
description: Пространство имен WMI — это программный объект, определяющий область для набора классов и экземпляров. Классы поставщиков WMI должны быть определены внутри пространства имен.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Создание иерархий в WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263939"
---
# <a name="creating-hierarchies-within-wmi"></a><span data-ttu-id="add3f-104">Создание иерархий в WMI</span><span class="sxs-lookup"><span data-stu-id="add3f-104">Creating Hierarchies Within WMI</span></span>

<span data-ttu-id="add3f-105">[*Пространство имен WMI*](gloss-n.md) — это программный объект, определяющий область для набора классов и экземпляров.</span><span class="sxs-lookup"><span data-stu-id="add3f-105">[*WMI namespace*](gloss-n.md) is a programming object that defines the scope for a set of classes and instances.</span></span> <span data-ttu-id="add3f-106">Классы поставщиков WMI должны быть определены внутри пространства имен.</span><span class="sxs-lookup"><span data-stu-id="add3f-106">WMI provider classes must be defined inside a namespace.</span></span>

<span data-ttu-id="add3f-107">Пространства имен описывают различные управляемые среды, такие как среда SMS.</span><span class="sxs-lookup"><span data-stu-id="add3f-107">Namespaces describe different managed environments, such as the SMS environment.</span></span> <span data-ttu-id="add3f-108">Поскольку классы и экземпляры схемы определяют компоненты управляемой среды, для каждой новой схемы требуется новое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="add3f-108">Because the classes and instances of a schema define the components of a managed environment, each new schema requires a new namespace.</span></span> <span data-ttu-id="add3f-109">Например, корневое \\ пространство имен CIMV2 содержит классы и экземпляры, определенные в схеме Win32, а также классы родительских модель CIM (CIM), из которых наследуется схема Win32.</span><span class="sxs-lookup"><span data-stu-id="add3f-109">For example, the root\\cimv2 namespace contains the classes and instances defined in the Win32 schema as well as the parent Common Information Model (CIM) classes from which the Win32 schema inherits.</span></span> <span data-ttu-id="add3f-110">Классы CIM определяются с помощью задачи распределенного управления "принудительная задача" ([DMTF](https://www.dmtf.org/home)).</span><span class="sxs-lookup"><span data-stu-id="add3f-110">CIM classes are defined by the Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).</span></span>

> [!Note]  
> <span data-ttu-id="add3f-111">Чтобы гарантировать, что все определения классов WMI для управляемых объектов будут восстановлены в [*репозитории WMI*](gloss-w.md) в случае сбоя и перезапуска WMI, воспользуйтесь инструкцией препроцессора [**\# pragma автовосстановления**](pragma-autorecover.md) в [*MOF-файл (MOF-файл)*](gloss-m.md) .</span><span class="sxs-lookup"><span data-stu-id="add3f-111">To ensure that all of your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format (MOF)*](gloss-m.md) file.</span></span>

 

<span data-ttu-id="add3f-112">WMI определяет пространство имен как экземпляр класса системы [**\_ \_ пространства имен**](--namespace.md) или любого класса, производного от **\_ \_ Namespace**.</span><span class="sxs-lookup"><span data-stu-id="add3f-112">WMI defines a namespace as an instance of the [**\_\_Namespace**](--namespace.md) system class or any class that derives from **\_\_Namespace**.</span></span> <span data-ttu-id="add3f-113">Класс системы **\_ \_ пространства имен** имеет одно свойство **Name**, которое должно быть уникальным в пределах области родительского пространства имен.</span><span class="sxs-lookup"><span data-stu-id="add3f-113">The **\_\_Namespace** system class has a single property called **Name**, which must be unique within the scope of the parent namespace.</span></span> <span data-ttu-id="add3f-114">Свойство **Name** также должно содержать строку, которая начинается с буквы.</span><span class="sxs-lookup"><span data-stu-id="add3f-114">The **Name** property must also contain a string that begins with a letter.</span></span> <span data-ttu-id="add3f-115">Все остальные символы в строке могут быть буквами, цифрами или символами подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="add3f-115">All other characters in the string can be letters, digits, or underscores.</span></span> <span data-ttu-id="add3f-116">Все символы не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="add3f-116">All characters are case-insensitive.</span></span>

<span data-ttu-id="add3f-117">Помимо определения уникального имени для дочернего пространства имен, родительское пространство имен WMI может защищать статические экземпляры классов от случайного изменения другими поставщиками.</span><span class="sxs-lookup"><span data-stu-id="add3f-117">In addition to determining the unique name for a child namespace, the parent WMI namespace can protect the static instances of your classes from accidental modification by other providers.</span></span> <span data-ttu-id="add3f-118">Например, может оказаться удобным вкладывать новое пространство имен в существующее пространство имен для другого поставщика.</span><span class="sxs-lookup"><span data-stu-id="add3f-118">For example, you may find it convenient to nest a new namespace under an existing namespace for another provider.</span></span> <span data-ttu-id="add3f-119">Однако исходный поставщик может попытаться обновить все экземпляры класса в соответствии с новой схемой.</span><span class="sxs-lookup"><span data-stu-id="add3f-119">However, the original provider may try to update all class instances to match up with a new schema.</span></span> <span data-ttu-id="add3f-120">При этом исходный поставщик может удалить все вложенные дочерние элементы в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="add3f-120">In doing so, the original provider may delete all sub-children in a namespace.</span></span> <span data-ttu-id="add3f-121">Хотя это действие может быть подходящим для целевого пространства имен, оно может повлиять на несвязанные экземпляры классов в дочернем пространстве имен (т. е. собственных классах поставщика).</span><span class="sxs-lookup"><span data-stu-id="add3f-121">While this may be an appropriate action for the target namespace, it may affect unrelated class instances in a child namespace (i.e., your own provider classes).</span></span>

<span data-ttu-id="add3f-122">Поэтому обычно рекомендуется создавать и регистрировать пространство имен отдельно от пространств имен, которыми вы не управляете напрямую.</span><span class="sxs-lookup"><span data-stu-id="add3f-122">Therefore, it is generally recommended that you create and register your namespace as separate from namespaces that you do not directly control.</span></span> <span data-ttu-id="add3f-123">Это особенно верно, если классы являются производными только от общих классов CIM или от других классов компании.</span><span class="sxs-lookup"><span data-stu-id="add3f-123">This is especially true if your classes derive only from general CIM classes or other classes from your company.</span></span> <span data-ttu-id="add3f-124">Пространство имен может находиться в **корневом** пространстве имен, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="add3f-124">Your namespace can be under the **Root** namespace, such as the following:</span></span>

<span data-ttu-id="add3f-125">**Root/myCompany/Мипродукт**</span><span class="sxs-lookup"><span data-stu-id="add3f-125">**Root/myCompany/myProduct**</span></span>

<span data-ttu-id="add3f-126">В отличие от этого, если новый класс является производным от класса другого поставщика, может потребоваться сохранить класс в подпространстве имен этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="add3f-126">In contrast, if your new class derives from the class of another provider, you may need to store your class in a sub-namespace of that provider.</span></span> <span data-ttu-id="add3f-127">Обратите внимание, что это предоставляет новому классу возможность случайного удаления от исходного поставщика.</span><span class="sxs-lookup"><span data-stu-id="add3f-127">Note that this exposes your new class to accidental deletion by the original provider.</span></span>

<span data-ttu-id="add3f-128">Инструментарий WMI предоставляет несколько различных способов создания пространства имен:</span><span class="sxs-lookup"><span data-stu-id="add3f-128">WMI provides several different ways to create a namespace:</span></span>

-   [<span data-ttu-id="add3f-129">Создание дочернего пространства имен с помощью MOF-кода</span><span class="sxs-lookup"><span data-stu-id="add3f-129">Creating a Child Namespace with MOF Code</span></span>](creating-a-child-namespace-with-mof-code.md)
-   [<span data-ttu-id="add3f-130">Создание родственного пространства имен с помощью MOF-кода</span><span class="sxs-lookup"><span data-stu-id="add3f-130">Creating a Sibling Namespace with MOF Code</span></span>](creating-a-sibling-namespace-with-mof-code.md)
-   [<span data-ttu-id="add3f-131">Создание пространства имен с помощью API инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="add3f-131">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a><span data-ttu-id="add3f-132">См. также</span><span class="sxs-lookup"><span data-stu-id="add3f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="add3f-133">Разработка классов MOF-файл (MOF)</span><span class="sxs-lookup"><span data-stu-id="add3f-133">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



