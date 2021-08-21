---
description: Уведомляет о преобразовании Media Foundation (MFT), которое будет обработано первым образцом.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ed40d9d3514dfa6223d4e20f2eb411caec497e16f2e97c456f16e14442c407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973033"
---
# <a name="mft_message_notify_start_of_stream"></a>\_ \_ уведомление о \_ начале \_ потока в \_ сообщении MFT

Уведомляет о преобразовании Media Foundation (MFT), которое будет обработано первым образцом.

## <a name="message-parameter"></a>Параметр сообщения

Нет.

## <a name="remarks"></a>Remarks

Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Для синхронных МФТС необязательно отправить это сообщение.

Для асинхронного МФТС клиент должен отправить это сообщение.

### <a name="implementation"></a>Реализация

Синхронная MFT не требуется для ответа на сообщение.

Асинхронная Таблица MFT должна реализовывать это сообщение, как описано в статье [асинхронный МФТС](asynchronous-mfts.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_тип сообщения \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




