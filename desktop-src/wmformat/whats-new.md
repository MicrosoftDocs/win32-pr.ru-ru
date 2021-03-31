---
title: Новые возможности (пакет SDK для Windows Media Format 11)
description: What's New
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK, новые возможности
- Windows Media Format SDK, функции
- Windows Media Format SDK, новые функции
- Пакет SDK для Windows Media Format, расширенные API клиента
- Пакет Windows Media Format SDK, обновления DRM
- Пакет Windows Media Format SDK, обновления кодеков
- Windows Media Format SDK, эскизы изображений
- Управление цифровыми правами (DRM), новые функции
- DRM (Управление цифровыми правами), новые возможности
- эскизы рисунков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800778"
---
# <a name="whats-new-windows-media-format-11-sdk"></a><span data-ttu-id="a37c2-113">Новые возможности (пакет SDK для Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="a37c2-113">What's New (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a37c2-114">В пакете SDK для формата Windows Media 11 появились новые функции управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="a37c2-114">The Windows Media Format 11 SDK introduces new digital rights management (DRM) features.</span></span> <span data-ttu-id="a37c2-115">С момента выпуска 9,5 в пакет SDK были внесены следующие изменения.</span><span class="sxs-lookup"><span data-stu-id="a37c2-115">The following changes have been made to the SDK since the 9.5 release.</span></span>

## <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="a37c2-116">Расширенные API клиента DRM Windows Media</span><span class="sxs-lookup"><span data-stu-id="a37c2-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="a37c2-117">Пакет SDK для Windows Media Format 11 поставляется с новым набором интерфейсов API DRM.</span><span class="sxs-lookup"><span data-stu-id="a37c2-117">The Windows Media Format 11 SDK ships with a new set of DRM APIs.</span></span> <span data-ttu-id="a37c2-118">Эти API реализованы в собственной библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a37c2-118">These APIs are implemented in their own library.</span></span> <span data-ttu-id="a37c2-119">Многие функции DRM, поддерживаемые объектами пакета SDK Windows Media Format, также поддерживаются расширенными API клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a37c2-119">Many of the DRM features supported by the objects of the Windows Media Format SDK are also supported by the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="a37c2-120">Основное различие в новых интерфейсах API заключается в том, что они не полагаются на наличие ASF-файла для работы.</span><span class="sxs-lookup"><span data-stu-id="a37c2-120">The primary difference in the new APIs is that they do not rely on having an ASF file to work.</span></span> <span data-ttu-id="a37c2-121">Вместо этого новые интерфейсы API напрямую работают с локальным хранилищем лицензий, часто используя идентификатор ключа для идентификации лицензий.</span><span class="sxs-lookup"><span data-stu-id="a37c2-121">Instead, the new APIs deal with the local license store directly, often using the key ID to identify licenses.</span></span>

<span data-ttu-id="a37c2-122">Дополнительные сведения см. в документации по [расширенным API-интерфейсам клиента DRM Windows Media](windows-media-drm-client-extended-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="a37c2-122">For more information, see the [Windows Media DRM Client Extended APIs](windows-media-drm-client-extended-apis.md) documentation.</span></span>

## <a name="updated-codecs"></a><span data-ttu-id="a37c2-123">Обновленные кодеки</span><span class="sxs-lookup"><span data-stu-id="a37c2-123">Updated Codecs</span></span>

<span data-ttu-id="a37c2-124">Кодек расширенного профиля Windows Media Video 9 был обновлен для создания сжатого потока, который соответствует опубликованному стандарту VC-1 SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a37c2-124">The Windows Media Video 9 Advanced Profile codec has been updated to produce a compressed bit stream that is compliant with the published SMPTE VC-1 standard.</span></span>

<span data-ttu-id="a37c2-125">В этот выпуск пакета SDK также включен кодек Windows Media Audio 10 Professional.</span><span class="sxs-lookup"><span data-stu-id="a37c2-125">The Windows Media Audio 10 Professional codec is also included in this release of the SDK.</span></span> <span data-ttu-id="a37c2-126">Новый аудиокодек имеет улучшенное качество с более низкими скоростью.</span><span class="sxs-lookup"><span data-stu-id="a37c2-126">The new audio codec features improved quality at lower bit rates.</span></span>

## <a name="thumbnail-right"></a><span data-ttu-id="a37c2-127">Эскиз справа</span><span class="sxs-lookup"><span data-stu-id="a37c2-127">Thumbnail Right</span></span>

<span data-ttu-id="a37c2-128">Приложения могут запрашивать новое действие DRM для чтения из видео для создания эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="a37c2-128">Applications can request a new DRM action to read from video to create a thumbnail image.</span></span> <span data-ttu-id="a37c2-129">Это позволяет приложениям создавать и отображать миниатюрные изображения для видеофайлов, не открывая файл для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a37c2-129">This enables applications to create and display thumbnail images for video files without opening the file for playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a37c2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a37c2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a37c2-131">**О пакете SDK для формата Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a37c2-131">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




