---
description: Encoder-Specific записи реестра
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific записи реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719578"
---
# <a name="encoder-specific-registry-entries"></a><span data-ttu-id="90df4-103">Encoder-Specific записи реестра</span><span class="sxs-lookup"><span data-stu-id="90df4-103">Encoder-Specific Registry Entries</span></span>


<span data-ttu-id="90df4-104">Кроме перечисленных выше записей для кодировщика, необходимо также зарегистрировать кодировщик в категории кодировщиков компонента Windows Imaging Component (WIC), чтобы механизм обнаружения мог его найти.</span><span class="sxs-lookup"><span data-stu-id="90df4-104">In addition to the entries listed above for encoder, you must also register your encoder under the category of Windows Imaging Component (WIC) encoders so the discovery engine can find it.</span></span> <span data-ttu-id="90df4-105">Для этого необходимо внести в реестр следующие записи.</span><span class="sxs-lookup"><span data-stu-id="90df4-105">You do this by making the following registry entries.</span></span> <span data-ttu-id="90df4-106">Первым идентификатором GUID в следующих записях является идентификатор категории (CATID) для Викбитмапенкодерс.</span><span class="sxs-lookup"><span data-stu-id="90df4-106">The first GUID in the following entries is the category identifier (CATID) for WICBitmapEncoders.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a><span data-ttu-id="90df4-107">Регистрация формата контейнера с помощью модулей записи метаданных</span><span class="sxs-lookup"><span data-stu-id="90df4-107">Registering a Container Format with Metadata Writers</span></span>

<span data-ttu-id="90df4-108">При создании нового формата контейнера для кодека необходимо также создать записи реестра для поддержки модулей записи метаданных для блоков метаданных в изображениях.</span><span class="sxs-lookup"><span data-stu-id="90df4-108">If you create a new container format for your codec, you must also create registry entries to support metadata writers for the metadata blocks in your images.</span></span> <span data-ttu-id="90df4-109">Следующие записи должны быть созданы с идентификатором класса (CLSID) модуля записи метаданных для каждого формата метаданных, поддерживаемого в вашем формате контейнера.</span><span class="sxs-lookup"><span data-stu-id="90df4-109">The following entries need to be created under the class identifier (CLSID) of the metadata writer for each metadata format supported in your container format.</span></span> <span data-ttu-id="90df4-110">Если кодек использует контейнер формата TIFF, эта информация уже находится в реестре и вам не нужно создавать эти записи.</span><span class="sxs-lookup"><span data-stu-id="90df4-110">If your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry and you don't need to create these entries.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

<span data-ttu-id="90df4-111">Если используется формат контейнера в стиле TIFF или JPEG, необходимо зарегистрировать связь между контейнером и этим форматом контейнера.</span><span class="sxs-lookup"><span data-stu-id="90df4-111">If you use a TIFF-style or JPEG-style container format, you must register an association between your container and that container format.</span></span> <span data-ttu-id="90df4-112">Дополнительные сведения см. в статье Введение в [интеграцию с Фотоальбомом Windows и проводником Windows](-wic-integrationregentries.md).</span><span class="sxs-lookup"><span data-stu-id="90df4-112">For more information, see the introduction in [Integration with Windows Photo Gallery and Windows Explorer](-wic-integrationregentries.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90df4-113">См. также</span><span class="sxs-lookup"><span data-stu-id="90df4-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="90df4-114">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="90df4-114">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="90df4-115">Общие записи реестра</span><span class="sxs-lookup"><span data-stu-id="90df4-115">General Registry Entries</span></span>](-wic-generalregentries.md)
</dt> <dt>

[<span data-ttu-id="90df4-116">Записи реестра, относящиеся к кодировщику</span><span class="sxs-lookup"><span data-stu-id="90df4-116">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="90df4-117">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="90df4-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="90df4-118">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="90df4-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



