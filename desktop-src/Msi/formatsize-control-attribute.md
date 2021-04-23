---
description: Если этот бит задан для статического текстового элемента управления, элемент управления автоматически пытается отформатировать отображаемый текст как число, представляющее число байтов.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Атрибут элемента управления Форматсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263600"
---
# <a name="formatsize-control-attribute"></a><span data-ttu-id="f5780-103">Атрибут элемента управления Форматсизе</span><span class="sxs-lookup"><span data-stu-id="f5780-103">FormatSize Control Attribute</span></span>

<span data-ttu-id="f5780-104">Если этот бит задан для статического текстового элемента управления, элемент управления автоматически пытается отформатировать отображаемый текст как число, представляющее число байтов.</span><span class="sxs-lookup"><span data-stu-id="f5780-104">If this bit is set for a static text control, the control automatically attempts to format the displayed text as a number that represents a count of bytes.</span></span> <span data-ttu-id="f5780-105">Для правильного форматирования текст элемента управления должен быть задан строкой, представляющей число, выраженное в единицах (512 байт).</span><span class="sxs-lookup"><span data-stu-id="f5780-105">For proper formatting, the control's text must be set to a string that represents a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="f5780-106">Отображаемое значение затем форматируется в килобайтах (КБ), мегабайтах (МБ) или гигабайтах (ГБ) и отображается с соответствующей строкой, представляющей единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="f5780-106">The displayed value is then formatted in kilobytes (KB), megabytes (MB), or gigabytes (GB), and displayed with the appropriate string that represents the units.</span></span> <span data-ttu-id="f5780-107">Дополнительные сведения см. в разделе [элемент управления текстом](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="f5780-107">For more information, see [Text Control](text-control.md).</span></span>



| <span data-ttu-id="f5780-108">Числовое значение исходного текста</span><span class="sxs-lookup"><span data-stu-id="f5780-108">Numerical value of original text</span></span> | <span data-ttu-id="f5780-109">Используемая строка единицы</span><span class="sxs-lookup"><span data-stu-id="f5780-109">Unit string used</span></span> |
|----------------------------------|------------------|
| <span data-ttu-id="f5780-110">Менее 20480</span><span class="sxs-lookup"><span data-stu-id="f5780-110">Less than 20480</span></span>                  | <span data-ttu-id="f5780-111">КБ</span><span class="sxs-lookup"><span data-stu-id="f5780-111">KB</span></span>               |
| <span data-ttu-id="f5780-112">Менее 20971520</span><span class="sxs-lookup"><span data-stu-id="f5780-112">Less than 20971520</span></span>               | <span data-ttu-id="f5780-113">МБ</span><span class="sxs-lookup"><span data-stu-id="f5780-113">MB</span></span>               |
| <span data-ttu-id="f5780-114">Менее 10737418240</span><span class="sxs-lookup"><span data-stu-id="f5780-114">Less than 10737418240</span></span>            | <span data-ttu-id="f5780-115">ГБ</span><span class="sxs-lookup"><span data-stu-id="f5780-115">GB</span></span>               |



 

## <a name="valid-controls"></a><span data-ttu-id="f5780-116">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="f5780-116">Valid Controls</span></span>



| <span data-ttu-id="f5780-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="f5780-117">Decimal</span></span> | <span data-ttu-id="f5780-118">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="f5780-118">Hexadecimal</span></span> | <span data-ttu-id="f5780-119">Control</span><span class="sxs-lookup"><span data-stu-id="f5780-119">Control</span></span>                          |
|---------|-------------|----------------------------------|
| <span data-ttu-id="f5780-120">524288</span><span class="sxs-lookup"><span data-stu-id="f5780-120">524288</span></span>  | <span data-ttu-id="f5780-121">0x00080000</span><span class="sxs-lookup"><span data-stu-id="f5780-121">0x00080000</span></span>  | <span data-ttu-id="f5780-122">мсидбконтролаттрибутесформатсизе</span><span class="sxs-lookup"><span data-stu-id="f5780-122">msidbControlAttributesFormatSize</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f5780-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5780-123">Remarks</span></span>

