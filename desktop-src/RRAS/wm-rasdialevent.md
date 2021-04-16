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
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672471"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

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

 

