---
title: Рекомендации по COM и Юникод
description: Поскольку Microsoft Active Accessibility основан на модели COM, разработчикам нужен умеренный уровень понимания COM-объектов и интерфейсов и должен знать, как выполнять основные задачи (например, как инициализировать библиотеку COM).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710301"
---
# <a name="com-and-unicode-guidelines"></a><span data-ttu-id="bf909-103">Рекомендации по COM и Юникод</span><span class="sxs-lookup"><span data-stu-id="bf909-103">COM and Unicode Guidelines</span></span>

<span data-ttu-id="bf909-104">Поскольку Microsoft Active Accessibility основан на модели COM, разработчикам нужен умеренный уровень понимания COM-объектов и интерфейсов и должен знать, как выполнять основные задачи (например, как инициализировать библиотеку COM).</span><span class="sxs-lookup"><span data-stu-id="bf909-104">Because Microsoft Active Accessibility is based on Component Object Model (COM), developers need a moderate level of understanding about COM objects and interfaces and must know how to perform basic tasks (for example, how to initialize the COM library).</span></span> <span data-ttu-id="bf909-105">Разработчикам серверов необходимо понимать, как проектировать классы, реализующие интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , и как создавать объекты со специальными возможностями.</span><span class="sxs-lookup"><span data-stu-id="bf909-105">Server developers need to understand how to design classes that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and how to create accessible objects.</span></span>

<span data-ttu-id="bf909-106">Также необходим средний уровень понимания Юникода, чтобы использовать многие функции Microsoft Active Accessibility, возвращающие строки.</span><span class="sxs-lookup"><span data-stu-id="bf909-106">You also need a moderate level of understanding about Unicode to use many of the Microsoft Active Accessibility functions that return strings.</span></span>

<span data-ttu-id="bf909-107">Чтобы эффективно использовать Microsoft Active Accessibility, необходимо понимать следующие функции COM и Юникода, структуры, типы данных и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="bf909-107">To use Microsoft Active Accessibility effectively, you should understand the following COM and Unicode functions, structures, data types, and interfaces.</span></span> <span data-ttu-id="bf909-108">Ограниченные сведения о некоторых из этих элементов приведены в этой документации.</span><span class="sxs-lookup"><span data-stu-id="bf909-108">Limited information about some of these items is provided in this documentation.</span></span>

### <a name="functions"></a><span data-ttu-id="bf909-109">Функции</span><span class="sxs-lookup"><span data-stu-id="bf909-109">Functions:</span></span>

-   [<span data-ttu-id="bf909-110">**олеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="bf909-110">**OleInitialize**</span></span>](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   <span data-ttu-id="bf909-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span><span class="sxs-lookup"><span data-stu-id="bf909-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span></span>
-   <span data-ttu-id="bf909-112">[**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) и [ **IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span><span class="sxs-lookup"><span data-stu-id="bf909-112">[**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span></span>
-   <span data-ttu-id="bf909-113">[**Вариантинит**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) и [ **вариантклеар**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span><span class="sxs-lookup"><span data-stu-id="bf909-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span></span>
-   <span data-ttu-id="bf909-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) и [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span><span class="sxs-lookup"><span data-stu-id="bf909-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span></span>
-   <span data-ttu-id="bf909-115">[**Сисаллокстринг**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) и [ **сисфристринг**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span><span class="sxs-lookup"><span data-stu-id="bf909-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span></span>

### <a name="structures-and-data-types"></a><span data-ttu-id="bf909-116">Структуры и типы данных:</span><span class="sxs-lookup"><span data-stu-id="bf909-116">Structures and data types:</span></span>

-   [<span data-ttu-id="bf909-117">**ЗНАЧЕНИЕ**</span><span class="sxs-lookup"><span data-stu-id="bf909-117">**VARIANT**</span></span>](variant-structure.md)
-   [<span data-ttu-id="bf909-118">**СОСТАВ**</span><span class="sxs-lookup"><span data-stu-id="bf909-118">**HRESULT**</span></span>](/windows/desktop/com/structure-of-com-error-codes)
-   [<span data-ttu-id="bf909-119">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="bf909-119">**BSTR**</span></span>](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a><span data-ttu-id="bf909-120">COM-интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="bf909-120">COM Interfaces:</span></span>

-   [<span data-ttu-id="bf909-121">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="bf909-121">**IUnknown**</span></span>](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [<span data-ttu-id="bf909-122">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="bf909-122">**IDispatch**</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="bf909-123">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="bf909-123">**IEnumVARIANT**</span></span>](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a><span data-ttu-id="bf909-124">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="bf909-124">In this section</span></span>

-   [<span data-ttu-id="bf909-125">Структура варианта</span><span class="sxs-lookup"><span data-stu-id="bf909-125">VARIANT Structure</span></span>](variant-structure.md)
-   [<span data-ttu-id="bf909-126">Интерфейс IDispatch</span><span class="sxs-lookup"><span data-stu-id="bf909-126">IDispatch Interface</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="bf909-127">Преобразование строк Юникода и ANSI</span><span class="sxs-lookup"><span data-stu-id="bf909-127">Converting Unicode and ANSI Strings</span></span>](converting-unicode-and-ansi-strings.md)

 

 