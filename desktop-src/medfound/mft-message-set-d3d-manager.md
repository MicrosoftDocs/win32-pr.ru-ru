---
description: Задает или очищает диспетчер устройств Direct3D для DirectX Video Акцерератион (ДКСВА).
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8ecb5db474935bb25138a960b6df1c2109c16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711695"
---
# <a name="mft_message_set_d3d_manager"></a><span data-ttu-id="2f4bb-103">\_ \_ Диспетчер D3D, набор сообщений \_ MFT \_</span><span class="sxs-lookup"><span data-stu-id="2f4bb-103">MFT\_MESSAGE\_SET\_D3D\_MANAGER</span></span>

<span data-ttu-id="2f4bb-104">Задает или очищает [Диспетчер устройств Direct3D](direct3d-device-manager.md) для DirectX Video АКЦЕРЕРАТИОН (дксва).</span><span class="sxs-lookup"><span data-stu-id="2f4bb-104">Sets or clears the [Direct3D Device Manager](direct3d-device-manager.md) for DirectX Video Accereration (DXVA).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="2f4bb-105">Параметр сообщения</span><span class="sxs-lookup"><span data-stu-id="2f4bb-105">Message Parameter</span></span>

<span data-ttu-id="2f4bb-106">При начале потоковой передачи параметр *улпарам* содержит указатель **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="2f4bb-106">When streaming begins, the *ulParam* parameter contains an **IUnknown** pointer.</span></span> <span data-ttu-id="2f4bb-107">MFT запросит этот указатель для интерфейса [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) для Direct3D 9 и интерфейса [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) для Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="2f4bb-107">The MFT will query this pointer for the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface for Direct3D 9 and the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface for Direct3D 11.</span></span> <span data-ttu-id="2f4bb-108">При остановке потоковой передачи *улпараметер* содержит значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2f4bb-108">When streaming stops, the *ulParameter* contains the value **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f4bb-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f4bb-109">Remarks</span></span>

<span data-ttu-id="2f4bb-110">Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="2f4bb-110">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="2f4bb-111">Это сообщение относится только к преобразованиям видео.</span><span class="sxs-lookup"><span data-stu-id="2f4bb-111">This message applies only to video transforms.</span></span> <span data-ttu-id="2f4bb-112">Клиент не должен отсылать это сообщение, если только MFT не возвращает **значение true** для атрибута, [**\_ \_ \_ совместимого с D3D SA**](mf-sa-d3d-aware-attribute.md) ([MF \_ SA D3D11, с \_ \_ учетом](mf-sa-d3d11-aware.md) Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="2f4bb-112">The client should not send this message unless the MFT returns **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute ([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span>

<span data-ttu-id="2f4bb-113">Не отправляйте это сообщение в MFT с несколькими аупутс.</span><span class="sxs-lookup"><span data-stu-id="2f4bb-113">Do not send this message to an MFT with multiple ouputs.</span></span>

### <a name="implementation"></a><span data-ttu-id="2f4bb-114">Реализация</span><span class="sxs-lookup"><span data-stu-id="2f4bb-114">Implementation</span></span>

<span data-ttu-id="2f4bb-115">Файл MFT должен поддерживать это сообщение только в том случае, если в MFT используется ускорение видео DirectX для обработки видео или декодирования.</span><span class="sxs-lookup"><span data-stu-id="2f4bb-115">An MFT should support this message only if the MFT uses DirectX Video Acceleration for video processing or decoding.</span></span>

<span data-ttu-id="2f4bb-116">Если MFT поддерживает это сообщение, оно также должно реализовывать метод [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) и возвращать значение **true** для атрибута [**MF \_ SA с \_ \_ поддержкой D3D**](mf-sa-d3d-aware-attribute.md) (([MF \_ SA D3D11 с \_ \_ поддержкой](mf-sa-d3d11-aware.md) Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="2f4bb-116">If an MFT supports this message, it should also implement the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method and return the value **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute (([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span> <span data-ttu-id="2f4bb-117">Этот атрибут информирует клиента о том, что клиент должен отправить сообщение **MFT \_ \_ \_ \_ диспетчера D3D** в MFT перед началом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="2f4bb-117">This attribute informs the client that the client should send the **MFT\_MESSAGE\_SET\_D3D\_MANAGER** message to the MFT before streaming begins.</span></span>

<span data-ttu-id="2f4bb-118">Если таблица MFT не поддерживает это сообщение, она должна вернуть **E \_ Нотимпл** из [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="2f4bb-118">If an MFT does not support this message, it should return **E\_NOTIMPL** from [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span> <span data-ttu-id="2f4bb-119">Это исключение из общего правила, которое MFT может вернуть **S \_ ОК** из любого сообщения, которое она пропускает.</span><span class="sxs-lookup"><span data-stu-id="2f4bb-119">This is an exception to the general rule that an MFT can return **S\_OK** from any message it ignores.</span></span>

<span data-ttu-id="2f4bb-120">Дополнительные сведения см. в разделе [МФТС с поддержкой Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="2f4bb-120">For more information, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f4bb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2f4bb-121">Requirements</span></span>



| <span data-ttu-id="2f4bb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2f4bb-122">Requirement</span></span> | <span data-ttu-id="2f4bb-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2f4bb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4bb-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f4bb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2f4bb-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f4bb-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2f4bb-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f4bb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2f4bb-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f4bb-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2f4bb-128">Header</span><span class="sxs-lookup"><span data-stu-id="2f4bb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f4bb-129"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f4bb-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f4bb-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f4bb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4bb-131">МФТС с поддержкой Direct3D</span><span class="sxs-lookup"><span data-stu-id="2f4bb-131">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="2f4bb-132">Поддержка ДКСВА 2,0 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f4bb-132">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="2f4bb-133">Поддержка декодирования видео Direct3D 11 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f4bb-133">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="2f4bb-134">**\_тип сообщения \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-134">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




