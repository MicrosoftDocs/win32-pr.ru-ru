---
description: Система передает \_ событие ДБТ куеричанжеконфиг Device, чтобы запросить разрешение на изменение текущей конфигурации (закрепление или Отстыковка). Любое приложение может отклонить этот запрос и отменить изменение.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: Событие DBT_QUERYCHANGECONFIG (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e9c222fdc29f635263b45b5fd7e54ee229a33d7dee1ff31cd1e3072bfe6e84f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318424"
---
# <a name="dbt_querychangeconfig-event"></a>\_Событие ДБТ куеричанжеконфиг

Система передает \_ событие ДБТ куеричанжеконфиг Device, чтобы запросить разрешение на изменение текущей конфигурации (закрепление или Отстыковка). Любое приложение может отклонить этот запрос и отменить изменение.

Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* , установленным в значение ДБТ \_ куеричанжеконфиг и *lParam* , равным нулю.


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

Задайте для параметра значение ДБТ \_ куеричанжеконфиг.

</dd> <dt>

*lParam* 
</dt> <dd>

Задайте нулевое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , чтобы предоставить разрешение на изменение конфигурации.

Верните ШИРОКОВЕЩАТЕЛЬный \_ запрос \_ Deny, чтобы запретить разрешение на изменение конфигурации.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>ДБТ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События устройства](device-events.md)
</dt> <dt>

[События управления устройствами](device-management-events.md)
</dt> <dt>

[**WM \_ девицечанже**](wm-devicechange.md)
</dt> </dl>

 

 




