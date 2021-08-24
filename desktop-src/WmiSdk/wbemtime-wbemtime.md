---
description: конструктор класса вбемтиме упрощает преобразование между различными Windows и форматами времени выполнения ANSI C.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'Конструкторы Вбемтиме:: Вбемтиме (Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ac02e3ee2a7a77ed1cc2cc9157b0d6c191563f234bf594cb53029a76e76f0137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757624"
---
# <a name="wbemtimewbemtime-constructors"></a>Конструкторы Вбемтиме:: Вбемтиме

\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

конструктор класса **вбемтиме** упрощает преобразование между различными Windows и форматами времени выполнения ANSI C.

### <a name="overload-list"></a>Список перегрузок



| Конструктор                                                                 | Описание                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**Вбемтиме ()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                                   | Создает неинициализированный объект Time.<br/>                          |
| [**Вбемтиме (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                           | Инициализирует новый объект Time для значения в параметре.<br/> |
| [**Вбемтиме (время константы \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))        | Инициализирует новый объект Time для значения в параметре.<br/> |
| [**Вбемтиме (const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))    | Инициализирует новый объект Time для значения в параметре.<br/> |
| [**Вбемтиме (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))     | Инициализирует новый объект Time для значения в параметре.<br/> |
| [**Вбемтиме (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_)) | Инициализирует новый объект Time для значения в параметре.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Сервер 2008<br/>                                                                                                                                |
| Заголовок<br/>                   | <dl> <dt>Вбемтиме. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
