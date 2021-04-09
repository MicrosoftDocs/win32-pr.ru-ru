---
title: Звуковые потоки
description: Звуковые потоки
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Интернет-магазины проигрывателя Windows Media, звуковые потоки
- Интернет-магазины, звуковые потоки
- Тип 1 Интернет-магазины, звуковые потоки
- Интернет-магазины проигрывателя Windows Media, потоки из музыкальных серверов
- Интернет-магазины, потоки из музыкальных серверов
- Тип 1 Интернет-магазины, потоки из музыкальных серверов
- Интернет-магазины проигрывателя Windows Media, потоки музыкального сервера
- Интернет-магазины, потоки музыкальных серверов
- Тип 1 Интернет-магазины, потоки музыкального сервера
- звуковые потоки
- потоки музыкального сервера
- потоки из музыкальных серверов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069593"
---
# <a name="audio-streams"></a><span data-ttu-id="85ce9-115">Звуковые потоки</span><span class="sxs-lookup"><span data-stu-id="85ce9-115">Audio Streams</span></span>

<span data-ttu-id="85ce9-116">Интернет-магазины могут предоставлять музыку в виде потока от музыкального сервера.</span><span class="sxs-lookup"><span data-stu-id="85ce9-116">Online stores can provide music as a stream from a music server.</span></span> <span data-ttu-id="85ce9-117">Это полезно для предоставления примеров, специальных рекламных акций или для того, чтобы пользователи подписки могли пользоваться музыкой без необходимости загрузки содержимого.</span><span class="sxs-lookup"><span data-stu-id="85ce9-117">This is useful for providing samples, special promotional items, or to enable subscription users to enjoy music without having to download the content.</span></span> <span data-ttu-id="85ce9-118">Обычно URL-адрес потока не хранится как часть музыкального каталога, а для разрешения URL-адреса непосредственно перед воспроизведением на основе идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="85ce9-118">It is common not to store the URL of the stream as part of the music catalog, but instead to resolve the URL just before playback based upon the track ID.</span></span> <span data-ttu-id="85ce9-119">Чтобы включить эту функцию, проигрыватель Windows Media вызывает [ивмпконтентпартнер:: жетстреамингурл](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) и предоставляет тип потоковой передачи (в виде значения перечисления [ВМПСТРЕАМИНГТИПЕ](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) и идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="85ce9-119">To enable this, Windows Media Player calls [IWMPContentPartner::GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) and provides the streaming type (as a [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) enumeration value) and the ID for the stream.</span></span> <span data-ttu-id="85ce9-120">Подключаемый модуль возвращает URL-адрес потока через параметр *пбструрл* .</span><span class="sxs-lookup"><span data-stu-id="85ce9-120">The plug-in returns the URL for the stream through the *pbstrURL* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85ce9-121">См. также</span><span class="sxs-lookup"><span data-stu-id="85ce9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85ce9-122">**Сведения об Интернет-магазинах типа 1**</span><span class="sxs-lookup"><span data-stu-id="85ce9-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




