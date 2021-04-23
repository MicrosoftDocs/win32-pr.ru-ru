---
description: Задает максимальную скорость ввода видеокадров, передаваемых кодировщику в режиме реального времени.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: Свойство CODECAPI_AVEncMaxFrameRate (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650468"
---
# <a name="codecapi_avencmaxframerate-property"></a><span data-ttu-id="0e0e2-103">КОДЕКАПИ \_ авенкмаксфрамерате, свойство</span><span class="sxs-lookup"><span data-stu-id="0e0e2-103">CODECAPI\_AVEncMaxFrameRate property</span></span>

<span data-ttu-id="0e0e2-104">Задает максимальную скорость ввода видеокадров, передаваемых кодировщику в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="0e0e2-104">Sets the maximum real-time input rate of video frames being fed to the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e0e2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0e0e2-105">Data type</span></span>

<span data-ttu-id="0e0e2-106">**Улонгулонг** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="0e0e2-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0e0e2-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="0e0e2-107">Property GUID</span></span>

<span data-ttu-id="0e0e2-108">**КОДЕКАПИ \_ авенкмаксфрамерате**</span><span class="sxs-lookup"><span data-stu-id="0e0e2-108">**CODECAPI\_AVEncMaxFrameRate**</span></span>

## <a name="remarks"></a><span data-ttu-id="0e0e2-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e0e2-109">Remarks</span></span>

<span data-ttu-id="0e0e2-110">Это свойство позволяет вызывающему объекту указать максимальную скорость ввода видеокадров, передаваемых кодировщику в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="0e0e2-110">This property allows the caller to specify the maximum real-time input rate of video frames being fed to the encoder.</span></span> <span data-ttu-id="0e0e2-111">Это дает кодировщику указание скорости, необходимой для обработки входящих кадров.</span><span class="sxs-lookup"><span data-stu-id="0e0e2-111">This gives the encoder an indication of the rate that it will need to process the incoming frames.</span></span> <span data-ttu-id="0e0e2-112">Это полезно для кодировщиков, которые задают себя в определенной конфигурации состояния электропитания в зависимости от разрешения и частоты кадров исходного видео.</span><span class="sxs-lookup"><span data-stu-id="0e0e2-112">This is useful for encoders that set themselves into a particular power state configuration based on the resolution and frame-rate of the source video.</span></span>

<span data-ttu-id="0e0e2-113">Частота кадров выражается в виде коэффициента.</span><span class="sxs-lookup"><span data-stu-id="0e0e2-113">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="0e0e2-114">Верхний 32 бит значения атрибута содержит числитель, а младшие 32 бита содержат знаменатель.</span><span class="sxs-lookup"><span data-stu-id="0e0e2-114">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="0e0e2-115">Например, если частота кадров составляет 30 кадров в секунду (кадров/с), то соотношение составляет 30/1.</span><span class="sxs-lookup"><span data-stu-id="0e0e2-115">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="0e0e2-116">Если частота кадров составляет 29,97 кадров/с, то коэффициент равен 30000/1001.</span><span class="sxs-lookup"><span data-stu-id="0e0e2-116">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e0e2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0e0e2-117">Requirements</span></span>



| <span data-ttu-id="0e0e2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0e0e2-118">Requirement</span></span> | <span data-ttu-id="0e0e2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0e0e2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e0e2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e0e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e0e2-121">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0e0e2-121">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0e0e2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e0e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e0e2-123">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="0e0e2-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e0e2-124">Header</span><span class="sxs-lookup"><span data-stu-id="0e0e2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e0e2-125"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e0e2-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e0e2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e0e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e0e2-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e0e2-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0e0e2-128">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="0e0e2-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

