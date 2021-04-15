---
description: Запрашивает преобразование Media Foundation (MFT) в эту потоковую передачу.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543911"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_тип сообщения \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




