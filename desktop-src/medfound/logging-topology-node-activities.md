---
description: Действия узла топологии ведения журнала
ms.assetid: 853b3900-1214-43b9-bf0e-e45c1159c5f1
title: Действия узла топологии ведения журнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b2325b7f300ac7ebc9b11e442169ad81f5769a8b54ba0ecf4537d637a9e7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465524"
---
# <a name="logging-topology-node-activities"></a>Действия узла топологии ведения журнала

Топоедит предоставляет возможность сбора сведений о ведении журнала для узла преобразования или выходного узла топологии.

## <a name="to-setup-logging"></a>Настройка ведения журнала

1.  На **панели топология** выберите узел преобразования или выходной узел, щелкнув его.

2.  В меню **Сервис** выберите пункт **Spy Selected node**.

Во время создания топологии все вызовы методов на выбранном узле записываются в текстовый файл. Он сохраняется в папке, в которой находится файл мультимедиа. Файл журнала сохраняется с именем узла и уникальным идентификатором узла топологии. Это гарантирует, что никакие другие узлы не записываются в журнал. Чтобы получить идентификатор программным путем, вызовите метод [**имфтопологиноде:: жеттопонодеид**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).

Ниже приведен фрагмент файла журнала.

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729720 1 02729760) returns 80004001`

`GetInputCurrentType(0 02C9F4A4) returns c00d6d60`

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729760 1 02729720) returns 80004001`

`SetInputType(0 0012F8D8 0) returns 0`

`--> Arg(2, in) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=WMAudioV8, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=2048, AVG_BYTES_PER_SECOND=12000, BITS_PER_SAMPLE=16, USER_DATA=<BLOB>, {9D62927D-36BE-4CF2-B5C4-A3926E3E8711}=5760, {9D62927F-36BE-4CF2-B5C4-A3926E3E8711}=674,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputCurrentType(0 02C9F4B0) returns c00d6d60`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729640 1 02729720) returns 80004001`

`GetOutputAvailableType(0 0 02C9F4B0) returns 0`

`--> Arg(3, out) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=Float, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=8, AVG_BYTES_PER_SECOND=384000, BITS_PER_SAMPLE=32, ALL_SAMPLES_INDEPENDENT=1, FIXED_SIZE_SAMPLES=1,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputAvailableType(0 1 02C9F4B0) returns 0`

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[топоедит](topoedit.md)
</dt> </dl>

 

 



