---
title: Использование заметки с картой значений
description: Пример кода см. в разделе пример заметки к карте значений.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413017"
---
# <a name="using-value-map-annotation"></a><span data-ttu-id="4bda7-103">Использование заметки с картой значений</span><span class="sxs-lookup"><span data-stu-id="4bda7-103">Using Value Map Annotation</span></span>

<span data-ttu-id="4bda7-104">**Создание схемы значений**</span><span class="sxs-lookup"><span data-stu-id="4bda7-104">**To create a value map**</span></span>

1.  <span data-ttu-id="4bda7-105">**Создайте строку сопоставления.**</span><span class="sxs-lookup"><span data-stu-id="4bda7-105">**Create a mapping string.**</span></span>

    <span data-ttu-id="4bda7-106">Строка сопоставления — это список числовых значений элемента управления, соответствующих удобочитаемой строке в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="4bda7-106">A mapping string is a list of a control's numeric values corresponding to a human-readable string in Unicode.</span></span> <span data-ttu-id="4bda7-107">Он начинается с "A:", за которым следует число, указывающее тип используемого индекса.</span><span class="sxs-lookup"><span data-stu-id="4bda7-107">It starts with "A:" followed by a number that indicates the type of index used.</span></span> <span data-ttu-id="4bda7-108">Поддерживаются только индексы изображений; Поэтому тип индекса всегда равен 0.</span><span class="sxs-lookup"><span data-stu-id="4bda7-108">Only image indexes are supported; therefore the index type is always 0.</span></span>

    <span data-ttu-id="4bda7-109">За строкой следуют следующие пары: индекс: результат.</span><span class="sxs-lookup"><span data-stu-id="4bda7-109">The string is followed by :index:result pairs.</span></span> <span data-ttu-id="4bda7-110">"Index" — это число, представляющее индекс изображения для List-View или представления дерева или значение для элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="4bda7-110">The "index" is a number representing an image index for a List-View or Tree-View, or the value for a slider control.</span></span>

    <span data-ttu-id="4bda7-111">Полученное значение представляет собой число, полученное при сопоставлении свойства Role или State для представления списка или элемента управления иерархического представления.</span><span class="sxs-lookup"><span data-stu-id="4bda7-111">The resulting value is a number obtained when you map the Role or State property for a list view or tree view control.</span></span> <span data-ttu-id="4bda7-112">Такие числа выражаются в десятичном или шестнадцатеричном формате с префиксом "0x".</span><span class="sxs-lookup"><span data-stu-id="4bda7-112">Such numbers are expressed in decimal or hexadecimal with an "0x" prefix.</span></span>

    <span data-ttu-id="4bda7-113">Строка сопоставления всегда заканчивается завершающим двоеточием (":").</span><span class="sxs-lookup"><span data-stu-id="4bda7-113">The mapping string is always terminated with a final colon (":").</span></span>

    <span data-ttu-id="4bda7-114">Ниже приведен пример отображения заметки для свойств State и Role флажка в представлении списка или элементе управления иерархического представления.</span><span class="sxs-lookup"><span data-stu-id="4bda7-114">The following is an example of an annotation map for the State and Role properties of a check box in a list view or tree view control.</span></span> <span data-ttu-id="4bda7-115">В представлении есть два элемента, представляющих флажки, каждый из которых имеет изображения, соответствующие установленному и непроверенному состоянию.</span><span class="sxs-lookup"><span data-stu-id="4bda7-115">There are two items in the view that represent check boxes, and each has images corresponding to the checked and unchecked state.</span></span>

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    <span data-ttu-id="4bda7-116">Допустимые значения ролей и состояний см. в разделе [роли объектов](object-roles.md) и [константы состояния объектов](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4bda7-116">For valid Role and State values, see [Object Roles](object-roles.md) and [Object State Constants](object-state-constants.md).</span></span>

    <span data-ttu-id="4bda7-117">Значение индекса может быть отрицательным при сопоставлении свойств для элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="4bda7-117">The index value may be negative when you map properties for a slider control.</span></span>

    <span data-ttu-id="4bda7-118">При сопоставлении свойства Value или Description результатом будет строка.</span><span class="sxs-lookup"><span data-stu-id="4bda7-118">When you map a Value or Description property, the result is a string.</span></span> <span data-ttu-id="4bda7-119">Строки не заключаются в кавычки, а двоеточия действуют как разделители.</span><span class="sxs-lookup"><span data-stu-id="4bda7-119">Strings are not quoted and the colons act as delimiters.</span></span>

    <span data-ttu-id="4bda7-120">Дополнительные сведения см. в разделе [Формат отображения заметок](value-map-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="4bda7-120">For more information, see [Annotation Map Format](value-map-annotation.md).</span></span>

2.  <span data-ttu-id="4bda7-121">**Создайте диспетчер заметок и получите указатель на его** интерфейс [**иаккпропсервицес**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**.**</span><span class="sxs-lookup"><span data-stu-id="4bda7-121">**Create the annotation manager and obtain a pointer to its**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**interface.**</span></span>

    <span data-ttu-id="4bda7-122">Ниже приведен пример создания диспетчера заметок.</span><span class="sxs-lookup"><span data-stu-id="4bda7-122">The following is an example of how to create the annotation manager.</span></span>

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  <span data-ttu-id="4bda7-123">**Присоедините строку сопоставления к элементу управления.**</span><span class="sxs-lookup"><span data-stu-id="4bda7-123">**Attach the mapping string to the control.**</span></span>

    <span data-ttu-id="4bda7-124">Вызовите [**иаккпропсервицес:: сесвндпропстр**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), передав **HWND** элемента управления и указатель на строку сопоставления.</span><span class="sxs-lookup"><span data-stu-id="4bda7-124">Call [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passing the **HWND** of the control and a pointer to the mapping string.</span></span>

    <span data-ttu-id="4bda7-125">Параметр *идпроп* будет иметь один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="4bda7-125">The *IdProp* parameter will be one of the following.</span></span>

    

    | <span data-ttu-id="4bda7-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="4bda7-126">Parameter</span></span>                   | <span data-ttu-id="4bda7-127">Используется для</span><span class="sxs-lookup"><span data-stu-id="4bda7-127">Used for</span></span>                                                |
    |-----------------------------|---------------------------------------------------------|
    | <span data-ttu-id="4bda7-128">МСААПРОПИД \_ ролемап</span><span class="sxs-lookup"><span data-stu-id="4bda7-128">MSAAPROPID\_ROLEMAP</span></span>         | <span data-ttu-id="4bda7-129">Для задания схемы роли для элементов управления представления списка или дерева.</span><span class="sxs-lookup"><span data-stu-id="4bda7-129">To set a role map for list view or tree view controls.</span></span>  |
    | <span data-ttu-id="4bda7-130">МСААПРОПИД \_ статемап</span><span class="sxs-lookup"><span data-stu-id="4bda7-130">MSAAPROPID\_STATEMAP</span></span>        | <span data-ttu-id="4bda7-131">Задание отображения состояния для представления списка или элементов управления иерархического представления.</span><span class="sxs-lookup"><span data-stu-id="4bda7-131">To set a state map for list view or tree view controls.</span></span> |
    | <span data-ttu-id="4bda7-132">PROPID \_ ACC \_ дескриптионмап</span><span class="sxs-lookup"><span data-stu-id="4bda7-132">PROPID\_ACC\_DESCRIPTIONMAP</span></span> | <span data-ttu-id="4bda7-133">Для задания схемы описания представления списка или представления в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="4bda7-133">To set a description map for list view or tree views.</span></span>   |
    | <span data-ttu-id="4bda7-134">МСААПРОПИД \_ VALUEMAP</span><span class="sxs-lookup"><span data-stu-id="4bda7-134">MSAAPROPID\_VALUEMAP</span></span>        | <span data-ttu-id="4bda7-135">Чтобы задать карту значений для элементов управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="4bda7-135">To set a value map on slider controls.</span></span>                  |

    

     

4.  <span data-ttu-id="4bda7-136">**Очистка.**</span><span class="sxs-lookup"><span data-stu-id="4bda7-136">**Clean up.**</span></span>

    <span data-ttu-id="4bda7-137">Перед удалением элементов управления с аннотацией значений (например, при обработке [WM \_ destroy](../winmsg/wm-destroy.md)) необходимо очистить ранее зарегистрированные свойства и отпустить диспетчер заметок.</span><span class="sxs-lookup"><span data-stu-id="4bda7-137">Before you destroy any value map annotated controls (for example, when handling [WM\_DESTROY](../winmsg/wm-destroy.md)), you must clear previously registered properties and release the annotation manager.</span></span>

    <span data-ttu-id="4bda7-138">Для этого вызовите [**иаккпропсервицес:: клеархвндпропс**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) , как нужно, и отпустите указатель на [**иаккпропсервицес**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span><span class="sxs-lookup"><span data-stu-id="4bda7-138">To do this, call [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) as appropriate and release your pointer to [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span></span>

<span data-ttu-id="4bda7-139">Пример кода см. в разделе [Пример заметки к карте значений](value-map-annotation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4bda7-139">For sample code, see [Value Map Annotation Sample](value-map-annotation-sample.md).</span></span>

 

 