---
description: Система передает \_ событие ДБТ девицеремовепендинг Device, когда устройство или носитель удаляется и больше не доступны для использования.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: Событие DBT_DEVICEREMOVEPENDING (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141514"
---
# <a name="dbt_deviceremovepending-event"></a>\_Событие ДБТ девицеремовепендинг

Система передает \_ событие ДБТ девицеремовепендинг Device, когда устройство или носитель удаляется и больше не доступны для использования.

Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* Set ДБТ \_ девицеремовепендинг и *lParam* Set, как описано ниже.


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

Задайте для параметра значение ДБТ \_ девицеремовепендинг.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру, идентифицирующую устройство. Структура состоит из независимого от событий заголовка, за которым следуют элементы, зависящие от события, которые описывают устройство. Чтобы использовать эту структуру, рассматривайте структуру как [**\_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -структуру для разработки вещания, а затем проверьте ее член **дбч \_ типа устройства** , чтобы определить тип устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true**.

## <a name="remarks"></a>Комментарии

Система может транслировать \_ сообщение ДБТ девицеремовепендинг, не отправляя соответствующее сообщение [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) . В таких случаях приложения и драйверы должны быть восстановлены после потери устройства, как лучше.

## <a name="examples"></a>Примеры

Пример см. в разделе [Обработка запроса на удаление устройства](processing-a-request-to-remove-a-device.md).

## <a name="requirements"></a>Требования



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

[**расвещание для разработки в \_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ девицечанже**](wm-devicechange.md)
</dt> </dl>

 

 




