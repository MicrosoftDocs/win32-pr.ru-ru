---
description: Метод Стиллофф возобновляет воспроизведение, отменяя режим по-прежнему.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Метод Стиллофф
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683774"
---
# <a name="stilloff-method"></a><span data-ttu-id="c2d56-103">Метод Стиллофф</span><span class="sxs-lookup"><span data-stu-id="c2d56-103">StillOff Method</span></span>

> [!Note]  
> <span data-ttu-id="c2d56-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c2d56-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c2d56-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="c2d56-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c2d56-106">`StillOff`Метод возобновляет воспроизведение, отменяя режим по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="c2d56-106">The `StillOff` method resumes playback, canceling still mode.</span></span>

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a><span data-ttu-id="c2d56-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2d56-107">Return Value</span></span>

<span data-ttu-id="c2d56-108">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="c2d56-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2d56-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2d56-109">Remarks</span></span>

<span data-ttu-id="c2d56-110">[Навигатор DVD](dvd-navigator-filter.md) переходит в режим по-прежнему при обнаружении кадра, созданного на диске. Он уведомляет ваше приложение, отправляя \_ DVD-диск EC \_ \_ на событие.</span><span class="sxs-lookup"><span data-stu-id="c2d56-110">The [DVD Navigator](dvd-navigator-filter.md) goes into still mode when it encounters a still frame authored on the disc. It notifies your application by sending an EC\_DVD\_STILL\_ON event.</span></span> <span data-ttu-id="c2d56-111">Режим по-прежнему отличается от навигатора DVD в приостановленном состоянии из-за пользовательской операции.</span><span class="sxs-lookup"><span data-stu-id="c2d56-111">Still mode is different from the DVD Navigator being in a paused state because of a user operation.</span></span> <span data-ttu-id="c2d56-112">Вызов `StillOff` возобновляет воспроизведение из-прежнему режима, но не перезапускает Навигатор DVD, когда он находится в приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c2d56-112">Calling `StillOff` resumes playback from still mode but does not restart the DVD Navigator when it is in a paused state.</span></span>

 

 



