---
description: Следующие GUID поддерживают API-интерфейсы видео Direct3D 11.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: Идентификаторы GUID видео Direct3D 11 (D3d11. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d97a43285a59cf5196584b9be04fc36b02e5243f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072571"
---
# <a name="direct3d-11-video-guids"></a><span data-ttu-id="daae6-103">Идентификаторы GUID видео Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="daae6-103">Direct3D 11 Video GUIDs</span></span>

<span data-ttu-id="daae6-104">Следующие GUID поддерживают API-интерфейсы видео Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="daae6-104">The following GUIDs support Direct3D 11 Video APIs.</span></span>

<dl> <dt>

<span data-ttu-id="daae6-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_Защита D3D11 Key с \_ обменом данными \_ \_**</span><span class="sxs-lookup"><span data-stu-id="daae6-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="daae6-106">Указывает, что декодер будет принимать данные из компонента DRM на основе оборудования</span><span class="sxs-lookup"><span data-stu-id="daae6-106">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="daae6-107">**D3D11 \_ \_ \_ \_ Защиту ключа** можно указать в параметре *Пкэйексчанжетипе* функции [**ID3D11VideoDevice:: Креатекриптосессион**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) , чтобы указать, что интерфейс [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) будет использоваться исключительно для обмена данными между компонентом DRM пользовательского режима и средой безопасного выполнения.</span><span class="sxs-lookup"><span data-stu-id="daae6-107">**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION** can be specified in the *pKeyExchangeType* parameter of the [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) function to indicate that the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) interface will be used purely for communication between a user mode DRM component and the secure execution environment.</span></span>

<span data-ttu-id="daae6-108">Если указан этот GUID, не следует вызывать следующие методы:</span><span class="sxs-lookup"><span data-stu-id="daae6-108">When this GUID is specified, the following methods should not be called:</span></span>

-   [<span data-ttu-id="daae6-109">**ID3D11CryptoSession:: Жетцертификатесизе**</span><span class="sxs-lookup"><span data-stu-id="daae6-109">**ID3D11CryptoSession::GetCertificateSize**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [<span data-ttu-id="daae6-110">**ID3D11CryptoSession:: Certificate**</span><span class="sxs-lookup"><span data-stu-id="daae6-110">**ID3D11CryptoSession::GetCertificate**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [<span data-ttu-id="daae6-111">**ID3D11VideoContext:: Енкриптионблт**</span><span class="sxs-lookup"><span data-stu-id="daae6-111">**ID3D11VideoContext::EncryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [<span data-ttu-id="daae6-112">**ID3D11VideoContext::D Екриптионблт**</span><span class="sxs-lookup"><span data-stu-id="daae6-112">**ID3D11VideoContext::DecryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [<span data-ttu-id="daae6-113">**ID3D11VideoContext:: Стартсессионкэйрефреш**</span><span class="sxs-lookup"><span data-stu-id="daae6-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [<span data-ttu-id="daae6-114">**ID3D11VideoContext:: Финишсессионкэйрефреш**</span><span class="sxs-lookup"><span data-stu-id="daae6-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [<span data-ttu-id="daae6-115">**ID3D11VideoContext:: Жетенкриптионблткэй**</span><span class="sxs-lookup"><span data-stu-id="daae6-115">**ID3D11VideoContext::GetEncryptionBltKey**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span data-ttu-id="daae6-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ декодер \_ шифрования \_ HW \_ CENC**</span><span class="sxs-lookup"><span data-stu-id="daae6-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11\_DECODER\_ENCRYPTION\_HW\_CENC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="daae6-117">Указывает, что декодер будет принимать данные из компонента DRM на основе оборудования</span><span class="sxs-lookup"><span data-stu-id="daae6-117">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="daae6-118">Установка этого идентификатора GUID в **гуидконфигбитстреаменкриптион** -члене [**структуры \_ \_ \_ конфигурации видеодекодера D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) , передаваемой в API [**ID3D11VideoDevice:: креатевидеодекодер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) , указывает, что следующие параметры будут переданы в вызов [**ID3D11VideoDevice::D екодербегинфраме**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :</span><span class="sxs-lookup"><span data-stu-id="daae6-118">Setting this GUID in the **guidConfigBitstreamEncryption** member of the [**D3D11\_VIDEO\_DECODER\_CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) structure passed to the [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API indicates that the following parameters will be passed in the [**ID3D11VideoDevice::DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) call:</span></span>



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daae6-119">*контенткэйсизе*</span><span class="sxs-lookup"><span data-stu-id="daae6-119">*ContentKeySize*</span></span> | <span data-ttu-id="daae6-120">Содержит размер структуры [**\_ \_ \_ \_ \_ \_ сеанса шифрования D3D11ного видеодекодера**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .</span><span class="sxs-lookup"><span data-stu-id="daae6-120">Contains the size of the [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) structure.</span></span>                                                                                                  |
| <span data-ttu-id="daae6-121">*пконтенткэй*</span><span class="sxs-lookup"><span data-stu-id="daae6-121">*pContentKey*</span></span>    | <span data-ttu-id="daae6-122">Указатель на [**\_ \_ \_ \_ \_ \_ сеанс шифрования D3D11 Video декодера**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) , предоставляющий [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) и ключевые сведения, необходимые для расшифровки кадра.</span><span class="sxs-lookup"><span data-stu-id="daae6-122">A pointer to a [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) providing the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) and the key information needed to decrypt the frame.</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="daae6-123">Требования</span><span class="sxs-lookup"><span data-stu-id="daae6-123">Requirements</span></span>



| <span data-ttu-id="daae6-124">Требование</span><span class="sxs-lookup"><span data-stu-id="daae6-124">Requirement</span></span> | <span data-ttu-id="daae6-125">Значение</span><span class="sxs-lookup"><span data-stu-id="daae6-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="daae6-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="daae6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="daae6-127">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="daae6-127">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="daae6-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="daae6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="daae6-129">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="daae6-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="daae6-130">Header</span><span class="sxs-lookup"><span data-stu-id="daae6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="daae6-131"><dt>D3d11. h</dt></span><span class="sxs-lookup"><span data-stu-id="daae6-131"><dt>D3d11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daae6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="daae6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daae6-133">API-интерфейсы видео Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="daae6-133">Direct3D 11 Video APIs</span></span>](direct3d-11-video-apis.md)
</dt> </dl>

 

 




