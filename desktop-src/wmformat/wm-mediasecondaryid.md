---
title: WM/Медиакласссекондарид
description: Атрибут WM/Медиакласссекондарид содержит идентификатор GUID вторичного класса мультимедиа.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- Формат Windows Media WM/Медиакласссекондарид
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411911"
---
# <a name="wmmediaclasssecondaryid"></a><span data-ttu-id="1069c-104">WM/Медиакласссекондарид</span><span class="sxs-lookup"><span data-stu-id="1069c-104">WM/MediaClassSecondaryID</span></span>

<span data-ttu-id="1069c-105">Атрибут **WM/медиакласссекондарид** содержит идентификатор GUID вторичного класса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1069c-105">The **WM/MediaClassSecondaryID** attribute contains the GUID of the secondary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1069c-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="1069c-106">Global Constant</span></span>

<span data-ttu-id="1069c-107">g \_ всзвммедиакласссекондарид</span><span class="sxs-lookup"><span data-stu-id="1069c-107">g\_wszWMMediaClassSecondaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="1069c-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1069c-108">Data Type</span></span>

<span data-ttu-id="1069c-109">**\_GUID типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1069c-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="1069c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1069c-110">Remarks</span></span>

<span data-ttu-id="1069c-111">Для этого атрибута следует задать одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1069c-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="1069c-112">Идентификатор GUID вторичного класса</span><span class="sxs-lookup"><span data-stu-id="1069c-112">Secondary class GUID</span></span>                   | <span data-ttu-id="1069c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="1069c-113">Description</span></span>                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1069c-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span><span class="sxs-lookup"><span data-stu-id="1069c-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span></span> | <span data-ttu-id="1069c-115">Используется для файлов звуковой книги.</span><span class="sxs-lookup"><span data-stu-id="1069c-115">Use for audio book files.</span></span>                                                                                                                                                               |
| <span data-ttu-id="1069c-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span><span class="sxs-lookup"><span data-stu-id="1069c-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span></span> | <span data-ttu-id="1069c-117">Используется для звуковых файлов, содержащих произнесенные слова, но не для звуковых книг.</span><span class="sxs-lookup"><span data-stu-id="1069c-117">Use for audio files that contain spoken word, but are not audio books.</span></span> <span data-ttu-id="1069c-118">Например, подпрограммы комедия.</span><span class="sxs-lookup"><span data-stu-id="1069c-118">For example, stand-up comedy routines.</span></span>                                                                           |
| <span data-ttu-id="1069c-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span><span class="sxs-lookup"><span data-stu-id="1069c-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span></span> | <span data-ttu-id="1069c-120">Используется для звуковых файлов, связанных с новостями.</span><span class="sxs-lookup"><span data-stu-id="1069c-120">Use for audio files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="1069c-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span><span class="sxs-lookup"><span data-stu-id="1069c-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span></span> | <span data-ttu-id="1069c-122">Используйте для звуковых файлов с разговором Показать содержимое.</span><span class="sxs-lookup"><span data-stu-id="1069c-122">Use for audio files with talk show content.</span></span>                                                                                                                                             |
| <span data-ttu-id="1069c-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span><span class="sxs-lookup"><span data-stu-id="1069c-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span></span> | <span data-ttu-id="1069c-124">Используется для видеофайлов, связанных с новостями.</span><span class="sxs-lookup"><span data-stu-id="1069c-124">Use for video files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="1069c-125">"D6DE1D88-C77C-4593-БФБК-9C61E8C373E3"</span><span class="sxs-lookup"><span data-stu-id="1069c-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span></span> | <span data-ttu-id="1069c-126">Используйте для видеофайлов, содержащих веб-экраны, короткие мультипликация, трейлеры фильмов и т. д.</span><span class="sxs-lookup"><span data-stu-id="1069c-126">Use for video files containing Web-based shows, short films, movie trailers, and so on.</span></span> <span data-ttu-id="1069c-127">Это общий идентификатор для развлекательного видео, который не помещается в другую категорию.</span><span class="sxs-lookup"><span data-stu-id="1069c-127">This is the general identifier for video entertainment that does not fit into another category.</span></span> |
| <span data-ttu-id="1069c-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span><span class="sxs-lookup"><span data-stu-id="1069c-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span></span> | <span data-ttu-id="1069c-129">Используется для звуковых файлов, содержащих звуковые клипы из игр.</span><span class="sxs-lookup"><span data-stu-id="1069c-129">Use for audio files containing sound clips from games.</span></span>                                                                                                                                  |
| <span data-ttu-id="1069c-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span><span class="sxs-lookup"><span data-stu-id="1069c-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span></span> | <span data-ttu-id="1069c-131">Используется для звуковых файлов, содержащих полные песни из звуковых дорожек игры.</span><span class="sxs-lookup"><span data-stu-id="1069c-131">Use for audio files containing complete songs from game sound tracks.</span></span> <span data-ttu-id="1069c-132">Если в файле кодируется только часть песни, используйте вместо этого идентификатор для звуковых клипов игры.</span><span class="sxs-lookup"><span data-stu-id="1069c-132">If only part of a song is encoded in the file, use the identifier for game sound clips instead.</span></span>                   |
| <span data-ttu-id="1069c-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span><span class="sxs-lookup"><span data-stu-id="1069c-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span></span> | <span data-ttu-id="1069c-134">Используйте для видеофайлов с музыкальными видео.</span><span class="sxs-lookup"><span data-stu-id="1069c-134">Use for video files containing music videos.</span></span>                                                                                                                                            |
| <span data-ttu-id="1069c-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span><span class="sxs-lookup"><span data-stu-id="1069c-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span></span> | <span data-ttu-id="1069c-136">Используйте для видеофайлов, содержащих общие сведения о домашнем видео.</span><span class="sxs-lookup"><span data-stu-id="1069c-136">Use for video files containing general home video.</span></span>                                                                                                                                      |
| <span data-ttu-id="1069c-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span><span class="sxs-lookup"><span data-stu-id="1069c-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span></span> | <span data-ttu-id="1069c-138">Используется для видеофайлов с функцией мультипликация.</span><span class="sxs-lookup"><span data-stu-id="1069c-138">Use for video files containing feature films.</span></span>                                                                                                                                           |
| <span data-ttu-id="1069c-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span><span class="sxs-lookup"><span data-stu-id="1069c-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span></span> | <span data-ttu-id="1069c-140">Используется для видеофайлов, содержащих телевизионные передачи.</span><span class="sxs-lookup"><span data-stu-id="1069c-140">Use for video files containing television shows.</span></span> <span data-ttu-id="1069c-141">Для веб-показов используйте более универсальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1069c-141">For Web-based shows, use the more generic identifier.</span></span>                                                                                  |
| <span data-ttu-id="1069c-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span><span class="sxs-lookup"><span data-stu-id="1069c-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span></span> | <span data-ttu-id="1069c-143">Используется для видеофайлов с корпоративным видео.</span><span class="sxs-lookup"><span data-stu-id="1069c-143">Use for video files containing corporate video.</span></span> <span data-ttu-id="1069c-144">Например, записанные встречи или обучающие видеоматериалы.</span><span class="sxs-lookup"><span data-stu-id="1069c-144">For example, recorded meetings or training videos.</span></span>                                                                                      |
| <span data-ttu-id="1069c-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span><span class="sxs-lookup"><span data-stu-id="1069c-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span></span> | <span data-ttu-id="1069c-146">Используется для видеофайлов с домашним видео, сделанным из фотографий.</span><span class="sxs-lookup"><span data-stu-id="1069c-146">Use for video files containing home video made from photographs.</span></span>                                                                                                                        |



 

<span data-ttu-id="1069c-147">При указании идентификатора вторичного класса файл также должен содержать атрибут идентификатора первичного класса.</span><span class="sxs-lookup"><span data-stu-id="1069c-147">When specifying a secondary class identifier, the file should also contain a primary class identifier attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="1069c-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1069c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1069c-149">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="1069c-149">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="1069c-150">**WM/Медиакласспримарид**</span><span class="sxs-lookup"><span data-stu-id="1069c-150">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
</dt> </dl>

 

 




