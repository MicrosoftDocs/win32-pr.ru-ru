---
description: Содержит статистику сети для сетевого источника.
ms.assetid: 1948481b-febd-434b-a5dc-faef592ea0ed
title: Свойство MFNETSOURCE_STATISTICS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 822e9ae2e65170f3bf6e0f9ce065dd0ea5c62189a9a2b77fe2cd59beeb164248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738571"
---
# <a name="mfnetsource_statistics-property"></a>\_Свойство статистики мфнетсаурце

Содержит статистику сети для сетевого источника.

## <a name="data-type"></a>Тип данных

Различать см. раздел Примечания.

## <a name="remarks"></a>Remarks

Постоянная \_ Статистика мфнетсаурце определяет идентификатор GUID, используемый в сочетании с перечислением [**\_ \_ идентификаторов мфнетсаурце Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) для определения набора ключей свойств. Каждый ключ свойства в наборе имеет **fmtid** , равный \_ статистике мфнетсаурце, и **PID** , равный одному элементу перечисления. Дополнительные сведения см. в разделе [**мфнетсаурце \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Ведение журнала клиента](client-logging.md)
</dt> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




