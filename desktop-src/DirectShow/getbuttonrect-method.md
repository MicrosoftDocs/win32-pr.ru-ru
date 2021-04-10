---
description: Метод Жетбуттонрект извлекает прямоугольник для указанной кнопки в координатах окна.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Метод Жетбуттонрект
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139342"
---
# <a name="getbuttonrect-method"></a><span data-ttu-id="616a4-103">Метод Жетбуттонрект</span><span class="sxs-lookup"><span data-stu-id="616a4-103">GetButtonRect Method</span></span>

> [!Note]  
> <span data-ttu-id="616a4-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="616a4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="616a4-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="616a4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="616a4-106">`GetButtonRect`Метод получает прямоугольник для указанной кнопки в координатах окна.</span><span class="sxs-lookup"><span data-stu-id="616a4-106">The `GetButtonRect` method retrieves the rectangle for the specified button, in window coordinates.</span></span>

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a><span data-ttu-id="616a4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="616a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="616a4-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*ибуттон*</span><span class="sxs-lookup"><span data-stu-id="616a4-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="616a4-109">Указывает номер кнопки в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="616a4-109">Specifies the button number as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="616a4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="616a4-110">Return Value</span></span>

<span data-ttu-id="616a4-111">Возвращает объект [двдрект](dvdrect-object.md) , определяющий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="616a4-111">Returns a [DVDRect](dvdrect-object.md) object that defines the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="616a4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="616a4-112">Remarks</span></span>

<span data-ttu-id="616a4-113">Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.</span><span class="sxs-lookup"><span data-stu-id="616a4-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="616a4-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="616a4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616a4-115">**буттонсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="616a4-115">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="616a4-116">**куррентбуттон**</span><span class="sxs-lookup"><span data-stu-id="616a4-116">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="616a4-117">**активатебуттон**</span><span class="sxs-lookup"><span data-stu-id="616a4-117">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="616a4-118">**селектандактиватебуттон**</span><span class="sxs-lookup"><span data-stu-id="616a4-118">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="616a4-119">**селектатпоситион**</span><span class="sxs-lookup"><span data-stu-id="616a4-119">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



