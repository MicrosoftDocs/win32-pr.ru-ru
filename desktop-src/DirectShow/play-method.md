---
description: Метод Play воспроизводит текущее название DVD-диска.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Метод Play (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537124"
---
# <a name="play-method-directshow"></a><span data-ttu-id="d7cd8-103">Метод Play (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="d7cd8-103">Play Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="d7cd8-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d7cd8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d7cd8-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="d7cd8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d7cd8-106">`Play`Метод воспроизводит текущее название DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="d7cd8-106">The `Play` method plays the current DVD title.</span></span>

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a><span data-ttu-id="d7cd8-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7cd8-107">Return Value</span></span>

<span data-ttu-id="d7cd8-108">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d7cd8-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7cd8-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7cd8-109">Remarks</span></span>

<span data-ttu-id="d7cd8-110">Если воспроизведение приостановлено или остановлено, а [**енаблересетонстоп**](enableresetonstop-property.md) имеет значение true, вызов **Play** продолжит воспроизведение с обычной скоростью в текущем расположении.</span><span class="sxs-lookup"><span data-stu-id="d7cd8-110">If playback is paused or stopped and [**EnableResetOnStop**](enableresetonstop-property.md) is true, then calling **Play** will resume playback at normal speed at the current location.</span></span> <span data-ttu-id="d7cd8-111">Если воспроизведение остановлено и **енаблересетонстоп** имеет значение false, вызов **Play** приведет к тому, что диск начнет играть в начале первого заголовка.</span><span class="sxs-lookup"><span data-stu-id="d7cd8-111">If playback is stopped and **EnableResetOnStop** is false, then calling **Play** will cause the disc to start playing at the beginning of the first title.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7cd8-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7cd8-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7cd8-113">**Возобновить**</span><span class="sxs-lookup"><span data-stu-id="d7cd8-113">**Resume**</span></span>](resume-method.md)
</dt> </dl>

 

 



