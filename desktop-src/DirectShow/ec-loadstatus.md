---
description: Уведомляет о ходе выполнения приложения при открытии сетевого файла.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679810"
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

Это событие отправляется фильтром [чтения WM ASF](wm-asf-reader-filter.md) и устаревшим фильтром [источников Windows Media](windows-media-source-filter.md) . Первый параметр события имеет одно из следующих значений.



| Значение                        | Описание                                    |
|------------------------------|------------------------------------------------|
| \_лоадстатус \_ закрыто       | Фильтр источника закрыл файл.         |
| \_Подключение лоадстатус \_   | Фильтр источника подключается к серверу. |
| \_лоадстатус \_ лоадингдескр | Не используется.                                      |
| \_лоадстатус \_ лоадингмкаст | Не используется                                       |
| \_лоадстатус \_ расположение     | Фильтр источника наследует поиск запрошенных данных.  |
| \_открытая лоадстатус \_         | Фильтр источника открыл файл.         |
| \_лоадстатус \_ Открытие      | Фильтр источника открывает файл.         |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




