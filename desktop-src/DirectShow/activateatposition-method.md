---
description: Метод Активатеатпоситион активирует кнопку меню в указанной позиции.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Метод Активатеатпоситион
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140538"
---
# <a name="activateatposition-method"></a><span data-ttu-id="814a7-103">Метод Активатеатпоситион</span><span class="sxs-lookup"><span data-stu-id="814a7-103">ActivateAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="814a7-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="814a7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="814a7-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="814a7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="814a7-106">Метод Активатеатпоситион активирует кнопку меню в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="814a7-106">The ActivateAtPosition method activates the menu button at the specified position.</span></span>

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="814a7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="814a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="814a7-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*кспос*</span><span class="sxs-lookup"><span data-stu-id="814a7-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="814a7-109">Задает координату x в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="814a7-109">Specifies x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="814a7-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*ипос*</span><span class="sxs-lookup"><span data-stu-id="814a7-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="814a7-111">Задает координату y в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="814a7-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="814a7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="814a7-112">Return Value</span></span>

<span data-ttu-id="814a7-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="814a7-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="814a7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="814a7-114">Remarks</span></span>

<span data-ttu-id="814a7-115">Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.</span><span class="sxs-lookup"><span data-stu-id="814a7-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="814a7-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="814a7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="814a7-117">**буттонсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="814a7-117">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="814a7-118">**куррентбуттон**</span><span class="sxs-lookup"><span data-stu-id="814a7-118">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="814a7-119">**жетбуттонатпоситион**</span><span class="sxs-lookup"><span data-stu-id="814a7-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="814a7-120">**жетбуттонрект**</span><span class="sxs-lookup"><span data-stu-id="814a7-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="814a7-121">**селектандактиватебуттон**</span><span class="sxs-lookup"><span data-stu-id="814a7-121">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="814a7-122">**селектатпоситион**</span><span class="sxs-lookup"><span data-stu-id="814a7-122">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



