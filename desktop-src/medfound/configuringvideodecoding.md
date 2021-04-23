---
description: Настройка декодирования видео
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Настройка декодирования видео (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701326"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a><span data-ttu-id="af221-103">Настройка декодирования видео (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="af221-103">Configuring Video Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="af221-104">Декодирование по сути является противоположностью кодировки в плане конфигурации.</span><span class="sxs-lookup"><span data-stu-id="af221-104">Decoding is essentially the opposite of encoding in terms of configuration.</span></span> <span data-ttu-id="af221-105">Декодер поддерживает очень мало свойств, и ни один из них не требуется.</span><span class="sxs-lookup"><span data-stu-id="af221-105">The decoder supports very few properties, and none of them is required.</span></span> <span data-ttu-id="af221-106">Установите тип входных данных в тип, используемый для выходных данных декодера (включая частные данные кодека).</span><span class="sxs-lookup"><span data-stu-id="af221-106">Set the input type to the type used for the decoder output (including the codec private data).</span></span> <span data-ttu-id="af221-107">Затем задайте для выходных данных нужный формат без сжатия, задайте структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , отражающую правильный размер кадра, и начните обработку образцов.</span><span class="sxs-lookup"><span data-stu-id="af221-107">Then set the output to the desired uncompressed format, set the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to reflect the proper frame size, and start processing samples.</span></span>

<span data-ttu-id="af221-108">Необходимо предоставить декодеру тип мультимедиа, содержащий частные данные кодека, расположенные непосредственно после структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="af221-108">You must supply the decoder with a media type that includes the codec private data positioned immediately after the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="af221-109">Декодер не может декодировать содержимое без этих данных.</span><span class="sxs-lookup"><span data-stu-id="af221-109">The decoder cannot decode the content without this data.</span></span> <span data-ttu-id="af221-110">Проверка формата, выполняемая декодером, не проверяет личные данные.</span><span class="sxs-lookup"><span data-stu-id="af221-110">The format validation performed by the decoder does not validate the private data.</span></span> <span data-ttu-id="af221-111">Если частные данные кодека отсутствуют или неверны, декодер реагирует как на повреждение потока.</span><span class="sxs-lookup"><span data-stu-id="af221-111">If the codec private data is missing or incorrect, the decoder responds as if the bit stream is corrupted.</span></span> <span data-ttu-id="af221-112">Дополнительные сведения см. [в разделе Использование частных данных видеокодека](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="af221-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af221-113">См. также</span><span class="sxs-lookup"><span data-stu-id="af221-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af221-114">Использование личных данных видеокодека</span><span class="sxs-lookup"><span data-stu-id="af221-114">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="af221-115">Работа с видео</span><span class="sxs-lookup"><span data-stu-id="af221-115">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
