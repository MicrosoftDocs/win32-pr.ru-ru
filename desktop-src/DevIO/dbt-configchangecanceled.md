---
description: Система передает \_ событие ДБТ конфигчанжеканцелед Device, когда запрос на изменение текущей конфигурации (закрепления или отстыковки) был отменен.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: Событие DBT_CONFIGCHANGECANCELED (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624144ccd5a87d983d453c8d6a3c0667376c2a1b9340bba83f229a29882bffe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874544"
---
# <a name="dbt_configchangecanceled-event"></a>\_Событие ДБТ конфигчанжеканцелед

Система передает \_ событие ДБТ конфигчанжеканцелед Device, когда запрос на изменение текущей конфигурации (закрепления или отстыковки) был отменен.

Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* , установленным в значение ДБТ \_ конфигчанжеканцелед и *lParam* , равным нулю.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Дескриптор окна.

</dd> <dt>

*Uiacp* 
</dt> <dd>

Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Задайте для параметра значение ДБТ \_ конфигчанжеканцелед.

</dd> <dt>

*lParam* 
</dt> <dd>

Задайте нулевое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>ДБТ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[События устройства](device-events.md)
</dt> <dt>

[События управления устройствами](device-management-events.md)
</dt> <dt>

[**WM \_ девицечанже**](wm-devicechange.md)
</dt> </dl>

 

 




