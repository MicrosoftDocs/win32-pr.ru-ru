---
description: Метод Жетлокалоффсетфордате возвращает смещение в минутах (+ или &\# 8211;) между GMT и местным временем для времени, заданного в аргументе.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Методы Вбемтиме:: Жетлокалоффсетфордате (Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911479"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a>Методы Вбемтиме:: Жетлокалоффсетфордате

\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Метод **жетлокалоффсетфордате** возвращает смещение в минутах (+ или) между GMT и местным временем для времени, заданного в аргументе.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                           | Описание                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| [**Жетлокалоффсетфордате (время \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))         | Аргумент — это ссылка на **время \_ t**.<br/>  |
| [**Жетлокалоффсетфордате (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))     | Аргумент — это указатель на **fileTime**.<br/>   |
| [**Жетлокалоффсетфордате (структура TM \* )**](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | Аргумент — это указатель на структуру **TM** .<br/> |
| [**Жетлокалоффсетфордате (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime)) | Аргумент является указателем на **SYSTEMTIME**.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Вбемтиме. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
