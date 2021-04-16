---
title: Аннотация схемы значений
description: Аннотация схемы значений
ms.assetid: f7c9304a-0eed-4a73-ab06-56723f3cfa5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d21b04374344475689989c2570af6975dc97c13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104556687"
---
# <a name="value-map-annotation"></a><span data-ttu-id="97066-103">Аннотация схемы значений</span><span class="sxs-lookup"><span data-stu-id="97066-103">Value Map Annotation</span></span>

<span data-ttu-id="97066-104">С помощью аннотации карты значений можно использовать строку сопоставления, чтобы указать, каким образом индекс изображения элемента в представлении списка или дерева соответствует его роли или состоянию.</span><span class="sxs-lookup"><span data-stu-id="97066-104">With value map annotation, you can use a mapping string to indicate how the image index of an item in a list view or tree view corresponds to its role or state.</span></span> <span data-ttu-id="97066-105">Например, строка сопоставления может указывать, что индекс изображения представления списка 0 сопоставляется с ролью флажка, а индекс изображения 1 соответствует роли переключателя.</span><span class="sxs-lookup"><span data-stu-id="97066-105">For example, a mapping string may indicate that a list view's image index 0 maps to a role of check box, while image index 1 maps to a role of radio button.</span></span>

<span data-ttu-id="97066-106">Можно также использовать заметку "схема значения" для указания строк, которые сопоставляются с числовыми значениями на ползунке.</span><span class="sxs-lookup"><span data-stu-id="97066-106">You can also use value map annotation to specify strings that map to the numeric values on a slider.</span></span>

## <a name="when-to-use-this-technique"></a><span data-ttu-id="97066-107">Когда следует использовать этот метод</span><span class="sxs-lookup"><span data-stu-id="97066-107">When to Use This Technique</span></span>

<span data-ttu-id="97066-108">Используйте заметку "схема значений" в следующих ситуациях.</span><span class="sxs-lookup"><span data-stu-id="97066-108">Consider using Value Map Annotation in the following situations.</span></span>

-   <span data-ttu-id="97066-109">Когда рисуемое владельцем представление списка или представление в виде дерева включает в себя использование изображений и необходимо предоставить настраиваемое описание (свойство [**описания**](description-property.md) ) на основе этого изображения.</span><span class="sxs-lookup"><span data-stu-id="97066-109">When an owner-drawn list view or tree view incorporates the use of images, and you want to provide a custom accessible description ([**Description**](description-property.md) property) based on that image.</span></span> <span data-ttu-id="97066-110">На следующем рисунке приведен пример.</span><span class="sxs-lookup"><span data-stu-id="97066-110">The following illustration shows an example.</span></span>

    ![Иллюстрация меню "Пуск", где значки предоставляют визуальные подсказки для содержания](images/iconlist.gif)

-   <span data-ttu-id="97066-112">Когда рисуемое владельцем представление списка или элемент управления представлением в виде дерева использует изображения, чтобы элементы дерева или списка действовали как простые элементы управления, обычно флажки или переключатели, и необходимо сопоставлять изображение с ролью.</span><span class="sxs-lookup"><span data-stu-id="97066-112">When an owner-drawn list view or tree view control incorporates the use of images to make the tree or list items act like simple controls, typically checkboxes or radio buttons, and you want to map the image to a role.</span></span> <span data-ttu-id="97066-113">На следующем снимке экрана показан пример.</span><span class="sxs-lookup"><span data-stu-id="97066-113">The following screen shot shows an example.</span></span>

    ![снимок экрана параметров Internet Explorer для установки значения флажков и переключателей](images/customlist.gif)

-   <span data-ttu-id="97066-115">При использовании ползунка для выбора значения, которое может быть определено как отличное от простого целого числа, как показано на следующем снимке экрана, где параметр разрешения экрана описывается строкой.</span><span class="sxs-lookup"><span data-stu-id="97066-115">When a slider is used to select a value that can be described as something other than a simple integer, as in the following screen shot, where the screen resolution setting is described by a string.</span></span>

    ![снимок экрана: ползунок, используемый для установки разрешения экрана](images/slider.gif)

<span data-ttu-id="97066-117">С помощью аннотации карты значений строка сопоставления указывает, как индекс изображения списка или дерева соответствует его роли или состоянию.</span><span class="sxs-lookup"><span data-stu-id="97066-117">With value map annotation, a mapping string indicates how the list's or tree's image index corresponds to its role or state.</span></span> <span data-ttu-id="97066-118">Или может указывать, как числовое значение ползунка соответствует строке.</span><span class="sxs-lookup"><span data-stu-id="97066-118">Or, it can indicate how a slider's numeric value corresponds to a string.</span></span> <span data-ttu-id="97066-119">Например, строка сопоставления может указывать, что индекс изображения представления списка 0 сопоставляется с ролью флажка, а изображение с индексом 1 соответствует роли переключателя.</span><span class="sxs-lookup"><span data-stu-id="97066-119">For example, a mapping string may indicate that a list view's image index 0 maps to a role of check box and image index 1 maps to a role of radio button.</span></span> <span data-ttu-id="97066-120">Используйте [**иаккпропсервицес:: сесвндпропстр ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) , чтобы присоединить строку сопоставления к элементу управления.</span><span class="sxs-lookup"><span data-stu-id="97066-120">Use [**IAccPropServices::SetHwndPropStr()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) to attach the mapping string to the control.</span></span>

