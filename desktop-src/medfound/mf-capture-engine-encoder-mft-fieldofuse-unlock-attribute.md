---
description: Позволяет подсистеме захвата использовать кодировщик с ограничениями на использование полей.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: Атрибут MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a9466162ff5551ee155343800d938276823ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263635"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="e13f2-103">\_Запись о \_ кодировщике модуля записи MF \_ \_ \_ фиелдофусе \_ разблокировать \_ атрибут атрибута</span><span class="sxs-lookup"><span data-stu-id="e13f2-103">MF\_CAPTURE\_ENGINE\_ENCODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="e13f2-104">Позволяет подсистеме захвата использовать кодировщик с ограничениями на использование полей.</span><span class="sxs-lookup"><span data-stu-id="e13f2-104">Enables the capture engine to use an encoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="e13f2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e13f2-105">Data type</span></span>

<span data-ttu-id="e13f2-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="e13f2-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="e13f2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e13f2-107">Remarks</span></span>

<span data-ttu-id="e13f2-108">Значением этого атрибута является указатель на интерфейс [_ *имффиелдофусемфтунлокк* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , реализованный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="e13f2-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="e13f2-109">Реализация этого интерфейса в вызывающем объекте должна выполнять подтверждение с кодировщиком, как описано в разделе [ограничения использования](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="e13f2-109">The caller's implementation of this interface is expected to perform a handshake with the encoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="e13f2-110">Microsoft Media Foundation не определяет подтверждение, как правило, это влечет за собой некоторый вид криптографических обменов.</span><span class="sxs-lookup"><span data-stu-id="e13f2-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="e13f2-111">На внутреннем уровне подсистема отслеживания задает указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) на кодировщике, задавая атрибут [ \_ Фиелдофусе \_ Unlock \_](mft-fieldofuse-unlock-attribute.md) в файле MFT для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="e13f2-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the encoder by setting the encoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13f2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e13f2-112">Requirements</span></span>



| <span data-ttu-id="e13f2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e13f2-113">Requirement</span></span> | <span data-ttu-id="e13f2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e13f2-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13f2-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e13f2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e13f2-116">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e13f2-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="e13f2-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e13f2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e13f2-118">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e13f2-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e13f2-119">Header</span><span class="sxs-lookup"><span data-stu-id="e13f2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e13f2-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="e13f2-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13f2-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e13f2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13f2-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e13f2-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e13f2-123">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="e13f2-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="e13f2-124">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="e13f2-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




