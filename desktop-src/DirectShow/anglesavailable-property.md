---
description: Свойство Англесаваилабле извлекает количество доступных в данный момент углов.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Англесаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655595"
---
# <a name="anglesavailable-property"></a><span data-ttu-id="00310-103">Англесаваилабле, свойство</span><span class="sxs-lookup"><span data-stu-id="00310-103">AnglesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="00310-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="00310-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="00310-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="00310-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="00310-106">`AnglesAvailable`Свойство получает количество доступных в данный момент углов.</span><span class="sxs-lookup"><span data-stu-id="00310-106">The `AnglesAvailable` property retrieves the number of angles currently available.</span></span>

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a><span data-ttu-id="00310-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00310-107">Return Value</span></span>

<span data-ttu-id="00310-108">Возвращает целочисленное значение от 1 до 9, представляющее число доступных в данный момент углов.</span><span class="sxs-lookup"><span data-stu-id="00310-108">Returns an integer value from 1 through 9 representing the number of angles currently available.</span></span> <span data-ttu-id="00310-109">If</span><span class="sxs-lookup"><span data-stu-id="00310-109">If</span></span>


```
iAngles
```



<span data-ttu-id="00310-110">= 1, в текущем расположении отсутствует блок Angle.</span><span class="sxs-lookup"><span data-stu-id="00310-110">= 1, there is no angle block at the current location.</span></span>

## <a name="remarks"></a><span data-ttu-id="00310-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00310-111">Remarks</span></span>

<span data-ttu-id="00310-112">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="00310-112">This property is read-only with no default value.</span></span> <span data-ttu-id="00310-113">*Блок угла* — это сегмент видео, который был снимком более чем одного угла камеры.</span><span class="sxs-lookup"><span data-stu-id="00310-113">An *angle block* is a video segment that was shot from more than one camera angle.</span></span> <span data-ttu-id="00310-114">В блоке углов может содержаться до девяти углов, пронумерованных от 1 до 9.</span><span class="sxs-lookup"><span data-stu-id="00310-114">There can be up to nine angles in an angle block, numbered from 1 through 9.</span></span> <span data-ttu-id="00310-115">Когда Навигатор DVD впервые входит в блок угла, он отправляет приложению уведомление о том, \_ что \_ \_ число углов в *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="00310-115">When the DVD Navigator first enters an angle block, it sends your application an EC\_DVD\_ANGLES\_AVAILABLE event notification with the number of angles in *lParam1*.</span></span> <span data-ttu-id="00310-116">Можно создать диск, чтобы автоматически отображать меню для доступных углов при входе в блок угла, но обычно приложение должно определить число доступных углов и предложить пользователю выбрать один из них.</span><span class="sxs-lookup"><span data-stu-id="00310-116">A disc can be authored to automatically show a menu for available angles when it enters an angle block, but generally an application must determine the number of angles available and offer the user a way to select one.</span></span>

## <a name="see-also"></a><span data-ttu-id="00310-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00310-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00310-118">**куррентангле**</span><span class="sxs-lookup"><span data-stu-id="00310-118">**CurrentAngle**</span></span>](currentangle-property.md)
</dt> </dl>

 

 



