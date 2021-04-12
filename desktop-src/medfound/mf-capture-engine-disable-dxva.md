---
description: Указывает, использует ли подсистема захвата ускорение видео DirectX (ДКСВА) для декодирования видео.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: Атрибут MF_CAPTURE_ENGINE_DISABLE_DXVA (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343935"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a><span data-ttu-id="bedba-103">\_Ключ записи \_ MF \_ Отключить \_ атрибут дксва</span><span class="sxs-lookup"><span data-stu-id="bedba-103">MF\_CAPTURE\_ENGINE\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="bedba-104">Указывает, использует ли подсистема захвата ускорение видео DirectX (ДКСВА) для декодирования видео.</span><span class="sxs-lookup"><span data-stu-id="bedba-104">Specifies whether the capture engine uses DirectX Video Acceleration (DXVA) for video decoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="bedba-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bedba-105">Data type</span></span>

<span data-ttu-id="bedba-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="bedba-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bedba-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bedba-107">Remarks</span></span>

<span data-ttu-id="bedba-108">Этот атрибут применяется, если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="bedba-108">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="bedba-109">Подсистема отслеживания декодирует сжатый поток видео с устройства записи (например, если устройство записи выводит H. 264).</span><span class="sxs-lookup"><span data-stu-id="bedba-109">The capture engine decodes a compressed video stream from the capture device (for example, if the capture device outputs H.264 video).</span></span>
-   <span data-ttu-id="bedba-110">Видеодекодер поддерживает декодирование с аппаратным ускорением с помощью ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="bedba-110">The video decoder supports hardware-accelerated decoding using DXVA.</span></span>
-   <span data-ttu-id="bedba-111">Приложение использует атрибут [ \_ \_ \_ \_ диспетчера D3D подсистемы захвата MF](mf-capture-engine-d3d-manager.md) для установки диспетчер устройств DXGI в подсистеме записи.</span><span class="sxs-lookup"><span data-stu-id="bedba-111">The application uses the [MF\_CAPTURE\_ENGINE\_D3D\_MANAGER](mf-capture-engine-d3d-manager.md) attribute to set the DXGI Device Manager on the capture engine.</span></span>

<span data-ttu-id="bedba-112">В противном случае этот атрибут игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bedba-112">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="bedba-113">Этот атрибут позволяет приложению отключить ДКСВА, продолжая декодироваться на поверхности Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bedba-113">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="bedba-114">Значение этого атрибута по умолчанию равно **false**, означающее, что при наличии включен декодирование дксва.</span><span class="sxs-lookup"><span data-stu-id="bedba-114">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="bedba-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bedba-115">Requirements</span></span>



| <span data-ttu-id="bedba-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bedba-116">Requirement</span></span> | <span data-ttu-id="bedba-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bedba-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bedba-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bedba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bedba-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bedba-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="bedba-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bedba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bedba-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bedba-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bedba-122">Header</span><span class="sxs-lookup"><span data-stu-id="bedba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bedba-123"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="bedba-123"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bedba-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bedba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bedba-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bedba-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bedba-126">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="bedba-126">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="bedba-127">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="bedba-127">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




