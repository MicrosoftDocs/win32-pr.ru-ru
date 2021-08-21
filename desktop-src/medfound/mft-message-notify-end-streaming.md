---
description: Запрашивает преобразование Media Foundation (MFT) в эту потоковую передачу.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae36412a35dd142efab89f17827b1c9cb6475494ff88f8af800bd8fee65d456f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871968"
---
# <a name="mft_message_notify_end_streaming"></a>\_ \_ уведомление о \_ завершении \_ ПОТОКовой передачи сообщения MFT

Запрашивает преобразование Media Foundation (MFT) в эту потоковую передачу.

## <a name="message-parameter"></a>Параметр сообщения

Нет.

## <a name="remarks"></a>Remarks

Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Клиенту не требуется отправлять это сообщение, даже если клиент ранее отправил сообщение **MFT с \_ \_ уведомлением о \_ начале \_ потоковой передачи** .

### <a name="implementation"></a>Реализация

MFT может ответить на это сообщение, освобождая буферы и другие ресурсы. Таблица MFT не очищает входные данные или не сбрасывает типы носителей в ответ на это сообщение. MFT не требуется для ответа на это сообщение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_тип сообщения \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




