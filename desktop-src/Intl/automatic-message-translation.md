---
description: Приложения, использующие функции API Юникода и кодировки символов, обычно используют один и тот же класс окна. Операционная система прозрачно преобразует сообщения между окнами различных классов.
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: Автоматическое преобразование сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809526"
---
# <a name="automatic-message-translation"></a>Автоматическое преобразование сообщений

Приложения, использующие функции API Юникода и кодировки символов, обычно используют один и тот же класс окна. Операционная система прозрачно преобразует сообщения между окнами различных классов.

Функция Window реализована для получения сообщений в формате Юникод или кодовой страницы Windows. Оконная функция может передавать сообщения или вызывать функции любого из этих типов.

Следующие сообщения содержат текстовые аргументы и подчиняются автоматическому преобразованию текста. Сведения об автоматическом переводе см. в разделе [подклассировать и автоматическое преобразование сообщений](subclassing-and-automatic-message-translation.md).

<dl>

[\_ADDSTRING CB](../controls/cb-addstring.md)  
[\_Каталог CB](../controls/cb-dir.md)  
[\_FINDSTRING CB](../controls/cb-findstring.md)  
[\_ЖЕТЛБТЕКСТ CB](../controls/cb-getlbtext.md)  
[\_ИНСЕРТСТРИНГ CB](../controls/cb-insertstring.md)  
[\_СЕЛЕКТСТРИНГ CB](../controls/cb-selectstring.md)  
[EM, \_ строка](../controls/em-getline.md)  
[EM \_ реплацесел](../controls/em-replacesel.md)  
[EM \_ сетпассвордчар](../controls/em-setpasswordchar.md)  
[ADDFILE балансировки нагрузки \_](../controls/lb-addfile.md)  
[ADDSTRING балансировки нагрузки \_](../controls/lb-addstring.md)  
[Каталог балансировки нагрузки \_](../controls/lb-dir.md)  
[FINDSTRING балансировки нагрузки \_](../controls/lb-findstring.md)  
[\_Балансировка нагрузки](../controls/lb-gettext.md)  
[инсертстринг балансировки нагрузки \_](../controls/lb-insertstring.md)  
[селектстринг балансировки нагрузки \_](../controls/lb-selectstring.md)  
[WM \_ асккбформатнаме](../dataxchg/wm-askcbformatname.md)  
[WM \_ char](../inputdev/wm-char.md)  
[WM \_ чартоитем](../controls/wm-chartoitem.md)  
[\_Создание WM](../winmsg/wm-create.md)  
[WM \_ деадчар](../inputdev/wm-deadchar.md)  
[WM \_ девмодечанже](../gdi/wm-devmodechange.md)  
[WM \_ gettext](../winmsg/wm-gettext.md)  
[WM \_ мдикреате](../winmsg/wm-mdicreate.md)  
[WM \_ менучар](../menurc/wm-menuchar.md)  
[WM \_ нккреате](../winmsg/wm-nccreate.md)  
[WM \_ SETTEXT](../winmsg/wm-settext.md)  
[WM \_ сисчар](../menurc/wm-syschar.md)  
[WM \_ сисдеадчар](../inputdev/wm-sysdeadchar.md)  
[WM \_ вининичанже](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Юникод в Windows API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
