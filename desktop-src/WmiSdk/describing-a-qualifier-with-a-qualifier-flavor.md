---
description: Разновидность квалификатора — это флаг, описывающий дополнительные сведения об квалификаторе.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Описание квалификатора с флагом квалификатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263934"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a><span data-ttu-id="67c92-103">Описание квалификатора с флагом квалификатора</span><span class="sxs-lookup"><span data-stu-id="67c92-103">Describing a Qualifier with a Qualifier Flavor</span></span>

<span data-ttu-id="67c92-104">[*Разновидность квалификатора*](gloss-q.md) — это флаг, описывающий дополнительные сведения об квалификаторе.</span><span class="sxs-lookup"><span data-stu-id="67c92-104">A [*qualifier flavor*](gloss-q.md) is a flag that describes more information about a qualifier.</span></span> <span data-ttu-id="67c92-105">Например, ограничение ограниченного квалификатора указывает, что инструментарий WMI не должен распространять связанный квалификатор на все производные классы или экземпляры.</span><span class="sxs-lookup"><span data-stu-id="67c92-105">For example, the Restricted qualifier flavor states that WMI should not propagate the associated qualifier to any derived classes or instances.</span></span> <span data-ttu-id="67c92-106">Установить флаги можно с помощью кода MOF или программно.</span><span class="sxs-lookup"><span data-stu-id="67c92-106">You can set flavors using either MOF code or programmatically.</span></span> <span data-ttu-id="67c92-107">Несмотря на то, что можно описать разнообразные эффекты с помощью разновидностей, основное назначение флагов разновидностей заключается в том, чтобы определить, как WMI распространяет квалификаторы с помощью наследования.</span><span class="sxs-lookup"><span data-stu-id="67c92-107">While you can describe a variety of effects with flavors, the main purposes of flavor flags is to define how WMI propagates qualifiers through inheritance.</span></span>

<span data-ttu-id="67c92-108">Инструментарий WMI определяет несколько разновидностей квалификаторов, которые можно присоединить к любому квалификатору независимо от источника квалификатора.</span><span class="sxs-lookup"><span data-stu-id="67c92-108">WMI defines several qualifier flavors that you can attach to any qualifier, regardless of the origin of the qualifier.</span></span> <span data-ttu-id="67c92-109">Однако некоторые разновидности не подходят для всех типов квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="67c92-109">However, some flavors are not appropriate for all qualifier types.</span></span> <span data-ttu-id="67c92-110">Например, флаг **ToSubClass** подходит только для квалификаторов, определенных для класса.</span><span class="sxs-lookup"><span data-stu-id="67c92-110">The **ToSubClass** flavor, for example, is appropriate only for qualifiers defined for a class.</span></span> <span data-ttu-id="67c92-111">Нельзя присоединить **ToSubClass** к квалификатору, используемому для описания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="67c92-111">You cannot attach **ToSubClass** to a qualifier used to describe an instance.</span></span>

<span data-ttu-id="67c92-112">С помощью разновидностей можно описать различные эффекты для квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="67c92-112">You can use flavors to describe a variety of different effects for qualifiers.</span></span> <span data-ttu-id="67c92-113">Например, версия может указывать, можно ли локализовать квалификатор.</span><span class="sxs-lookup"><span data-stu-id="67c92-113">For example, flavor can indicate if a qualifier can be localized.</span></span> <span data-ttu-id="67c92-114">Однако одна из основных целей разновидности квалификатора заключается в том, чтобы описать, может ли родительский класс передавать квалификаторы в класс или экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="67c92-114">However, one of the main purposes of a qualifier flavor is to describe whether a parent class can pass qualifiers to a subclass or class instance.</span></span> <span data-ttu-id="67c92-115">Кроме того, с помощью флагов можно определить, передает ли свойство класса квалификатор в свойство экземпляра.</span><span class="sxs-lookup"><span data-stu-id="67c92-115">You can also use flavors to determine if a class property passes a qualifier on to an instance property.</span></span> <span data-ttu-id="67c92-116">Наконец, используйте флаги, чтобы указать, может ли подкласс переопределять исходное значение унаследованного квалификатора.</span><span class="sxs-lookup"><span data-stu-id="67c92-116">Finally, use flavors to state whether a subclass can override the original value of an inherited qualifier.</span></span> <span data-ttu-id="67c92-117">Однако квалификаторы, объявляемые для класса или экземпляра, не распространяются на свойства этого класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="67c92-117">However, qualifiers that you declare for a class or instance do not propagate to the properties of that class or instance.</span></span> <span data-ttu-id="67c92-118">Кроме того, разновидности, устанавливающие разрешения на переопределение, допустимы только в том случае, если заданы флаги **тоинстанце** или **ToSubClass** .</span><span class="sxs-lookup"><span data-stu-id="67c92-118">Further, flavors that establish override permissions are valid only if you also set the **ToInstance** or **ToSubClass** flavors.</span></span>

