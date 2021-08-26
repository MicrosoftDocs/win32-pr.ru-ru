---
description: '\_Событие устройства ДБТ пользователяопределенные определяет определяемое пользователем событие.'
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: Событие DBT_USERDEFINED (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49eca726ea9c4336a36f30872ad068e45062a67189192154374d5d5b21e578ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103874"
---
# <a name="dbt_userdefined-event"></a>\_Событие ДБТ пользователяопределенные

\_Событие устройства ДБТ пользователяопределенные определяет определяемое пользователем событие.

Для вещания этого события устройства вызовите функцию [**броадкастсистеммессаже**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) с сообщением [**WM \_ девицечанже**](wm-devicechange.md) . Присвойте параметру *wParam* значение ДБТ \_ Пользователяопределенные и задайте *lParam* , как описано ниже.


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
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

Задайте для параметра значение ДБТ \_ пользователяопределенные.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**\_ \_ \_ пользователяопределенные для разработки**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) , которая описывает выполняемую пользователем трансляцию. Член **дбуд \_ szName** содержит имя определяемого пользователем сообщения, за которым следуют все определяемые пользователем данные.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true**.

## <a name="requirements"></a>Требования



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

[**\_\_пользователяопределенныеная рассылка dev \_**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**WM \_ девицечанже**](wm-devicechange.md)
</dt> <dt>

[**броадкастсистеммессаже**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

