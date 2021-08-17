---
description: класс вбемтиме упрощает преобразование между различными Windows и форматами времени выполнения ANSI C. Дополнительные сведения см. в разделе также методы класса Вбемтимеспан.
ms.assetid: b633bc8c-9d02-4bcf-8528-10773fb5ae7a
ms.tgt_platform: multiple
title: Класс WBEMTime (WbemTime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEMTime
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 16b4e8933113386e877aec23313f74695b321f932c10f0e2730bcf5888675cc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553250"
---
# <a name="wbemtime-class"></a>Класс Вбемтиме

\[Класс **вбемтиме** является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

класс **вбемтиме** упрощает преобразование между различными Windows и форматами времени выполнения ANSI C. Дополнительные сведения см. в разделе также [**методы класса вбемтимеспан**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan).

## <a name="members"></a>Элементы

Класс **вбемтиме** имеет следующие типы членов:

-   [Конструкторы](#constructors)
-   [Методы](#methods)

### <a name="constructors"></a>Конструкторы

Класс **вбемтиме** содержит эти конструкторы.



| Конструктор                           | Описание                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**вбемтиме**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | конструктор, упрощающий преобразование между различными Windows и форматами времени выполнения ANSI C.<br/> |



 

### <a name="methods"></a>Методы

Класс **вбемтиме** содержит следующие методы.



| Метод                                                           | Описание                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Clear**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Устанавливает время в объекте **вбемтиме** на недопустимое время.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Представляет время как значение **BSTR** .<br/>                                                                                      |
| [**жетдмтф**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Возвращает время в виде значения **BSTR** в формате даты и времени CIM.<br/>                                                                   |
| [**жетдмтфноннтфс**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Возвращает дату в формате DMTF на основе файловой системы FAT или [формата даты и времени](date-and-time-format.md) , где неизвестно время в формате UTC.<br/> |
| [**Функции getFileTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Возвращает время в виде структуры **fileTime** MFC.<br/>                                                                             |
| [**жетлокалоффсетфордате**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Перегружен. Возвращает смещение в минутах (+ или-) между GMT и местным временем для времени, заданного в аргументе.<br/>         |
| [**жетструкттм**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Получает время как структуру **TM** среды выполнения C в формате CRT.<br/>                                                                |
| [**GetSYSTEMTIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Возвращает время как структуру MFC **SYSTEMTIME** .<br/>                                                                           |
| [**GetTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Возвращает время в виде 64-разрядного целого числа.<br/>                                                                                          |
| [**Время \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Получает время как переменную t времени выполнения C в формате ANSI \_ .<br/>                                                                       |
| [**исок**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Указывает, представляет ли объект **вбемтиме** допустимое время.<br/>                                                          |
| [**сетдмтф**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Задает время в объекте **вбемтиме** в формате даты и времени CIM.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>Вбемтиме перегруженные операторы

Объект **вбемтиме** определяет следующие перегруженные операторы.



| Вбемтиме перегруженные операторы                                                                                                                                                                                                                                                                                                                                                                                                                                        | Описание                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Оператор =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | оператор *присваивания* упрощает преобразование между различными Windows и форматами времени выполнения ANSI C.                           |
| [**operator +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | Оператор *сложения* увеличивает время объекта на интервал времени. Результат возвращается в новом объекте **вбемтиме** .              |
| [**operator + =**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | Оператор *Add-and-Assign* увеличивает время объекта на интервал времени.                                                             |
| [**станции**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | Оператор *вычитания* уменьшает время объекта на время другого объекта. Результат возвращается в новом объекте **вбемтиме** . |
| [**Оператор-=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | Оператор *вычитания и присваивания* уменьшает время объекта на интервал времени.                                                        |
| operator [**= =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)[**оператор! =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**Оператор >**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**Оператор >=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**Оператор <**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**Оператор <=**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Операторы сравнения сравнивают два объекта **вбемтиме** .                                                                            |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Вбемтиме. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



 

