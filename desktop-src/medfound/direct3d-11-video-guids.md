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
# <a name="direct3d-11-video-guids"></a>Идентификаторы GUID видео Direct3D 11

Следующие GUID поддерживают API-интерфейсы видео Direct3D 11.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_Защита D3D11 Key с \_ обменом данными \_ \_**
</dt> <dd> <dl> <dt>



Указывает, что декодер будет принимать данные из компонента DRM на основе оборудования

**D3D11 \_ \_ \_ \_ Защиту ключа** можно указать в параметре *Пкэйексчанжетипе* функции [**ID3D11VideoDevice:: Креатекриптосессион**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) , чтобы указать, что интерфейс [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) будет использоваться исключительно для обмена данными между компонентом DRM пользовательского режима и средой безопасного выполнения.

Если указан этот GUID, не следует вызывать следующие методы:

-   [**ID3D11CryptoSession:: Жетцертификатесизе**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession:: Certificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext:: Енкриптионблт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext::D Екриптионблт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext:: Стартсессионкэйрефреш**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext:: Финишсессионкэйрефреш**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext:: Жетенкриптионблткэй**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ декодер \_ шифрования \_ HW \_ CENC**
</dt> <dd> <dl> <dt>



Указывает, что декодер будет принимать данные из компонента DRM на основе оборудования

Установка этого идентификатора GUID в **гуидконфигбитстреаменкриптион** -члене [**структуры \_ \_ \_ конфигурации видеодекодера D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) , передаваемой в API [**ID3D11VideoDevice:: креатевидеодекодер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) , указывает, что следующие параметры будут переданы в вызов [**ID3D11VideoDevice::D екодербегинфраме**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *контенткэйсизе* | Содержит размер структуры [**\_ \_ \_ \_ \_ \_ сеанса шифрования D3D11ного видеодекодера**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .                                                                                                  |
| *пконтенткэй*    | Указатель на [**\_ \_ \_ \_ \_ \_ сеанс шифрования D3D11 Video декодера**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) , предоставляющий [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) и ключевые сведения, необходимые для расшифровки кадра. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                               |
| Header<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[API-интерфейсы видео Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




