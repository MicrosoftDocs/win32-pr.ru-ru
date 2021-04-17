---
description: Конструктор классов Вбемтиме упрощает преобразование между различными форматами времени выполнения Windows и ANSI C.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'Конструкторы Вбемтиме:: Вбемтиме (Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713023"
---
# <a name="wbemtimewbemtime-constructors"></a>Конструкторы Вбемтиме:: Вбемтиме

\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Конструктор классов **вбемтиме** упрощает преобразование между различными форматами времени выполнения Windows и ANSI C.

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
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Вбемтиме. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
