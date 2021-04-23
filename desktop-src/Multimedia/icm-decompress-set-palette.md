---
title: Сообщение ICM_DECOMPRESS_SET_PALETTE (VFW. h)
description: Сообщение ICM \_ распаковка \_ Установка \_ палитры указывает палитру для драйвера распаковки видео, который будет использоваться при распаковке в формат, использующий палитру. Это сообщение можно отправить явно или с помощью макроса Икдекомпресссетпалетте.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- ICM_DECOMPRESS_SET_PALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672799"
---
# <a name="icm_decompress_set_palette-message"></a><span data-ttu-id="0ff6d-105">\_Сообщение о настройке распаковки ICM \_ \_</span><span class="sxs-lookup"><span data-stu-id="0ff6d-105">ICM\_DECOMPRESS\_SET\_PALETTE message</span></span>

<span data-ttu-id="0ff6d-106">Сообщение **ICM \_ распаковка \_ Установка \_ палитры** указывает палитру для драйвера распаковки видео, который будет использоваться при распаковке в формат, использующий палитру.</span><span class="sxs-lookup"><span data-stu-id="0ff6d-106">The **ICM\_DECOMPRESS\_SET\_PALETTE** message specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette.</span></span> <span data-ttu-id="0ff6d-107">Это сообщение можно отправить явно или с помощью макроса [**икдекомпресссетпалетте**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) .</span><span class="sxs-lookup"><span data-stu-id="0ff6d-107">You can send this message explicitly or by using the [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="0ff6d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ff6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff6d-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*лпбипалетте*</span><span class="sxs-lookup"><span data-stu-id="0ff6d-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span></span>
</dt> <dd>

<span data-ttu-id="0ff6d-110">Указатель на структуру [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) , таблица цветов которой содержит цвета, которые должны использоваться, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="0ff6d-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure whose color table contains the colors that should be used if possible.</span></span> <span data-ttu-id="0ff6d-111">Можно задать нуль, чтобы использовать набор выходных цветов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ff6d-111">You can specify zero to use the default set of output colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff6d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ff6d-112">Return Value</span></span>

<span data-ttu-id="0ff6d-113">Возвращает ИЦЕРР \_ ОК, если драйвер распаковки может точно распаковать изображения в предлагаемую палитру, используя набор цветов, упорядоченных в палитре.</span><span class="sxs-lookup"><span data-stu-id="0ff6d-113">Returns ICERR\_OK if the decompression driver can precisely decompress images to the suggested palette using the set of colors as they are arranged in the palette.</span></span> <span data-ttu-id="0ff6d-114">\_В противном случае ВОЗВРАЩАЕТ ицерр.</span><span class="sxs-lookup"><span data-stu-id="0ff6d-114">Returns ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff6d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ff6d-115">Remarks</span></span>

<span data-ttu-id="0ff6d-116">Это сообщение не должно влиять на уже выполняющееся распаковку; Вместо этого цвета, передаваемые с помощью этого сообщения, должны возвращаться в ответ на будущее [**ICM \_ unуплотнение \_ Get \_ Format**](icm-decompress-get-format.md) и [**ICM \_ unсжимать \_ Получение сообщений \_ палитры**](icm-decompress-get-palette.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff6d-116">This message should not affect decompression already in progress; rather, colors passed using this message should be returned in response to future [**ICM\_DECOMPRESS\_GET\_FORMAT**](icm-decompress-get-format.md) and [**ICM\_DECOMPRESS\_GET\_PALETTE**](icm-decompress-get-palette.md) messages.</span></span> <span data-ttu-id="0ff6d-117">Цвета отправляются обратно в драйвер распаковки в будущем сообщении [**о \_ \_ начале распаковки ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff6d-117">Colors are sent back to the decompression driver in a future [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="0ff6d-118">Это сообщение используется в основном, когда драйвер распаковывает изображения на экран, а другое приложение, использующее палитру, находится на переднем плане, представляя драйвер распаковки адаптироваться к внешнему набору цветов.</span><span class="sxs-lookup"><span data-stu-id="0ff6d-118">This message is used primarily when a driver decompresses images to the screen and another application that uses a palette is in the foreground, forcing the decompression driver to adapt to a foreign set of colors.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff6d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0ff6d-119">Requirements</span></span>



| <span data-ttu-id="0ff6d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0ff6d-120">Requirement</span></span> | <span data-ttu-id="0ff6d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0ff6d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0ff6d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ff6d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0ff6d-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0ff6d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0ff6d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ff6d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0ff6d-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0ff6d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0ff6d-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0ff6d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ff6d-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ff6d-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ff6d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ff6d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff6d-129">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="0ff6d-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0ff6d-130">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="0ff6d-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