<span data-ttu-id="97066-121">Так как для поддержки сопоставления значений требуются знания конкретного элемента управления, существует ограниченное число элементов управления и свойств, которые поддерживают заметку карты значений, включая карты значений ползунков, представления списков и представления в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="97066-121">Because control-specific knowledge is required to support value mapping, there are a limited number of controls and properties that support value map annotation, including slider value maps, list views, and tree views.</span></span>

## <a name="slider-value-map"></a><span data-ttu-id="97066-122">Схема значения ползунка</span><span class="sxs-lookup"><span data-stu-id="97066-122">Slider Value Map</span></span>

<span data-ttu-id="97066-123">**PropID \_ ACC- \_ VALUEMAP** содержит сопоставление из внутренних положений ползунка со строками, доступными для чтения человеком.</span><span class="sxs-lookup"><span data-stu-id="97066-123">**PROPID\_ACC\_VALUEMAP** contains a mapping from internal slider positions to human-readable strings.</span></span> <span data-ttu-id="97066-124">Это свойство поддерживается прокси-сервером Slider Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="97066-124">This property is supported by the Oleacc.dll slider proxy.</span></span> <span data-ttu-id="97066-125">Если текущее значение ползунка находится в карте значений, соответствующая строка будет предоставляться как значение вместо строки процента по умолчанию (например, "50").</span><span class="sxs-lookup"><span data-stu-id="97066-125">If the current slider value is found in the value map, the corresponding string will be exposed as the value instead of the default percentage string (for example, "50").</span></span>

## <a name="list-view-and-tree-view"></a><span data-ttu-id="97066-126">Представление списка и представление в виде дерева</span><span class="sxs-lookup"><span data-stu-id="97066-126">List View and Tree View</span></span>

