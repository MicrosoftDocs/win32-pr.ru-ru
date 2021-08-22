---
description: операторы присваивания класса вбемтиме перегружаются для упрощения преобразований между различными Windows и форматами времени выполнения ANSI C. Ниже перечислены различные перегруженные сигнатуры.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'Операторы Вбемтиме:: operator = (Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 321ca0ba75d40389fbd6eb2ba70dc67a9b8e16afd3b5390bbc9ec61bd875c79a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502904"
---
# <a name="wbemtimeoperator-operators"></a>Операторы Вбемтиме:: operator =

\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

операторы присваивания класса [**вбемтиме**](wbemtime.md) перегружаются для упрощения преобразований между различными Windows и форматами времени выполнения ANSI C. Ниже перечислены различные перегруженные сигнатуры.

### <a name="overload-list"></a>Список перегрузок



| Оператор                                                                     | Описание                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**operator = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Преобразует **BSTR** в формат **вбемтиме** .<br/>         |
| [**operator = (время \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Преобразует **\_ t** в формат **вбемтиме** .<br/>        |
| [**operator = (FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Преобразует значение **fileTime** в формат **вбемтиме** .<br/>       |
| [**operator = (структура TM&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Преобразует структуру **TM** в формат **вбемтиме** .<br/> |
| [**operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Преобразует **SYSTEMTIME** в формат **вбемтиме** .<br/>     |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Сервер 2008<br/>                                                                                                                                |
| Заголовок<br/>                   | <dl> <dt>Вбемтиме. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
