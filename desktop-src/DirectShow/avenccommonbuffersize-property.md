---
description: Указывает размер буфера, используемого во время кодирования. Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Свойство Авенккоммонбуфферсизе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140486"
---
# <a name="avenccommonbuffersize-property"></a><span data-ttu-id="7dc28-104">Авенккоммонбуфферсизе, свойство</span><span class="sxs-lookup"><span data-stu-id="7dc28-104">AVEncCommonBufferSize property</span></span>

<span data-ttu-id="7dc28-105">Указывает размер буфера, используемого во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="7dc28-105">Specifies the size of the buffer used during encoding.</span></span> <span data-ttu-id="7dc28-106">Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).</span><span class="sxs-lookup"><span data-stu-id="7dc28-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="7dc28-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7dc28-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7dc28-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7dc28-108">Data type</span></span>

<span data-ttu-id="7dc28-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="7dc28-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7dc28-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="7dc28-110">Property GUID</span></span>

<span data-ttu-id="7dc28-111">**КОДЕКАПИ \_ авенккоммонбуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="7dc28-111">**CODECAPI\_AVEncCommonBufferSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="7dc28-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7dc28-112">Property value</span></span>

<span data-ttu-id="7dc28-113">Это свойство имеет линейный Диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="7dc28-113">This property has a linear range of values.</span></span> <span data-ttu-id="7dc28-114">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="7dc28-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span> <span data-ttu-id="7dc28-115">Диапазоны параметров не поддерживаются для кодировщиков камеры H. 264 УВК 1,5.</span><span class="sxs-lookup"><span data-stu-id="7dc28-115">Parameter ranges are not supported for H.264 UVC 1.5 camera encoders.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc28-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7dc28-116">Remarks</span></span>

<span data-ttu-id="7dc28-117">Для некоторых форматов видео размер буфера указывается в битах, а для других — в байтах.</span><span class="sxs-lookup"><span data-stu-id="7dc28-117">For some video formats the buffer size is specified in bits and for others it is specified in bytes.</span></span> <span data-ttu-id="7dc28-118">Конкретные сведения см. в примечаниях ниже.</span><span class="sxs-lookup"><span data-stu-id="7dc28-118">See the remarks below for specific information.</span></span>

<span data-ttu-id="7dc28-119">Для видео в формате MPEG это свойство определяет размер буфера средства проверки буфера видео (ВБВ).</span><span class="sxs-lookup"><span data-stu-id="7dc28-119">For MPEG video, this property defines the video buffer verifier (VBV) buffer size.</span></span> <span data-ttu-id="7dc28-120">Размер буфера находится в битах.</span><span class="sxs-lookup"><span data-stu-id="7dc28-120">The size of the buffer is in bits.</span></span>

<span data-ttu-id="7dc28-121">Для видео H. 264 и Windows Media Video свойство определяет гипотетический размер декодера ссылок (обнаружения домашней области).</span><span class="sxs-lookup"><span data-stu-id="7dc28-121">For H.264 video and Windows Media Video, the property defines the hypothetical reference decoder (HRD) size.</span></span> <span data-ttu-id="7dc28-122">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="7dc28-122">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="7dc28-123">Для камер с кодировкой УВК 1,5 H264 Single bitrate значение КПБ, отправляемое кодировщику камеры, должно быть согласовано с 16-битным.</span><span class="sxs-lookup"><span data-stu-id="7dc28-123">For UVC 1.5 H264 encoding cameras, the CPB value sent to the camera encoder must be 16-bit aligned.</span></span> <span data-ttu-id="7dc28-124">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="7dc28-124">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="7dc28-125">Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="7dc28-125">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc28-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7dc28-126">Requirements</span></span>



| <span data-ttu-id="7dc28-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7dc28-127">Requirement</span></span> | <span data-ttu-id="7dc28-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7dc28-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc28-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dc28-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc28-130">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7dc28-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7dc28-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dc28-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc28-132">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="7dc28-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7dc28-133">Header</span><span class="sxs-lookup"><span data-stu-id="7dc28-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc28-134"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc28-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc28-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7dc28-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc28-136">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="7dc28-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7dc28-137">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="7dc28-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