<span data-ttu-id="f5780-124">Чтобы задать этот атрибут для элемента управления, включите биты Форматсизе в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="f5780-124">To set this attribute on a control, include the FormatSize bits in the Attributes column of the control's record in the [Control Table](control-table.md).</span></span> <span data-ttu-id="f5780-125">Текст элемента управления должен быть задан строкой, представляющей число, выраженное в единицах (512 байт).</span><span class="sxs-lookup"><span data-stu-id="f5780-125">The control's text must be set to a string representing a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="f5780-126">Текст строк единиц измерения определяется в [таблице уитекст](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="f5780-126">The text of the unit strings are defined in the [UIText Table](uitext-table.md).</span></span> <span data-ttu-id="f5780-127">Расположение строки единицы управляется свойством [**лефтунит**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="f5780-127">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="f5780-128">Если свойство **лефтунит** определено как какое-либо значение, строка единицы появляется перед числовым значением.</span><span class="sxs-lookup"><span data-stu-id="f5780-128">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span> <span data-ttu-id="f5780-129">Если в тексте, связанном с элементом управления, отображается что-либо, Кроме числовых символов, отображаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="f5780-129">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="f5780-130">Во время выполнения установщик разрешает свойство [**примариволумеспацерекуиред**](primaryvolumespacerequired.md) к общему количеству байтов, необходимых для установки в единицах 512.</span><span class="sxs-lookup"><span data-stu-id="f5780-130">At run time, the installer resolves the [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) Property to the total number of bytes required for the installation in units of 512.</span></span> <span data-ttu-id="f5780-131">Статический элемент управления Text с Форматсизе bit можно использовать для автоматического форматирования и метки общего числа байтов, необходимых для установки, в КБ, МБ или ГБ.</span><span class="sxs-lookup"><span data-stu-id="f5780-131">A static text control with FormatSize bit can be used to automatically format and label the total number of bytes required for the installation in KB, MB, or GB as appropriate.</span></span> <span data-ttu-id="f5780-132">Для целей этого примера предположим, что общее число байтов равно 18 336 768.</span><span class="sxs-lookup"><span data-stu-id="f5780-132">For the purposes of this example, assume the total number of bytes is 18,336,768.</span></span> <span data-ttu-id="f5780-133">Установщик задает для свойства Примариволумеспацерекуиред значение 18 336 768, деленное на 512 или 35 814.</span><span class="sxs-lookup"><span data-stu-id="f5780-133">The installer sets the value of the PrimaryVolumeSpaceRequired property to 18,336,768 divided by 512, or 35,814.</span></span> <span data-ttu-id="f5780-134">Число, отображаемое элементом управления "текст" с помощью Форматсизе, было бы 17MB.</span><span class="sxs-lookup"><span data-stu-id="f5780-134">The number displayed by the text control with FormatSize would be 17MB.</span></span>

<span data-ttu-id="f5780-135">Числовые значения исходного текста задаются в единицах измерения 512.</span><span class="sxs-lookup"><span data-stu-id="f5780-135">The numerical values of the original text are given in units of 512.</span></span> <span data-ttu-id="f5780-136">В приведенной выше таблице строка 20 480 соответствует строке KB, так как 20 480 раз 512, результатом является 10 485 760 байт или 10 240 КБ.</span><span class="sxs-lookup"><span data-stu-id="f5780-136">In the table above, the string 20,480 corresponds to the KB string because 20,480 times 512 yields a result of 10,485,760 bytes or 10,240 KB.</span></span>

<span data-ttu-id="f5780-137">Строки единиц измерения, перечисленные в предыдущей таблице, ссылаются на ключи в [таблице уитекст](uitext-table.md), где определен текст строки единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="f5780-137">The unit strings listed in the previous table refer to keys in the [UIText Table](uitext-table.md), where the text of the unit string is defined.</span></span>

<span data-ttu-id="f5780-138">Расположение строки единицы управляется свойством [**лефтунит**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="f5780-138">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="f5780-139">Если свойство **лефтунит** определено как какое-либо значение, строка единицы появляется перед числовым значением.</span><span class="sxs-lookup"><span data-stu-id="f5780-139">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span>

<span data-ttu-id="f5780-140">Если в тексте, связанном с элементом управления, отображается что-либо, Кроме числовых символов, отображаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="f5780-140">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="f5780-141">Дополнительные сведения см. в разделе [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="f5780-141">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



