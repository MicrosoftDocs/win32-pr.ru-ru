---
description: Уведомляет Media Foundation преобразование (MFT), которое начинается потоковая передача.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263514"
---
# <a name="mft_message_notify_begin_streaming"></a>\_ \_ уведомление о \_ начале \_ ПОТОКовой передачи сообщения MFT

Уведомляет Media Foundation преобразование (MFT), которое начинается потоковая передача.

## <a name="message-parameter"></a>Параметр сообщения

Нет.

## <a name="remarks"></a>Remarks

Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Клиенту не требуется отсылать это сообщение. Если клиент отправляет это сообщение, он должен сделать это после установки всех типов носителей в MFT и перед вызовом метода [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). MFT может ответить путем выделения буферов или других ресурсов. Если клиент не отправляет это сообщение, MFT выделяет ресурсы при первом вызове **ProcessInput**. Поэтому отправка этого сообщения может уменьшить начальную задержку при запуске потоковой передачи.

### <a name="implementation"></a>Реализация

MFT не требуется для ответа на это сообщение.

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

 

 




