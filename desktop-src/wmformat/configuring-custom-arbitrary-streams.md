---
title: Настройка настраиваемых произвольных потоков
description: Настройка настраиваемых произвольных потоков
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- потоки, Настройка пользовательских произвольных потоков
- кодеки, Настройка пользовательских произвольных потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775698"
---
# <a name="configuring-custom-arbitrary-streams"></a><span data-ttu-id="b5cc9-105">Настройка настраиваемых произвольных потоков</span><span class="sxs-lookup"><span data-stu-id="b5cc9-105">Configuring Custom Arbitrary Streams</span></span>

<span data-ttu-id="b5cc9-106">При использовании собственного произвольного типа данных необходимо создать значение идентификатора GUID, которое будет служить основным идентификатором типа носителя.</span><span class="sxs-lookup"><span data-stu-id="b5cc9-106">When using your own arbitrary data type, you must create a GUID value to serve as the major media type identifier for it.</span></span> <span data-ttu-id="b5cc9-107">Когда модуль записи встречает поток в профиле с основным типом, который он не распознает, предполагается, что поток является пользовательским произвольным набором данных.</span><span class="sxs-lookup"><span data-stu-id="b5cc9-107">When the writer encounters a stream in a profile with a major type it does not recognize, it assumes that the stream is custom arbitrary data.</span></span> <span data-ttu-id="b5cc9-108">Он примет примеры, паккетизе их и объединит их с образцами из других потоков в файле, не проверяя данные каким бы то ни было.</span><span class="sxs-lookup"><span data-stu-id="b5cc9-108">It will accept your samples, packetize them, and combine them with samples from the other streams in the file without verifying the data in any way.</span></span>

<span data-ttu-id="b5cc9-109">Можно также создать собственные идентификаторы GUID подтипа для определения подкатегорий пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="b5cc9-109">You can also create your own subtype GUID identifiers to define subcategories of your custom data.</span></span> <span data-ttu-id="b5cc9-110">Модуль записи будет полностью игнорировать эти подтипы, но они будут сохранены в разделе заголовка файла ASF, поэтому приложение для чтения может получить их и принимать решения на их основе.</span><span class="sxs-lookup"><span data-stu-id="b5cc9-110">The writer will ignore these subtypes completely, but they will be preserved in the header section of the ASF file, so your reading application can retrieve them and make decisions based on them.</span></span>

<span data-ttu-id="b5cc9-111">Для произвольного потока требуется Побитовая скорость и окно буфера, а также должна быть структура [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) со значениями, которые очищаются, за исключением основного типа и подтипа носителя (если используется один).</span><span class="sxs-lookup"><span data-stu-id="b5cc9-111">An arbitrary stream requires a bit rate and buffer window, and must have a [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure with the values cleared except for the major media type and subtype(if using one).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5cc9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="b5cc9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5cc9-113">**Общая конфигурация для всех потоков**</span><span class="sxs-lookup"><span data-stu-id="b5cc9-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="b5cc9-114">**Настройка произвольных типов потоков**</span><span class="sxs-lookup"><span data-stu-id="b5cc9-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="b5cc9-115">**Настраиваемые произвольные потоки данных**</span><span class="sxs-lookup"><span data-stu-id="b5cc9-115">**Custom Arbitrary Data Streams**</span></span>](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




