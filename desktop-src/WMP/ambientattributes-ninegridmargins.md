---
title: Амбиентаттрибутес. Нинегридмаргинс
description: Атрибут Нинегридмаргинс задает ширину полей для неравномерного масштабирования элемента обложки.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Нинегридмаргинс
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694767"
---
# <a name="ambientattributesninegridmargins"></a><span data-ttu-id="6bffd-104">Амбиентаттрибутес. Нинегридмаргинс</span><span class="sxs-lookup"><span data-stu-id="6bffd-104">AmbientAttributes.nineGridMargins</span></span>

<span data-ttu-id="6bffd-105">Атрибут **нинегридмаргинс** задает ширину полей для неравномерного масштабирования элемента обложки.</span><span class="sxs-lookup"><span data-stu-id="6bffd-105">The **nineGridMargins** attribute specifies margin widths for non-uniform scaling of the skin element.</span></span>

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a><span data-ttu-id="6bffd-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="6bffd-106">Possible Values</span></span>

<span data-ttu-id="6bffd-107">Этот атрибут является **строкой** для чтения и записи, которая содержит ширину полей в форме "*видслефт*,*видстоп*,*видсригхт*,*видсботтом*".</span><span class="sxs-lookup"><span data-stu-id="6bffd-107">This attribute is a read/write **String** that contains the widths of the margins in the form "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*".</span></span> <span data-ttu-id="6bffd-108">Каждое значение ширины — это число, представляющее ширину (в пикселях) поля для девяти сеток.</span><span class="sxs-lookup"><span data-stu-id="6bffd-108">Each width value is a number representing the width, in pixels, of a margin for the nine grid.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bffd-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bffd-109">Remarks</span></span>

<span data-ttu-id="6bffd-110">*Девять сеток* — это прием, используемый для разделения элементов пользовательского интерфейса на девять прямоугольных областей, расположенных в матрице размером 3 на 3.</span><span class="sxs-lookup"><span data-stu-id="6bffd-110">A *nine grid* is a technique used to divide user interface elements into nine rectangular regions arranged in a 3 by 3 matrix.</span></span> <span data-ttu-id="6bffd-111">При изменении размера элемента девять областей сетки могут масштабироваться различными факторами.</span><span class="sxs-lookup"><span data-stu-id="6bffd-111">When an element is resized, the nine grid regions can each scale by a different factor.</span></span>

<span data-ttu-id="6bffd-112">Каждое из четырех указанных значений ширины представляет ширину строки или столбца трех смежных областей.</span><span class="sxs-lookup"><span data-stu-id="6bffd-112">Each of the four width values you specify represents the width of a row or column of three adjacent regions.</span></span> <span data-ttu-id="6bffd-113">Каждая строка или столбец образует левую сторону, верхнюю, правую или нижнюю часть девять сеток.</span><span class="sxs-lookup"><span data-stu-id="6bffd-113">Each row or column forms the left side, top, right side, or bottom of the nine grid.</span></span>

<span data-ttu-id="6bffd-114">[Амбиентаттрибутес. ресизеимажес](ambientattributes-resizeimages.md) должно иметь значение true, чтобы этот атрибут работал.</span><span class="sxs-lookup"><span data-stu-id="6bffd-114">[AmbientAttributes.resizeImages](ambientattributes-resizeimages.md) must be set to true for this attribute to work.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bffd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6bffd-115">Requirements</span></span>



| <span data-ttu-id="6bffd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6bffd-116">Requirement</span></span> | <span data-ttu-id="6bffd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6bffd-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="6bffd-118">Версия</span><span class="sxs-lookup"><span data-stu-id="6bffd-118">Version</span></span><br/> | <span data-ttu-id="6bffd-119">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="6bffd-119">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6bffd-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bffd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bffd-121">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="6bffd-121">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





