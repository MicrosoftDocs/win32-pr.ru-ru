---
description: Позволяет подсистеме захвата использовать декодер с ограничениями на использование полей.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: Атрибут MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d858d4382b669621f6dc43cbfee77b62e9d1124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711560"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="490c2-103">\_ \_ \_ \_ \_ Фиелдофусе \_ разблокирование \_ атрибута MFT для декодера ядра записи MF</span><span class="sxs-lookup"><span data-stu-id="490c2-103">MF\_CAPTURE\_ENGINE\_DECODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="490c2-104">Позволяет подсистеме захвата использовать декодер с ограничениями на использование полей.</span><span class="sxs-lookup"><span data-stu-id="490c2-104">Enables the capture engine to use a decoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="490c2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="490c2-105">Data type</span></span>

<span data-ttu-id="490c2-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="490c2-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="490c2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="490c2-107">Remarks</span></span>

<span data-ttu-id="490c2-108">Значением этого атрибута является указатель на интерфейс [_ *имффиелдофусемфтунлокк* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , реализованный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="490c2-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="490c2-109">Реализация этого интерфейса в вызывающем объекте должна выполнять подтверждение с помощью декодера, как описано в разделе [ограничения использования](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="490c2-109">The caller's implementation of this interface is expected to perform a handshake with the decoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="490c2-110">Microsoft Media Foundation не определяет подтверждение, как правило, это влечет за собой некоторый вид криптографических обменов.</span><span class="sxs-lookup"><span data-stu-id="490c2-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="490c2-111">На внутреннем уровне подсистема отслеживания устанавливает указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) на декодер, установив атрибут [ \_ \_ \_ атрибута MFT фиелдофусе Unlock](mft-fieldofuse-unlock-attribute.md) для декодера.</span><span class="sxs-lookup"><span data-stu-id="490c2-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the decoder by setting the decoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="490c2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="490c2-112">Requirements</span></span>



| <span data-ttu-id="490c2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="490c2-113">Requirement</span></span> | <span data-ttu-id="490c2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="490c2-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="490c2-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="490c2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="490c2-116">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="490c2-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="490c2-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="490c2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="490c2-118">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="490c2-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="490c2-119">Header</span><span class="sxs-lookup"><span data-stu-id="490c2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="490c2-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="490c2-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="490c2-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="490c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="490c2-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="490c2-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="490c2-123">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="490c2-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="490c2-124">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="490c2-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




