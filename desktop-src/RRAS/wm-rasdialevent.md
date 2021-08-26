---
title: Сообщение WM_RASDIALEVENT (RAS. h)
description: Операционная система отправляет \_ сообщение WM расдиалевент в процедуру окна, когда происходит изменение события состояния во время процесса подключения RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- RAS сообщения WM_RASDIALEVENT
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093591ffe07ecbe662ca85306b74c34c670e1adbe51e2605b1f21faa20696c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024774"
---
# <a name="wm_rasdialevent-message"></a>\_Сообщение РАСДИАЛЕВЕНТ WM

Операционная система отправляет сообщение **WM \_ расдиалевент** в процедуру окна, когда происходит изменение события состояния во время процесса подключения RAS. Это происходит, когда указано окно для управления уведомлениями о таких событиях с помощью параметра " *уведомление* " в [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Два параметра сообщения эквивалентны параметрам тех же имен, которые используются с функциями обратного вызова [**расдиалфунк**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) и [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*расконнстате* 
</dt> <dd>

Значение параметра *wParam*. Эквивалентно параметру *расконнстате* функций обратного вызова [**расдиалфунк**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) и [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Указывает значение перечислителя [**расконнстате**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) , указывающее состояние, которое будет введено процессом подключения к удаленному доступу RasDial.

</dd> <dt>

*дверрор* 
</dt> <dd>

Значение *lParam*. Эквивалентно параметру *дверрор* функций обратного вызова [**расдиалфунк**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) и [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Ненулевое значение указывает на произошедшее ошибку или нуль, если ошибка не возникла.

[**Rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) отправляет это сообщение с параметром *дверрор* , имеющим значение 0, после ввода каждого состояния подключения. Если ошибка возникает в состоянии, сообщение снова отправляется в состояние, на этот раз с ненулевым *дверрор* значением.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Обзор службы удаленного доступа (RAS)](about-remote-access-service.md)
</dt> <dt>

[Сообщения службы удаленного доступа](remote-access-service-messages.md)
</dt> <dt>

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[**расдиалфунк**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

[**расконнстате**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))
</dt> </dl>

 

