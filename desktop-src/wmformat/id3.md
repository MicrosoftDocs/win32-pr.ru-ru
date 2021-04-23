---
title: Поддержка ID3
description: ID3 — это организация, которая определила набор стандартов для включения метаданных в звуковые файлы MPEG Layer-3 (MP3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Пакет SDK для Windows Media Format, поддержка ID3
- Расширенный системный формат (ASF), поддержка ID3
- ASF (Расширенный системный формат), поддержка ID3
- метаданные, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778905"
---
# <a name="id3-support"></a><span data-ttu-id="d24e7-108">Поддержка ID3</span><span class="sxs-lookup"><span data-stu-id="d24e7-108">ID3 Support</span></span>

<span data-ttu-id="d24e7-109">ID3 — это организация, которая определила набор стандартов для включения метаданных в звуковые файлы MPEG Layer-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="d24e7-109">ID3 is an organization that has defined a set of standards for including metadata in MPEG Layer-3 (MP3) audio files.</span></span> <span data-ttu-id="d24e7-110">Объекты пакета SDK для формата Windows Media обеспечивают поддержку атрибутов, совместимых с ID3.</span><span class="sxs-lookup"><span data-stu-id="d24e7-110">The objects of the Windows Media Format SDK provide support for ID3 compatible attributes.</span></span> <span data-ttu-id="d24e7-111">Поддерживаются три различные версии ID3: ID3v1. x, ID3v 2.2 и ID3v 2.3/v2, 4.</span><span class="sxs-lookup"><span data-stu-id="d24e7-111">Three distinct ID3 versions are supported: ID3v1.x, ID3v2.2, and ID3v2.3/v2,4.</span></span> <span data-ttu-id="d24e7-112">Список атрибутов, которые эквивалентны кадрам ID3, см. в разделе [Поддержка тегов ID3](id3-tag-support.md).</span><span class="sxs-lookup"><span data-stu-id="d24e7-112">For a list of the attributes that equate to ID3 frames, see [ID3 Tag Support](id3-tag-support.md).</span></span>

<span data-ttu-id="d24e7-113">Если не указано иное, объекты этого пакета SDK не выполняют проверку данных кадра ID3.</span><span class="sxs-lookup"><span data-stu-id="d24e7-113">Unless otherwise noted, no validation of ID3 frame data is performed by the objects of this SDK.</span></span> <span data-ttu-id="d24e7-114">Например, атрибут метаданных [**WM/песен \_ синхронизированы**](wm-lyrics-synchronised.md) сохраняет песни песни с соответствующими штампами времени.</span><span class="sxs-lookup"><span data-stu-id="d24e7-114">For example, the metadata attribute [**WM/Lyrics\_Synchronised**](wm-lyrics-synchronised.md) stores the song lyrics with corresponding time stamps.</span></span> <span data-ttu-id="d24e7-115">При записи атрибута **WM/песен \_ синхронизированы** объекты этого пакета SDK не будут проверять, что отметки времени находятся в хронологическом порядке или выполняют проверку любого вида.</span><span class="sxs-lookup"><span data-stu-id="d24e7-115">When writing a **WM/Lyrics\_Synchronised** attribute, the objects of this SDK will not check to ensure that the time stamps are in chronological order or perform validation of any kind.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d24e7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d24e7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d24e7-117">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="d24e7-117">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="d24e7-118">**Компоненты метаданных**</span><span class="sxs-lookup"><span data-stu-id="d24e7-118">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="d24e7-119">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="d24e7-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




