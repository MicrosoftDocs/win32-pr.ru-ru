---
description: Метод Жетбуттонатпоситион извлекает номер кнопки по заданным координатам без выбора или активации.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Метод Жетбуттонатпоситион
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139343"
---
# <a name="getbuttonatposition-method"></a><span data-ttu-id="6d90f-103">Метод Жетбуттонатпоситион</span><span class="sxs-lookup"><span data-stu-id="6d90f-103">GetButtonAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="6d90f-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6d90f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6d90f-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="6d90f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6d90f-106">`GetButtonAtPosition`Метод получает номер кнопки по заданным координатам без выбора или активации.</span><span class="sxs-lookup"><span data-stu-id="6d90f-106">The `GetButtonAtPosition` method retrieves the number of the button at the specified coordinates without selecting or activating it.</span></span>

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="6d90f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d90f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d90f-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*кспос*</span><span class="sxs-lookup"><span data-stu-id="6d90f-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="6d90f-109">Задает координату по оси x для указателя мыши в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="6d90f-109">Specifies the x-coordinate of the mouse pointer as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="6d90f-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*ипос*</span><span class="sxs-lookup"><span data-stu-id="6d90f-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="6d90f-111">Задает координату y указателя мыши в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="6d90f-111">Specifies the y-coordinate of the mouse pointer as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d90f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d90f-112">Return Value</span></span>

<span data-ttu-id="6d90f-113">Возвращает целочисленное значение, задающее кнопку, если она имеется, в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="6d90f-113">Returns an integer value specifying the button, if any, at the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d90f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d90f-114">Remarks</span></span>

<span data-ttu-id="6d90f-115">Этот метод возвращает нуль, если в заданных координатах отсутствует кнопка.</span><span class="sxs-lookup"><span data-stu-id="6d90f-115">This method returns zero if no button is present at the given coordinates.</span></span> <span data-ttu-id="6d90f-116">Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.</span><span class="sxs-lookup"><span data-stu-id="6d90f-116">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d90f-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d90f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d90f-118">**активатебуттон**</span><span class="sxs-lookup"><span data-stu-id="6d90f-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="6d90f-119">**буттонсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="6d90f-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="6d90f-120">**куррентбуттон**</span><span class="sxs-lookup"><span data-stu-id="6d90f-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="6d90f-121">**жетбуттонрект**</span><span class="sxs-lookup"><span data-stu-id="6d90f-121">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="6d90f-122">**селектандактиватебуттон**</span><span class="sxs-lookup"><span data-stu-id="6d90f-122">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="6d90f-123">**селектатпоситион**</span><span class="sxs-lookup"><span data-stu-id="6d90f-123">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



