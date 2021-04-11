---
description: Свойство Куррентбуттон извлекает номер выбранной кнопки меню.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Куррентбуттон, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341862"
---
# <a name="currentbutton-property"></a><span data-ttu-id="5ad79-103">Куррентбуттон, свойство</span><span class="sxs-lookup"><span data-stu-id="5ad79-103">CurrentButton Property</span></span>

> [!Note]  
> <span data-ttu-id="5ad79-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5ad79-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5ad79-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="5ad79-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5ad79-106">`CurrentButton`Свойство получает номер выбранной кнопки меню.</span><span class="sxs-lookup"><span data-stu-id="5ad79-106">The `CurrentButton` property retrieves the number of the selected menu button.</span></span>

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a><span data-ttu-id="5ad79-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ad79-107">Return Value</span></span>

<span data-ttu-id="5ad79-108">Возвращает целочисленное значение, представляющее кнопку.</span><span class="sxs-lookup"><span data-stu-id="5ad79-108">Returns an integer value representing the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ad79-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ad79-109">Remarks</span></span>

<span data-ttu-id="5ad79-110">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5ad79-110">This property is read-only with no default value.</span></span> <span data-ttu-id="5ad79-111">Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.</span><span class="sxs-lookup"><span data-stu-id="5ad79-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ad79-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ad79-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad79-113">**активатебуттон**</span><span class="sxs-lookup"><span data-stu-id="5ad79-113">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="5ad79-114">**буттонсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="5ad79-114">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="5ad79-115">**жетбуттонатпоситион**</span><span class="sxs-lookup"><span data-stu-id="5ad79-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="5ad79-116">**жетбуттонрект**</span><span class="sxs-lookup"><span data-stu-id="5ad79-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="5ad79-117">**селектандактиватебуттон**</span><span class="sxs-lookup"><span data-stu-id="5ad79-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="5ad79-118">**селектатпоситион**</span><span class="sxs-lookup"><span data-stu-id="5ad79-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



