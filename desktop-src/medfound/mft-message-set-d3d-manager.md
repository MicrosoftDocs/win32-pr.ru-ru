---
description: Задает или очищает диспетчер устройств Direct3D для DirectX Video Акцерератион (ДКСВА).
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0e7ccbf9f28615b17e6acded6ecc932334b4fb0fa4a607d6fd6213ba2cd214
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848073"
---
# <a name="mft_message_set_d3d_manager"></a>\_ \_ Диспетчер D3D, набор сообщений \_ MFT \_

Задает или очищает [Диспетчер устройств Direct3D](direct3d-device-manager.md) для DirectX Video АКЦЕРЕРАТИОН (дксва).

## <a name="message-parameter"></a>Параметр сообщения

При начале потоковой передачи параметр *улпарам* содержит указатель **IUnknown** . MFT запросит этот указатель для интерфейса [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) для Direct3D 9 и интерфейса [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) для Direct3D 11. При остановке потоковой передачи *улпараметер* содержит значение **null**.

## <a name="remarks"></a>Remarks

Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Это сообщение относится только к преобразованиям видео. Клиент не должен отсылать это сообщение, если только MFT не возвращает **значение true** для атрибута, [**\_ \_ \_ совместимого с D3D SA**](mf-sa-d3d-aware-attribute.md) ([MF \_ SA D3D11, с \_ \_ учетом](mf-sa-d3d11-aware.md) Direct3D 11).

Не отправляйте это сообщение в MFT с несколькими аупутс.

### <a name="implementation"></a>Реализация

Файл MFT должен поддерживать это сообщение только в том случае, если в MFT используется ускорение видео DirectX для обработки видео или декодирования.

Если MFT поддерживает это сообщение, оно также должно реализовывать метод [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) и возвращать значение **true** для атрибута [**MF \_ SA с \_ \_ поддержкой D3D**](mf-sa-d3d-aware-attribute.md) (([MF \_ SA D3D11 с \_ \_ поддержкой](mf-sa-d3d11-aware.md) Direct3D 11). Этот атрибут информирует клиента о том, что клиент должен отправить сообщение **MFT \_ \_ \_ \_ диспетчера D3D** в MFT перед началом потоковой передачи.

Если таблица MFT не поддерживает это сообщение, она должна вернуть **E \_ Нотимпл** из [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage). Это исключение из общего правила, которое MFT может вернуть **S \_ ОК** из любого сообщения, которое она пропускает.

Дополнительные сведения см. в разделе [МФТС с поддержкой Direct3D](direct3d-aware-mfts.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[МФТС с поддержкой Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Поддержка ДКСВА 2,0 в Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Поддержка декодирования видео Direct3D 11 в Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**\_тип сообщения \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




