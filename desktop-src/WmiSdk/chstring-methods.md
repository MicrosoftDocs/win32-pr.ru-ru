---
description: Класс Чстринг предоставляет следующие методы.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Методы Чстринг
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081004"
---
# <a name="chstring-methods"></a>Методы Чстринг

\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Класс [**чстринг**](chstring.md) предоставляет следующие методы.

## <a name="in-this-section"></a>Содержание раздела

-   [**Метод Аллоксисстринг**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   [**Конструкторы Чстринг**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))
-   [**Метод COLLATE**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [**Compare - метод**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [**Метод Компаренокасе**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [**Пустой метод**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   [**Поиск методов**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))
-   [**Метод Финдонеоф**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   [**Методы форматирования**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))
-   [**Методы Форматмессажев**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))
-   [**Метод Форматв**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [**Метод Фриекстра**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [**Метод Жеталлокленгс**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   [**Метод GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))
-   [**GetBuffer - метод**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [**Метод Жетбуфферсетленгс**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [**Метод GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [**Метод DATALENGTH**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [**IsEmpty - метод**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [**Метод Left**](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   [**Метод Лоадстрингв**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))
-   [**Метод Локкбуффер**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [**Метод Макеловер**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [**Метод Макереверсе**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [**Метод Макеуппер**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   [**Методы mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))
-   [**\[ \] метод оператора**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))
-   [**Чстринг:: operator +**](chstring--operator-plus.md)
-   [**Чстринг:: operator + =**](chstring--operator-plus-equal.md)
-   [**Чстринг:: operator =**](chstring--operator-equal.md)
-   [**operator = = (Констчстринг&, Констчстринг&) метод**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))
-   [**operator = = (Констчстринг&, Констлпквстр&) метод**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))
-   [**метод> оператора (Констчстринг&, Констчстринг&)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))
-   [**метод> оператора (Констчстринг&, Констлпквстр&)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))
-   [**operator>= (Констчстринг&, Констчстринг&) метод**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))
-   [**operator>= (Констчстринг&, Констлпквстр&) метод**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))
-   [**метод< оператора (Констчстринг&, Констчстринг&)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))
-   [**метод< оператора (Констчстринг&, Констлпквстр&)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))
-   [**operator<= (Констчстринг&, Констчстринг&) метод**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))
-   [**operator<= (Констчстринг&, Констлпквстр&) метод**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))
-   [**operator! = (Констчстринг&, Констчстринг&) метод**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))
-   [**operator! = (Констчстринг&, Констлпквстр&) метод**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))
-   [**operator ЛПКВСТР, метод**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [**Метод Релеасебуффер**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [**Метод Реверсефинд**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [**Метод right**](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [**Метод SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [**Метод Спанексклудинг**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [**Метод Спанинклудинг**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [**Метод Тримлефт**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [**Метод Тримригхт**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [**Метод Унлоккбуффер**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
