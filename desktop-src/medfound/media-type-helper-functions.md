---
description: Следующие функции относятся к объектам типа мультимедиа.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Вспомогательные функции типа мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547399"
---
# <a name="media-type-helper-functions"></a><span data-ttu-id="b8ea4-103">Вспомогательные функции типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b8ea4-103">Media Type Helper Functions</span></span>

<span data-ttu-id="b8ea4-104">Следующие функции относятся к объектам типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-104">The following functions pertain to media type objects.</span></span>



| <span data-ttu-id="b8ea4-105">Функция</span><span class="sxs-lookup"><span data-stu-id="b8ea4-105">Function</span></span>                                                                     | <span data-ttu-id="b8ea4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b8ea4-106">Description</span></span>                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b8ea4-107">**мфаверажетимеперфраметофрамерате**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-107">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="b8ea4-108">Вычисляет частоту кадров от средней длительности видеокадра.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-108">Calculates the frame rate from the average duration of a video frame.</span></span> |
| [<span data-ttu-id="b8ea4-109">**мфкалкулатеимажесизе**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-109">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="b8ea4-110">Получает размер изображения для несжатого видеоформата.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-110">Retrieves the image size for an uncompressed video format.</span></span>            |
| [<span data-ttu-id="b8ea4-111">**мфкомпарефуллтопартиалмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-111">**MFCompareFullToPartialMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | <span data-ttu-id="b8ea4-112">Сравнение полного типа носителя с частичным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-112">Compares a full media type to a partial media type.</span></span>                   |
| [<span data-ttu-id="b8ea4-113">**мфкреатемедиатипе**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-113">**MFCreateMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | <span data-ttu-id="b8ea4-114">Создает пустой тип носителя.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-114">Creates an empty media type.</span></span>                                          |
| [<span data-ttu-id="b8ea4-115">**мффрамератетоаверажетимеперфраме**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-115">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="b8ea4-116">Преобразует частоту кадров видео в Длительность кадра.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-116">Converts a video frame rate into a frame duration.</span></span>                    |
| [<span data-ttu-id="b8ea4-117">**мфжетстридефорбитмапинфохеадер**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-117">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="b8ea4-118">Возвращает минимальный шаг поверхности для формата видео.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-118">Retrieves the minimum surface stride for a video format.</span></span>              |
| [<span data-ttu-id="b8ea4-119">**мфисформатюв**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-119">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="b8ea4-120">Запрашивает, является ли код FOURCC или значение **D3DFORMAT** форматом YUV.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-120">Queries whether a FOURCC code or **D3DFORMAT** value is a YUV format.</span></span> |
| [<span data-ttu-id="b8ea4-121">**мфвалидатемедиатипесизе**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-121">**MFValidateMediaTypeSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | <span data-ttu-id="b8ea4-122">Проверяет размер буфера для блока видеоформата.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-122">Validates the size of a buffer for a video format block.</span></span>              |
| [<span data-ttu-id="b8ea4-123">**мфврапмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-123">**MFWrapMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | <span data-ttu-id="b8ea4-124">Создает тип носителя, который служит оболочкой для другого типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b8ea4-124">Creates a media type that wraps another media type.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="b8ea4-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b8ea4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8ea4-126">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="b8ea4-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="b8ea4-127">Преобразования типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b8ea4-127">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="b8ea4-128">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="b8ea4-128">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



