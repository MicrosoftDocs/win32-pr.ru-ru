---
description: Уведомляет о преобразовании Media Foundation (MFT), которое будет обработано первым образцом.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080437"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_тип сообщения \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