<span data-ttu-id="97066-127">**PropID \_ ACC \_ ролемап**, **PropID \_ ACC \_ статемап** и **PropID \_ ACC \_ дескриптонмап** предоставляют сопоставления между индексами изображений состояний и значениями ролей и состояний.</span><span class="sxs-lookup"><span data-stu-id="97066-127">**PROPID\_ACC\_ROLEMAP**, **PROPID\_ACC\_STATEMAP**, and **PROPID\_ACC\_DESCRIPTONMAP** provide mappings from state image indexes to role and state values.</span></span> <span data-ttu-id="97066-128">Эти карты позволяют сопоставлять индексы изображений с соответствующими ролями (обычно в [**системе роли \_ \_**](object-roles.md) или [**системой роли System \_ \_ чеккбуттон**](object-roles.md)) и в дополнительных битах состояния (обычно в [**\_ системе \_ состояния**](object-state-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="97066-128">These maps allow those image indexes to be mapped to appropriate roles (usually [**ROLE\_SYSTEM\_RADIOBUTTON**](object-roles.md) or [**ROLE\_SYSTEM\_CHECKBUTTON**](object-roles.md)) and additional state bits (usually [**STATE\_SYSTEM\_CHECKED**](object-state-constants.md)).</span></span>

<span data-ttu-id="97066-129">Дополнительные сведения об аннотировании карт значений см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="97066-129">For more information about value map annotation, see the following topics:</span></span>

-   [<span data-ttu-id="97066-130">Использование заметки с картой значений</span><span class="sxs-lookup"><span data-stu-id="97066-130">Using Value Map Annotation</span></span>](using-value-map-annotation.md)
-   [<span data-ttu-id="97066-131">Пример заметки к карте значений</span><span class="sxs-lookup"><span data-stu-id="97066-131">Value Map Annotation Sample</span></span>](value-map-annotation-sample.md)

## <a name="annotation-map-format"></a><span data-ttu-id="97066-132">Формат отображения заметки</span><span class="sxs-lookup"><span data-stu-id="97066-132">Annotation Map Format</span></span>

<span data-ttu-id="97066-133">В следующей таблице описаны поля, которые включены в карту заметок.</span><span class="sxs-lookup"><span data-stu-id="97066-133">The following table describes the fields that are included in an annotation map.</span></span>



| <span data-ttu-id="97066-134">Поле</span><span class="sxs-lookup"><span data-stu-id="97066-134">Field</span></span>               | <span data-ttu-id="97066-135">Описание</span><span class="sxs-lookup"><span data-stu-id="97066-135">Description</span></span>                                                                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97066-136">Конкретного</span><span class="sxs-lookup"><span data-stu-id="97066-136">'A'</span></span>                 | <span data-ttu-id="97066-137">Указывает, что используется определенная схема кодирования.</span><span class="sxs-lookup"><span data-stu-id="97066-137">Indicates that a particular coding scheme is used.</span></span> <span data-ttu-id="97066-138">Для будущих схем кодирования могут поддерживаться дополнительные префиксы.</span><span class="sxs-lookup"><span data-stu-id="97066-138">Additional prefixes may be supported for future encoding schemes.</span></span>                                                                                                                                                          |
| <span data-ttu-id="97066-139">Символ разделителя</span><span class="sxs-lookup"><span data-stu-id="97066-139">Delimiter character</span></span> | <span data-ttu-id="97066-140">Обычно это двоеточие (:) используется, но может быть другим символом, кроме **null** или пустого пространства.</span><span class="sxs-lookup"><span data-stu-id="97066-140">Usually a colon (:) is used, but can be another character except for **NULL** or an empty space.</span></span> <span data-ttu-id="97066-141">Поскольку этот символ будет использоваться в качестве разделителя для остальных полей, он не может использоваться как часть значения на карте.</span><span class="sxs-lookup"><span data-stu-id="97066-141">Because this character will be used as a delimiter for the remaining fields, it may not be used as part of a value in the map.</span></span>                                               |
| <span data-ttu-id="97066-142">0, 1 или 2</span><span class="sxs-lookup"><span data-stu-id="97066-142">0, 1, or 2</span></span>          | <span data-ttu-id="97066-143">Значение, указывающее, какой ключ используется.</span><span class="sxs-lookup"><span data-stu-id="97066-143">A value that indicates which key is being used.</span></span> <span data-ttu-id="97066-144">Для представлений в виде дерева и представления списка и сопоставлений состояний этот ключ может иметь значение 0 (индекс изображения), 1 (индекс изображения состояния) или 2 (индекс изображения оверлея).</span><span class="sxs-lookup"><span data-stu-id="97066-144">For Tree View and List View role and state maps, this key can be 0 (image index), 1 (state image index), or 2 (overlay image index).</span></span> <span data-ttu-id="97066-145">Для ползунков и других элементов управления, не предлагающих выбора ключей, это значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="97066-145">For sliders and other controls that do not offer a choice of keys, this value must be 0.</span></span> |
| <span data-ttu-id="97066-146">Символ разделителя</span><span class="sxs-lookup"><span data-stu-id="97066-146">Delimiter character</span></span> | <span data-ttu-id="97066-147">:</span><span class="sxs-lookup"><span data-stu-id="97066-147">:</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="97066-148">Пары "ключ — значение"</span><span class="sxs-lookup"><span data-stu-id="97066-148">Key value pairs</span></span>     | <span data-ttu-id="97066-149">Каждая пара состоит из строки ключа и символа-разделителя.</span><span class="sxs-lookup"><span data-stu-id="97066-149">Each pair consists of a key string and a delimiter character.</span></span> <span data-ttu-id="97066-150">Строка ключа является числом и может быть в десятичном или шестнадцатеричном формате (с начальным префиксом "0x").</span><span class="sxs-lookup"><span data-stu-id="97066-150">The key string is a number and may be in decimal or hexadecimal (with a leading "0x" prefix) format.</span></span>                                                                                                            |
| <span data-ttu-id="97066-151">Строка значения</span><span class="sxs-lookup"><span data-stu-id="97066-151">Value string</span></span>        | <span data-ttu-id="97066-152">Для карт значений это строка.</span><span class="sxs-lookup"><span data-stu-id="97066-152">For value maps, this is a string.</span></span> <span data-ttu-id="97066-153">Для сопоставлений ролей и состояний это число (десятичное или шестнадцатеричное).</span><span class="sxs-lookup"><span data-stu-id="97066-153">For role and state maps, this is a number (decimal or hexadecimal).</span></span>                                                                                                                                                                         |
| <span data-ttu-id="97066-154">Символ разделителя</span><span class="sxs-lookup"><span data-stu-id="97066-154">Delimiter character</span></span> | <span data-ttu-id="97066-155">:</span><span class="sxs-lookup"><span data-stu-id="97066-155">:</span></span>                                                                                                                                                                                                                                                                             |



 

<span data-ttu-id="97066-156">Например, схема может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="97066-156">For example, a map may look like the following:</span></span>


```C++
A:0:0:Cold:1:Warm:3:Hot:
```



<span data-ttu-id="97066-157">Когда эта схема значений применяется к элементу управления "ползунок", значение "тепло" будет предоставляться, когда ползунок находится в позиции 1.</span><span class="sxs-lookup"><span data-stu-id="97066-157">When this value map is applied to a slider control, a value of "Warm" will be exposed when the slider is at position 1.</span></span> <span data-ttu-id="97066-158">Так как значение 2 не включено в этот пример, будет предоставлено значение по умолчанию для этой должности.</span><span class="sxs-lookup"><span data-stu-id="97066-158">Because value 2 is not included in this example, the default value for that position will be exposed.</span></span> <span data-ttu-id="97066-159">Для ползунка значение по умолчанию равно процентному значению, например 33.</span><span class="sxs-lookup"><span data-stu-id="97066-159">For a slider, the default would be a percentage value, such as 33.</span></span>

 

 




