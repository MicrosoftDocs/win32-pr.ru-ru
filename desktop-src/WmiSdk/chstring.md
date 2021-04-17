---
description: В следующей таблице перечислены методы Чстринг.
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.tgt_platform: multiple
title: Класс Чстринг (Чстринг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CHString
- ??1CHString@@QAE@XZ
- ??1CHString@@QEAA@XZ
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 0c94fcd89a41e610d039afe17f4b56e58cb117bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693502"
---
# <a name="chstring-class"></a>Класс Чстринг

\[Класс **чстринг** является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

В следующей таблице перечислены методы **чстринг** .

## <a name="members"></a>Элементы

Класс **чстринг** имеет следующие типы членов:

-   [Конструкторы](#constructors)
-   [Методы](#methods)
-   [Операторы](#operators)

### <a name="constructors"></a>Конструкторы

Класс **чстринг** содержит эти конструкторы.



| Конструктор                           | Описание                                                 |
|:--------------------------------------|:------------------------------------------------------------|
| [**чстринг**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_)) | Конструирует строки **чстринг** различными способами.<br/> |



 

### <a name="methods"></a>Методы

Класс **чстринг** содержит следующие методы.



| Метод                                                    | Описание                                                                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**аллоксисстринг**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)         | Выделяет BSTR из данных **чстринг** .<br/>                                                            |
| [**COLLATE**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)                       | Сравнивает две строки (с учетом регистра; использует сведения, зависящие от локали).<br/>                            |
| [**Сравнение**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)                       | Сравнивает две строки (с учетом регистра).<br/>                                                              |
| [**компаренокасе**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)           | Сравнивает две строки (без учета регистра).<br/>                                                            |
| [**Указано**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)                           | Задает для строки нулевую длину.<br/>                                                            |
| [**Поиск**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))                        | Перегружен. Находит символ или подстроку в более длинной строке.<br/>                                  |
| [**финдонеоф**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)                   | Находит первый соответствующий символ из набора.<br/>                                                      |
| [**Формат**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))                         | Перегружен. Форматирует строку как **sprintf** .<br/>                                                 |
| [**форматмессажев**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))         | Перегружен. Форматирует строку сообщения.<br/>                                                               |
| [**форматв**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)                       | Форматирует строку как **vsprintf** .<br/>                                                            |
| [**фриекстра**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)                   | Удаляет все издержки этой строки путем освобождения дополнительной памяти, ранее выделенной для строки.<br/> |
| [**жеталлокленгс**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)         | Возвращает размер строкового буфера.<br/>                                                              |
| [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))                           | Перегружен. Возвращает символ в заданной позиции.<br/>                                              |
| [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)                   | Возвращает указатель на символы в строке **чстринг** .<br/>                                     |
| [**жетбуфферсетленгс**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength) | Возвращает указатель на символы в строке **чстринг** , усекаются до указанной длины.<br/> |
| [**GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)                       | Возвращает указатель на данные в строке **чстринг** .<br/>                                           |
| [**GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)                   | Возвращает число символов Юникода в строке **чстринг** .<br/>                                  |
| [**IsEmpty**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)                       | Проверяет, содержит ли строка **чстринг** символы.<br/>                                         |
| [**Слева**](/windows/desktop/api/ChString/nf-chstring-chstring-left)                             | Извлекает левую часть строки (например, базовую функцию **Left $** ).<br/>                             |
| [**лоадстрингв**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))               | Загружает существующую **чстринг** строку из файла ресурсов.<br/>                                         |
| [**локкбуффер**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)                 | Отключает подсчет ссылок и защищает строку в буфере.<br/>                                  |
| [**макеловер**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)                   | Преобразует все символы в этой строке в символы нижнего регистра.<br/>                              |
| [**макереверсе**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)               | Меняет местами символы в этой строке.<br/>                                                             |
| [**макеуппер**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)                   | Преобразует все символы в этой строке в символы верхнего регистра.<br/>                              |
| [**Расчет**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))                               | Перегружен. Извлекает среднюю часть строки (например, базовую функцию **MID $** ).<br/>                |
| [**релеасебуффер**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)           | Выводит управление буфером, возвращенным методом [**onbuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer).<br/>                 |
| [**реверсефинд**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)               | Находит символ в более длинной строке; начинается с конца.<br/>                                      |
| [**Правильно**](/windows/desktop/api/ChString/nf-chstring-chstring-right)                           | Извлекает правую часть строки (как базовая **правая $** Function).<br/>                           |
| [**SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)                           | Задает символ в заданной позиции.<br/>                                                               |
| [**спанексклудинг**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)           | Извлекает подстроку, которая содержит только символы, отсутствующие в наборе.<br/>                     |
| [**спанинклудинг**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)           | Извлекает подстроку, содержащую только символы в наборе.<br/>                                    |
| [**TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)                     | Обрезает начальные символы пробела из строки.<br/>                                                |
| [**TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)                   | Обрезает пробелы в конце строки.<br/>                                               |
| [**унлоккбуффер**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)             | Включает подсчет ссылок и освобождает строку в буфере.<br/>                                   |



 

