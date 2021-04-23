---
description: Указывает размер единиц доступа к видео в байтах. Это свойство применяется только к режимам управления с переменной скоростью (VBR).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Свойство Авенквидеокодедвидеоакцессунитсизе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be3a6e499749d862fdcc63f28b1a9a02f476d1c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989919"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a><span data-ttu-id="2c5c8-104">Авенквидеокодедвидеоакцессунитсизе, свойство</span><span class="sxs-lookup"><span data-stu-id="2c5c8-104">AVEncVideoCodedVideoAccessUnitSize property</span></span>

<span data-ttu-id="2c5c8-105">Указывает размер единиц доступа к видео в байтах.</span><span class="sxs-lookup"><span data-stu-id="2c5c8-105">Specifies the size of the video access units, in bytes.</span></span> <span data-ttu-id="2c5c8-106">Это свойство применяется только к режимам управления с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="2c5c8-106">This property applies only to variable bit rate (VBR) control modes.</span></span>

<span data-ttu-id="2c5c8-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2c5c8-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2c5c8-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2c5c8-108">Data type</span></span>

<span data-ttu-id="2c5c8-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="2c5c8-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2c5c8-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="2c5c8-110">Property GUID</span></span>

<span data-ttu-id="2c5c8-111">**КОДЕКАПИ \_ авенквидеокодедвидеоакцессунитсизе**</span><span class="sxs-lookup"><span data-stu-id="2c5c8-111">**CODECAPI\_AVEncVideoCodedVideoAccessUnitSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="2c5c8-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2c5c8-112">Property value</span></span>

<span data-ttu-id="2c5c8-113">Это свойство возвращается в виде диапазона значений.</span><span class="sxs-lookup"><span data-stu-id="2c5c8-113">This property is returned as a range of values.</span></span> <span data-ttu-id="2c5c8-114">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="2c5c8-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c5c8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2c5c8-115">Requirements</span></span>



| <span data-ttu-id="2c5c8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2c5c8-116">Requirement</span></span> | <span data-ttu-id="2c5c8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2c5c8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5c8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c5c8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c5c8-119">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2c5c8-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2c5c8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c5c8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c5c8-121">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="2c5c8-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2c5c8-122">Header</span><span class="sxs-lookup"><span data-stu-id="2c5c8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c5c8-123"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c5c8-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c5c8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c5c8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c5c8-125">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="2c5c8-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2c5c8-126">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="2c5c8-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




