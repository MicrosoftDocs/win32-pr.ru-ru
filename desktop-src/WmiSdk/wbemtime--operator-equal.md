---
description: Операторы присваивания класса Вбемтиме перегружаются для упрощения преобразований между различными форматами времени выполнения Windows и ANSI C. Ниже перечислены различные перегруженные сигнатуры.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'Операторы Вбемтиме:: operator = (Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349612"
---
# <a name="wbemtimeoperator-operators"></a>Операторы Вбемтиме:: operator =

\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Операторы присваивания класса [**вбемтиме**](wbemtime.md) перегружаются для упрощения преобразований между различными форматами времени выполнения Windows и ANSI C. Ниже перечислены различные перегруженные сигнатуры.

### <a name="overload-list"></a>Список перегрузок



| Оператор                                                                     | Описание                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**operator = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Преобразует **BSTR** в формат **вбемтиме** .<br/>         |
| [**operator = (время \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Преобразует **\_ t** в формат **вбемтиме** .<br/>        |
| [**operator = (FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Преобразует значение **fileTime** в формат **вбемтиме** .<br/>       |
| [**operator = (структура TM&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Преобразует структуру **TM** в формат **вбемтиме** .<br/> |
| [**operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Преобразует **SYSTEMTIME** в формат **вбемтиме** .<br/>     |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Вбемтиме. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
