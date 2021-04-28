---
description: MFT_MESSAGE_COMMAND_FLUSH — запрашивает преобразование Media Foundation (MFT) для сброса всех хранящихся данных.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092742"
---
# <a name="mft_message_command_flush"></a>\_ \_ Очистка команды сообщения \_ MFT

Запрашивает преобразование Media Foundation (MFT) для сброса всех хранящихся данных.

## <a name="message-parameter"></a>Параметр сообщения

Нет.

## <a name="remarks"></a>Remarks

Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

После отправки сообщения MFT может принимать новые входные образцы. Текущие типы носителей не являются недействительными.

### <a name="implementation"></a>Реализация

Все МФТС должны реализовывать это сообщение. При получении этого сообщения MFT должно удалить все примеры мультимедиа, которые он удерживает.

[Асинхронный МФТС](asynchronous-mfts.md): MFT не отправляет другое событие [метрансформнидинпут](metransformneedinput.md) , пока оно не получит [**\_ сообщение \_ MFT \_ о \_ начале \_ потока**](mft-message-notify-start-of-stream.md) сообщения от клиента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_тип сообщения \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




