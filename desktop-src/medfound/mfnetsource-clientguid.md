---
description: Уникальный идентификатор, по которому сервер идентифицирует клиента.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: Свойство MFNETSOURCE_CLIENTGUID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9585f5ac9cd69148272cb986746f6849aad4c3aa048b46baf2f75aeaba77c092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738993"
---
# <a name="mfnetsource_clientguid-property"></a>МФНЕТСАУРЦЕ \_ клиентгуид, свойство

Уникальный идентификатор, по которому сервер идентифицирует клиента.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**GUID**

VT \_ CLSID

**пууид**



## <a name="remarks"></a>Remarks

Константа **\_ клиентгуид мфнетсаурце** определяет идентификатор GUID для ключа свойства. Идентификатор свойства (PID) равен нулю. Чтобы задать это свойство в сетевом источнике, передайте указатель **ипропертисторе** в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

Если параметр не задан или задан как **GUID \_ NULL**, Microsoft Media Foundation создает анонимный идентификатор GUID для сеанса, гарантирующий конфиденциальность пользователя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




