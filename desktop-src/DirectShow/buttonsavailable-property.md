---
description: Свойство Буттонсаваилабле извлекает общее число кнопок в текущем меню.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Буттонсаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423018"
---
# <a name="buttonsavailable-property"></a><span data-ttu-id="74295-103">Буттонсаваилабле, свойство</span><span class="sxs-lookup"><span data-stu-id="74295-103">ButtonsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="74295-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="74295-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="74295-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="74295-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="74295-106">`ButtonsAvailable`Свойство получает общее количество кнопок в текущем меню.</span><span class="sxs-lookup"><span data-stu-id="74295-106">The `ButtonsAvailable` property retrieves the total number of buttons on the current menu.</span></span>

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a><span data-ttu-id="74295-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74295-107">Return Value</span></span>

<span data-ttu-id="74295-108">Возвращает целочисленное значение, представляющее количество кнопок.</span><span class="sxs-lookup"><span data-stu-id="74295-108">Returns an integer value representing the number of buttons.</span></span>

## <a name="remarks"></a><span data-ttu-id="74295-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74295-109">Remarks</span></span>

<span data-ttu-id="74295-110">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="74295-110">This property is read-only with no default value.</span></span> <span data-ttu-id="74295-111">Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.</span><span class="sxs-lookup"><span data-stu-id="74295-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="74295-112">Вызовите этот метод, чтобы получить верхний предел диапазона допустимых номеров кнопок.</span><span class="sxs-lookup"><span data-stu-id="74295-112">Call this method to retrieve the upper limit for the range of valid button numbers.</span></span>

## <a name="see-also"></a><span data-ttu-id="74295-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74295-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74295-114">**куррентбуттон**</span><span class="sxs-lookup"><span data-stu-id="74295-114">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="74295-115">**жетбуттонатпоситион**</span><span class="sxs-lookup"><span data-stu-id="74295-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="74295-116">**жетбуттонрект**</span><span class="sxs-lookup"><span data-stu-id="74295-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="74295-117">**селектандактиватебуттон**</span><span class="sxs-lookup"><span data-stu-id="74295-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="74295-118">**селектатпоситион**</span><span class="sxs-lookup"><span data-stu-id="74295-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



