---
description: Состояние воспроизведения устройства.
ms.assetid: 7F77459B-5900-4967-A2A3-AAEE78DF84E1
title: System. Devices. Плайбаккстате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a95b736d80df49587954f20c4c000c82779d5648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683322"
---
# <a name="systemdevicesplaybackstate"></a><span data-ttu-id="e7c18-103">System. Devices. Плайбаккстате</span><span class="sxs-lookup"><span data-stu-id="e7c18-103">System.Devices.PlaybackState</span></span>

<span data-ttu-id="e7c18-104">Состояние воспроизведения устройства.</span><span class="sxs-lookup"><span data-stu-id="e7c18-104">The playback state of the device.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="e7c18-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="e7c18-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.Devices.PlaybackState
   shellPKey = PKEY_Devices_PlaybackState
   formatID = 3633DE59-6825-4381-A49B-9F6BA13A1471
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = UnknownState
            value = 0
            text = Unknown State
            defineToken = PLAYBACKSTATE_UNKNOWN
         enum
            name = Stopped
            value = 1
            text = Stopped
            defineToken = PLAYBACKSTATE_STOPPED
         enum
            name = Playing
            value = 2
            text = Playing
            defineToken = PLAYBACKSTATE_PLAYING
         enum
            name = Transitioning
            value = 3
            text = Transitioning
            defineToken = PLAYBACKSTATE_TRANSITIONING
         enum
            name = PlaybackPaused
            value = 4
            text = Paused
            defineToken = PLAYBACKSTATE_PAUSED
         enum
            name = RecordingPaused
            value = 5
            text = Recording Paused
            defineToken = PLAYBACKSTATE_RECORDINGPAUSED
         enum
            name = Recording
            value = 6
            text = Recording
            defineToken = PLAYBACKSTATE_RECORDING
         enum
            name = NoMedia
            value = 7
            text = No Media
            defineToken = PLAYBACKSTATE_NOMEDIA
```

## <a name="remarks"></a><span data-ttu-id="e7c18-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7c18-106">Remarks</span></span>

<span data-ttu-id="e7c18-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="e7c18-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7c18-108">См. также</span><span class="sxs-lookup"><span data-stu-id="e7c18-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7c18-109">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="e7c18-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e7c18-110">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="e7c18-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e7c18-111">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="e7c18-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e7c18-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e7c18-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e7c18-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e7c18-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e7c18-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e7c18-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e7c18-115">булеанформат</span><span class="sxs-lookup"><span data-stu-id="e7c18-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e7c18-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e7c18-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e7c18-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e7c18-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e7c18-118">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="e7c18-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e7c18-119">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="e7c18-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e7c18-120">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="e7c18-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e7c18-121">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="e7c18-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e7c18-122">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="e7c18-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
