---
title: Записи Phone-Book
description: Записи телефонной книги содержат сведения, необходимые для установления подключения RAS. Пользователь или администратор может использовать диалоговое окно удаленный доступ к сети для создания, изменения и набора записей телефонной книги.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cc01e66b5877c90b81610a5d8cf151b7cb7bd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134367"
---
# <a name="phone-book-entries"></a>Записи Phone-Book

Записи телефонной книги содержат сведения, необходимые для установления подключения RAS. Пользователь или администратор может использовать диалоговое окно **Удаленный доступ к сети** для создания, изменения и набора записей телефонной книги.

Начиная с Windows NT Server 4,0, система поддерживает функции, описанные для Windows 95, а также ряд дополнительных функций, которые приложение может использовать для работы с телефонными книгами и записями телефонной книги.

Функция [**расентридлг**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) отображает страницу свойств, которая позволяет пользователю создавать, изменять и копировать записи телефонной книги. Функции [**раскреатефонебукентри**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) и [**Раседитфонебукентри**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) вызывают функцию **расентридлг** . Можно использовать функцию [**расренаминтри**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) для переименования записи телефонной книги или [**расделетинтри**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) для удаления записи. [**Расвалидатинтринаме**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) определяет, имеет ли указанная строка правильный формат для использования в качестве имени записи.

Для получения и настройки дополнительных сведений о записи телефонной книги можно использовать [**расжетентрипропертиес**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) и [**рассетентрипропертиес**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) . Эти функции используют структуру [**расентри**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .

Функции [**расжеткредентиалс**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) и [**рассеткредентиалс**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) получают и задают учетные данные пользователя, связанные с указанной записью телефонной книги службы удаленного доступа. Эти функции используют структуру [**раскредентиалс**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)) .

Функция [**расжеткаунтринфо**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) извлекает сведения об наборе, зависящем от страны или региона, из списка телефонии Windows для стран. **Расжеткаунтринфо** использует структуру [**расктринфо**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)) .

**Windows 95:  ** Поддерживает ограниченный набор функций для работы с записями телефонной книги. Для создания или редактирования записи телефонной книги можно использовать функции [**раскреатефонебукентри**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) и [**раседитфонебукентри**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) . Эти функции отображают диалоговое окно, в котором пользователь может указать сведения о записи телефонной книги. Вы можете использовать функции [**расжетентридиалпарамс**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) и [**рассетентридиалпарамс**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) , чтобы задать или получить параметры подключения для записи телефонной книги. Функция [**расенументриес**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) извлекает массив структур [**расентринаме**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) , содержащих имена записей телефонной книги.

 

 