<span data-ttu-id="67c92-119">Разновидность можно глобально назначить квалификатору для всего MOF-файла с помощью следующего синтаксиса, в котором пробел действует как разделитель, если задано несколько разновидностей.</span><span class="sxs-lookup"><span data-stu-id="67c92-119">A flavor can be globally assigned to a qualifier for an entire MOF file using the following syntax in which white space acts as the delimiter when multiple flavors are specified.</span></span>

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

<span data-ttu-id="67c92-120">Глобальные разновидности применяются ко всем последующим применениям квалификатора в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="67c92-120">Global flavors apply to all subsequent uses of the qualifier in the MOF file.</span></span> <span data-ttu-id="67c92-121">Глобальные инструкции типа могут находиться в файле за пределами блока объявления объекта.</span><span class="sxs-lookup"><span data-stu-id="67c92-121">Global flavor statements may occur anywhere in the file outside of an object declaration block.</span></span> <span data-ttu-id="67c92-122">Флаги, переопределенные на уровне класса, экземпляра или свойства, переопределяют глобальные объявления разновидностей для области этого объекта.</span><span class="sxs-lookup"><span data-stu-id="67c92-122">Flavors redefined at the class, instance, or property level override the global flavor declarations for the scope of that object.</span></span>

<span data-ttu-id="67c92-123">Невозможно определить новую разновидность.</span><span class="sxs-lookup"><span data-stu-id="67c92-123">You cannot define a new flavor.</span></span> <span data-ttu-id="67c92-124">Хотя можно создать новый квалификатор, используйте только существующие [разновидности квалификаторов](qualifier-flavors.md) для описания нового квалификатора.</span><span class="sxs-lookup"><span data-stu-id="67c92-124">Although you can create a new qualifier, use only existing [Qualifier Flavors](qualifier-flavors.md) to describe your new qualifier.</span></span>

<span data-ttu-id="67c92-125">**Определение разновидностей квалификаторов в MOF**</span><span class="sxs-lookup"><span data-stu-id="67c92-125">**To define qualifier flavors in MOF**</span></span>

-   <span data-ttu-id="67c92-126">Объявите флаги, описывающие заданный квалификатор после имени квалификатора, между квадратными скобками.</span><span class="sxs-lookup"><span data-stu-id="67c92-126">Declare the flavors that describe a given qualifier after the qualifier name, between the qualifier brackets.</span></span> <span data-ttu-id="67c92-127">Используйте пробелы в качестве разделителя между несколькими разновидностями.</span><span class="sxs-lookup"><span data-stu-id="67c92-127">Use white space as the delimiter between multiple flavors.</span></span>

    <span data-ttu-id="67c92-128">В следующем примере показан шаблон для присоединения предопределенных описателей.</span><span class="sxs-lookup"><span data-stu-id="67c92-128">The following example shows the pattern for attaching predefined qualifiers.</span></span>

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

<span data-ttu-id="67c92-129">Атрибуты квалификатора можно добавлять программным способом только в C++.</span><span class="sxs-lookup"><span data-stu-id="67c92-129">You can add qualifier flavors programmatically only in C++.</span></span> <span data-ttu-id="67c92-130">Эта операция недоступна в [API скриптов для WMI](scripting-api-for-wmi.md), хотя можно добавить новый квалификатор, вызвав [**свбемкуалифиерсет. Add**](swbemqualifierset-add.md).</span><span class="sxs-lookup"><span data-stu-id="67c92-130">This operation is not available in the [Scripting API for WMI](scripting-api-for-wmi.md), although you can add a new qualifier by calling [**SWbemQualifierSet.Add**](swbemqualifierset-add.md).</span></span>

<span data-ttu-id="67c92-131">**Назначение разновидности с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="67c92-131">**To assign a flavor using C++**</span></span>

-   <span data-ttu-id="67c92-132">Вызовите метод [**ивбемкуалифиерсет::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) с параметром *лфлавор* , для которого задана одна из констант, определенных для метода.</span><span class="sxs-lookup"><span data-stu-id="67c92-132">Call the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method with the *lFlavor* parameter set to one of the constants defined for the method.</span></span>

 

 



