---
description: Свойство Двдадм. ДефаултаудиолЦид задает или получает параметр реестра для указанного пользователем кода языка по умолчанию для звукового потока.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: ДефаултаудиолЦид, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673081"
---
# <a name="defaultaudiolcid-property"></a><span data-ttu-id="59e73-103">ДефаултаудиолЦид, свойство</span><span class="sxs-lookup"><span data-stu-id="59e73-103">DefaultAudioLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="59e73-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="59e73-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="59e73-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="59e73-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="59e73-106">`DVDAdm.DefaultAudioLCID`Свойство задает или получает параметр реестра для указанного пользователем кода языка по умолчанию для звукового потока.</span><span class="sxs-lookup"><span data-stu-id="59e73-106">The `DVDAdm.DefaultAudioLCID` property sets or retrieves the registry setting for the user-specified default LCID for the audio stream.</span></span>

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a><span data-ttu-id="59e73-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59e73-107">Return Value</span></span>

<span data-ttu-id="59e73-108">Возвращает целочисленное значение, представляющее заданный пользователем код звука по умолчанию, сохраненный в параметрах реестра для приложения DVD.</span><span class="sxs-lookup"><span data-stu-id="59e73-108">Returns an Integer value representing the user-specified default audio LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="59e73-109">Это значение не обязательно совпадает с звуковым потоком по умолчанию, созданным на DVD-диске.</span><span class="sxs-lookup"><span data-stu-id="59e73-109">This value is not necessarily the same as the default audio stream as authored on the DVD.</span></span>

## <a name="remarks"></a><span data-ttu-id="59e73-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59e73-110">Remarks</span></span>

<span data-ttu-id="59e73-111">Это свойство доступно для чтения и записи и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59e73-111">This property is read/write with no default value.</span></span> <span data-ttu-id="59e73-112">Если не указан код звука по умолчанию, объект Мсдвдадм воспроизведет аудиопоток, который помечен как поток по умолчанию на диске.</span><span class="sxs-lookup"><span data-stu-id="59e73-112">If no default audio LCID is specified, the MSDVDAdm object will play the audio stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="59e73-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59e73-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e73-114">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="59e73-114">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



