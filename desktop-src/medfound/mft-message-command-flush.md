---
description: Запрашивает преобразование Media Foundation (MFT) для сброса всех хранящихся данных.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811614"
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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_тип сообщения \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




