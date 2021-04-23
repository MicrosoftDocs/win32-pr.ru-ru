---
description: Метод Селектатпоситион выбирает кнопку меню с заданными координатами указателя мыши.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Метод Селектатпоситион
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805837"
---
# <a name="selectatposition-method"></a><span data-ttu-id="eb44b-103">Метод Селектатпоситион</span><span class="sxs-lookup"><span data-stu-id="eb44b-103">SelectAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="eb44b-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="eb44b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="eb44b-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="eb44b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="eb44b-106">`SelectAtPosition`Метод выбирает кнопку меню с заданными координатами указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="eb44b-106">The `SelectAtPosition` method selects the menu button at the specified mouse pointer coordinates.</span></span>

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="eb44b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb44b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb44b-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*кспос*</span><span class="sxs-lookup"><span data-stu-id="eb44b-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="eb44b-109">Задает координату x в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="eb44b-109">Specifies the x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="eb44b-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*ипос*</span><span class="sxs-lookup"><span data-stu-id="eb44b-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="eb44b-111">Задает координату y в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="eb44b-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb44b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb44b-112">Return Value</span></span>

<span data-ttu-id="eb44b-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="eb44b-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb44b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb44b-114">Remarks</span></span>

<span data-ttu-id="eb44b-115">Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.</span><span class="sxs-lookup"><span data-stu-id="eb44b-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="eb44b-116">При выборе команды просто выделяется кнопка.</span><span class="sxs-lookup"><span data-stu-id="eb44b-116">Selecting merely highlights the button.</span></span> <span data-ttu-id="eb44b-117">Чтобы отправить команду, связанную с выбранной кнопкой, вызовите [**активатебуттон**](activatebutton-method.md).</span><span class="sxs-lookup"><span data-stu-id="eb44b-117">To send the command associated with a button that has been selected, call [**ActivateButton**](activatebutton-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="eb44b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb44b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb44b-119">**буттонсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="eb44b-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="eb44b-120">**куррентбуттон**</span><span class="sxs-lookup"><span data-stu-id="eb44b-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="eb44b-121">**жетбуттонатпоситион**</span><span class="sxs-lookup"><span data-stu-id="eb44b-121">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="eb44b-122">**жетбуттонрект**</span><span class="sxs-lookup"><span data-stu-id="eb44b-122">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="eb44b-123">**селектандактиватебуттон**</span><span class="sxs-lookup"><span data-stu-id="eb44b-123">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> </dl>

 

 



