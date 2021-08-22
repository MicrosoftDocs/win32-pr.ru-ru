---
description: Уведомляет о ходе выполнения приложения при открытии сетевого файла.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499f05a26f3fa1387347929f5c14a64b1f440a53ed9b5fd17830d582fb640c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015942"
---
# <a name="ec_loadstatus"></a>EC \_ лоадстатус

Уведомляет о ходе выполнения приложения при открытии сетевого файла.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Код состояния. См. заметки.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

фильтр [чтения WM ASF](wm-asf-reader-filter.md) и фильтр [источника Windows носителя](windows-media-source-filter.md) прежних версий отправляют это событие. Первый параметр события имеет одно из следующих значений.



| Значение                        | Описание                                    |
|------------------------------|------------------------------------------------|
| \_лоадстатус \_ закрыто       | Фильтр источника закрыл файл.         |
| \_Подключение лоадстатус \_   | Фильтр источника подключается к серверу. |
| \_лоадстатус \_ лоадингдескр | Не используется.                                      |
| \_лоадстатус \_ лоадингмкаст | Не используется                                       |
| \_лоадстатус \_ расположение     | Фильтр источника наследует поиск запрошенных данных.  |
| \_открытая лоадстатус \_         | Фильтр источника открыл файл.         |
| \_лоадстатус \_ Открытие      | Фильтр источника открывает файл.         |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




