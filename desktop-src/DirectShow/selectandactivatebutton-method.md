---
description: Метод Селектандактиватебуттон выбирает и активирует указанную кнопку.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Метод Селектандактиватебуттон
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682208"
---
# <a name="selectandactivatebutton-method"></a><span data-ttu-id="41c4b-103">Метод Селектандактиватебуттон</span><span class="sxs-lookup"><span data-stu-id="41c4b-103">SelectAndActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="41c4b-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="41c4b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="41c4b-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="41c4b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="41c4b-106">`SelectAndActivateButton`Метод выбирает и активирует указанную кнопку.</span><span class="sxs-lookup"><span data-stu-id="41c4b-106">The `SelectAndActivateButton` method selects and activates the specified button.</span></span>

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a><span data-ttu-id="41c4b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="41c4b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41c4b-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*ибуттон*</span><span class="sxs-lookup"><span data-stu-id="41c4b-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="41c4b-109">Задает кнопку в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="41c4b-109">Specifies the button as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41c4b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41c4b-110">Return Value</span></span>

<span data-ttu-id="41c4b-111">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="41c4b-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41c4b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41c4b-112">Remarks</span></span>

<span data-ttu-id="41c4b-113">Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.</span><span class="sxs-lookup"><span data-stu-id="41c4b-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="41c4b-114">Этот метод выделяет указанную кнопку и активирует ее автоматически.</span><span class="sxs-lookup"><span data-stu-id="41c4b-114">This method highlights the specified button and activate it automatically.</span></span>

## <a name="see-also"></a><span data-ttu-id="41c4b-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41c4b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c4b-116">**буттонсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="41c4b-116">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="41c4b-117">**куррентбуттон**</span><span class="sxs-lookup"><span data-stu-id="41c4b-117">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="41c4b-118">**активатебуттон**</span><span class="sxs-lookup"><span data-stu-id="41c4b-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="41c4b-119">**жетбуттонатпоситион**</span><span class="sxs-lookup"><span data-stu-id="41c4b-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="41c4b-120">**жетбуттонрект**</span><span class="sxs-lookup"><span data-stu-id="41c4b-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="41c4b-121">**селектатпоситион**</span><span class="sxs-lookup"><span data-stu-id="41c4b-121">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



