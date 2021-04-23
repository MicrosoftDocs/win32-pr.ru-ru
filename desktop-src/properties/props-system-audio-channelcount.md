---
description: 'Указывает число каналов для звукового файла. Возможные значения: 1 для Mono и 2 для стерео.'
ms.assetid: 8a028167-dc0f-4ed9-a710-568caf1b9a47
title: System. Audio. Чаннелкаунт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a370e517f8c3552e27bf034c4873b5e1cb593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898666"
---
# <a name="systemaudiochannelcount"></a><span data-ttu-id="e0240-104">System. Audio. Чаннелкаунт</span><span class="sxs-lookup"><span data-stu-id="e0240-104">System.Audio.ChannelCount</span></span>

<span data-ttu-id="e0240-105">Указывает число каналов для звукового файла.</span><span class="sxs-lookup"><span data-stu-id="e0240-105">Indicates the channel count for the audio file.</span></span> <span data-ttu-id="e0240-106">Возможные значения: 1 для Mono и 2 для стерео.</span><span class="sxs-lookup"><span data-stu-id="e0240-106">Possible values are 1 for mono and 2 for stereo.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="e0240-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0240-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Audio.ChannelCount
   shellPKey = PKEY_Audio_ChannelCount
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 7
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Mono
            value = 1
            text = 1 (mono)
            defineToken = AUDIO_CHANNELCOUNT_MONO
         enum
            name = Stereo
            value = 2
            text = 2 (stereo)
            defineToken = AUDIO_CHANNELCOUNT_STEREO
```

## <a name="windows-vista"></a><span data-ttu-id="e0240-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0240-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Audio.ChannelCount
   shellPKey = PKEY_Audio_ChannelCount
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 7
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = 1 (mono)
            defineName = AUDIO_CHANNELCOUNT_MONO
         enum
            value = 2
            text = 2 (stereo)
            defineName = AUDIO_CHANNELCOUNT_STEREO
```

## <a name="remarks"></a><span data-ttu-id="e0240-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0240-109">Remarks</span></span>

<span data-ttu-id="e0240-110">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="e0240-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0240-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e0240-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0240-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="e0240-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e0240-113">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="e0240-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e0240-114">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="e0240-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e0240-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e0240-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e0240-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e0240-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e0240-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e0240-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e0240-118">булеанформат</span><span class="sxs-lookup"><span data-stu-id="e0240-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e0240-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e0240-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e0240-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e0240-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e0240-121">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="e0240-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e0240-122">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="e0240-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e0240-123">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="e0240-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e0240-124">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="e0240-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e0240-125">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="e0240-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