### <a name="operators"></a>Операторы
`
The **CHString** class has these operators.`



| Оператор                                                                                            | Описание                                                                                                       |
|:----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| [**operator! = (Чстринг, Чстринг)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))            | Сравнивает две **чстрингс** для неравенства.<br/>                                                             |
| [**operator! = (Чстринг, ЛПКВСТР)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))              | Сравнивает **чстринг** с **лпквстр** для неравенства.<br/>                                             |
| [**станции \[\]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))                                                | Возвращает символ в заданной подстановке оператора позиции для [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int)).<br/> |
| [**operator +**](chstring--operator-plus.md)                                                       | Сцепляет две строки и возвращает новую строку.<br/>                                                     |
| [**operator + =**](chstring--operator-plus-equal.md)                                                | Сцепляет новую строку до конца существующей строки.<br/>                                            |
| [**< оператора (Чстринг, ЛПКВСТР)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))            | Сравнивает **чстринг** с **лпквстр**.<br/>                                                            |
| [**< оператора (Чстринг, Чстринг)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))          | Сравнивает два **чстрингс**.<br/>                                                                            |
| [**Оператор <= (Чстринг, Чстринг)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))    | Сравнивает два **чстрингс**.<br/>                                                                            |
| [**Оператор <= (Чстринг, ЛПКВСТР)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))      | Сравнивает **чстринг** с **лпквстр**.<br/>                                                            |
| [**Оператор =**](chstring--operator-equal.md)                                                      | Присваивает новое значение **чстринг** строке.<br/>                                                          |
| [**оператор = = (Чстринг, Чстринг)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))          | Сравнивает два **чстрингс** на равенство.<br/>                                                               |
| [**оператор = = (Чстринг, ЛПКВСТР)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))            | Сравнивает **чстринг** с **лпквстр** для равенства.<br/>                                               |
| [**> оператора (Чстринг, Чстринг)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))       | Сравнивает два **чстрингс**.<br/>                                                                            |
| [**> оператора (Чстринг, ЛПКВСТР)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))         | Сравнивает **чстринг** с **лпквстр**.<br/>                                                            |
| [**Оператор >= (Чстринг, Чстринг)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85)) | Сравнивает два **чстрингс**.<br/>                                                                            |
| [**Оператор >= (Чстринг, ЛПКВСТР)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))   | Сравнивает **чстринг** с **лпквстр**.<br/>                                                            |
| [**Оператор ЛПКВСТР**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)                                               | Прямой доступ к символам, хранящимся в строке **чстринг** , в виде строки в стиле C.<br/>                      |



 

## <a name="remarks"></a>Комментарии

Деструктор для класса — **чстринг:: ~ чстринг**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Чстринг. h (включение Фвкоммон. h)</dt> </dl>                                                    |
| Библиотека<br/>                  | <dl> <dt>Фрамедин. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



