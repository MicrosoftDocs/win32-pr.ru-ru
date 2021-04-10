---
description: Содержит статистику сети для сетевого источника.
ms.assetid: 1948481b-febd-434b-a5dc-faef592ea0ed
title: Свойство MFNETSOURCE_STATISTICS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a09e6c0fe4697595ff3600135327ba093350e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143081"
---
# <a name="mfnetsource_statistics-property"></a>\_Свойство статистики мфнетсаурце

Содержит статистику сети для сетевого источника.

## <a name="data-type"></a>Тип данных

Различать см. раздел Примечания.

## <a name="remarks"></a>Комментарии

Постоянная \_ Статистика мфнетсаурце определяет идентификатор GUID, используемый в сочетании с перечислением [**\_ \_ идентификаторов мфнетсаурце Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) для определения набора ключей свойств. Каждый ключ свойства в наборе имеет **fmtid** , равный \_ статистике мфнетсаурце, и **PID** , равный одному элементу перечисления. Дополнительные сведения см. в разделе [**мфнетсаурце \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Ведение журнала клиента](client-logging.md)
</dt> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




