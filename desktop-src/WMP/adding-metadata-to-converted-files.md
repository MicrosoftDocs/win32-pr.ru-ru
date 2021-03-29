---
title: Добавление метаданных в преобразованные файлы
description: Добавление метаданных в преобразованные файлы
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Проигрыватель Windows Media, процесс преобразования
- Подключаемые модули проигрывателя Windows Media, преобразование
- подключаемые модули, преобразование
- подключаемые модули преобразования, Добавление метаданных в преобразованные файлы
- Добавление метаданных в преобразованные файлы
- метаданные, добавление к преобразованным файлам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791952"
---
# <a name="adding-metadata-to-converted-files"></a><span data-ttu-id="c1dd8-109">Добавление метаданных в преобразованные файлы</span><span class="sxs-lookup"><span data-stu-id="c1dd8-109">Adding Metadata to Converted Files</span></span>

<span data-ttu-id="c1dd8-110">Преобразованные файлы должны содержать определенные метаданные, чтобы обеспечить хорошее взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-110">Converted files must contain certain metadata to ensure a good user experience.</span></span> <span data-ttu-id="c1dd8-111">Как минимум, преобразованные файлы должны содержать основные атрибуты, перечисленные в [руководстве по использованию метаданных Windows Media](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c1dd8-111">At a minimum, converted files must contain the primary attributes listed in the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

<span data-ttu-id="c1dd8-112">Для музыкальных файлов задайте для **WM/медиакласспримарид** значение D1607DBC-E323-4BE2-86A1-48A42A28441E.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-112">For music files, set the value for **WM/MediaClassPrimaryID** to D1607DBC-E323-4BE2-86A1-48A42A28441E.</span></span>

<span data-ttu-id="c1dd8-113">Для файлов голосовой почты задайте для **WM/медиакласспримарид** значение 01CD0F29-DA4E-4157-897B-6275D50C4F11, которое является основным классом GUID для звуковых файлов.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-113">For voicemail files, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11, which is the primary class GUID for audio files.</span></span> <span data-ttu-id="c1dd8-114">Задайте для **WM/медиакласссекондарид** значение 193c8824-4d52-4178-90bd-305240b04636.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-114">Set the value for **WM/MediaClassSecondaryID** to 193c8824-4d52-4178-90bd-305240b04636.</span></span>

<span data-ttu-id="c1dd8-115">В случае с голосовыми заметками установите для **WM/медиакласспримарид** значение 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-115">For voice notes, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span></span> <span data-ttu-id="c1dd8-116">Задайте для **WM/медиакласссекондарид** значение 3A172A13-2BD9-4831-835B-114F6A95943F.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-116">Set the value for **WM/MediaClassSecondaryID** to 3A172A13-2BD9-4831-835B-114F6A95943F.</span></span>

<span data-ttu-id="c1dd8-117">Задайте в качестве значения для **WM/контентдистрибутор** имя ключа для музыкальной службы, которая предоставил содержимое.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-117">Set the value for **WM/ContentDistributor** to the key name for the music service that provided the content.</span></span>

<span data-ttu-id="c1dd8-118">Задайте для **WM/уникуефилеидентифиер** значение идентификатора содержимого.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-118">Set the value for **WM/UniqueFileIdentifier** to the content ID.</span></span> <span data-ttu-id="c1dd8-119">Это позволит вам получать определенные элементы содержимого в будущем.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-119">This will enable you to retrieve specific content items at a future time.</span></span>

<span data-ttu-id="c1dd8-120">Задайте значение для **WM/вмшадовфилесаурцефилетипе**.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-120">Set a value for **WM/WMShadowFileSourceFileType**.</span></span>

<span data-ttu-id="c1dd8-121">Для защищенного содержимого используйте пакет SDK Windows Media Format, чтобы задать атрибуту **\_ \_ дрмхеадер DRM** идентификатор содержимого.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-121">For protected content, use the Windows Media Format SDK to set the **DRM\_DRMHeader\_ContentID** attribute to the content ID.</span></span>

<span data-ttu-id="c1dd8-122">Для защищенного содержимого задайте значение для **WM/вмшадовфилесаурцедрмтипе**.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-122">For protected content, set a value for **WM/WMShadowFileSourceDRMType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1dd8-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c1dd8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1dd8-124">**О подключаемых модулях преобразования**</span><span class="sxs-lookup"><span data-stu-id="c1dd8-124">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="c1dd8-125">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="c1dd8-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 