---
description: В этом разделе описываются типы оконных классов, способ их определения системой и элементы, определяющие поведение по умолчанию для окон, к которым они относятся.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: классы окон (Windows и сообщения)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77e96a06433bf6bbcb72fb76a41a29fccee27ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482650"
---
# <a name="window-classes-windows-and-messages"></a>классы окон (Windows и сообщения)

В этом разделе описываются типы оконных классов, способ их определения системой и элементы, определяющие поведение по умолчанию для окон, к которым они относятся.

Класс окна — это набор атрибутов, которые система использует в качестве шаблона для создания окна. Каждое окно является членом класса Window. Все классы окон обрабатываются отдельно.

### <a name="in-this-section"></a>В этом разделе



| Имя                                                 | Описание                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [О классах окон](about-window-classes.md)     | Обсуждаются классы окон. Каждый класс окна имеет связанную процедуру окна, совместно используемую всеми окнами того же класса. Процедура окна обрабатывает сообщения для всех окон этого класса и, следовательно, управляет их поведением и внешним видом.<br/> |
| [Использование классов окон](using-window-classes.md)     | Демонстрирует, как зарегистрировать локальное окно и использовать его для создания главного окна.<br/>                                                                                                                                                                     |
| [Справочник по классам окон](window-class-reference.md) | Содержит справочник по API.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Функции класса Window



| Имя                                         | Описание                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетклассинфоекс**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Извлекает сведения о классе окна, включая маркер мелкого значка, связанного с классом окна. Функция [**жетклассинфо**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) не получает маркер для мелкого значка.<br/> |
| [**жеткласслонг**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Извлекает заданное 32-разрядное (**длинное**) значение из структуры [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) , связанной с указанным окном. <br/>                                                                         |
| [**жеткласслонгптр**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Извлекает указанное значение из структуры [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) , связанной с указанным окном.<br/>                                                                                            |
| [**ClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Возвращает имя класса, которому принадлежит указанное окно. <br/>                                                                                                                                            |
| [**жетвиндовлонг**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Извлекает сведения об указанном окне. Функция также получает 32-разрядное (**длинное**) значение с указанным смещением в дополнительной памяти окна.<br/>                                                    |
| [**жетвиндовлонгптр**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Извлекает сведения об указанном окне. Функция также получает значение с указанным смещением в дополнительной памяти окна.<br/>                                                                        |
| [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Регистрирует класс окна для последующего использования в вызовах функции [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Регистрирует класс окна для последующего использования в вызовах функции [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . <br/>                                                            |
| [**сеткласслонгптр**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Заменяет указанное значение по указанному смещению в памяти дополнительного класса или структуры [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) для класса, к которому принадлежит указанное окно.<br/>                              |
| [**сетклассворд**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Заменяет 16-разрядное значение (**Word**) с указанным смещением на дополнительную память класса для класса Window, к которому принадлежит указанное окно.<br/>                                                               |
| [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Изменяет атрибут указанного окна. Функция также задает 32-разрядное (длинное) значение с указанным смещением в дополнительной памяти окна.<br/>                                                                 |
| [**сетвиндовлонгптр**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Изменяет атрибут указанного окна. Функция также задает значение с указанным смещением в дополнительной памяти окна.<br/>                                                                                   |
| [**унрегистеркласс**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Отменяет регистрацию класса окна, освобождая память, необходимую для класса. <br/>                                                                                                                                            |



 

Следующие функции являются устаревшими.




| Имя | Описание | 
|------|-------------|
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>жетклассинфо</strong></a> | Извлекает сведения о классе окна. <br /><blockquote>[!Note]<br />Функция <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>жетклассинфо</strong></a> была заменена функцией <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>жетклассинфоекс</strong></a> . Однако вы по-прежнему можете использовать <strong>жетклассинфо</strong>, если вам не нужны сведения о небольшом значке класса.</blockquote><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>жетклассворд</strong></a> | Получает 16-разрядное значение (<strong>Word</strong>) с указанным смещением в память дополнительного класса для класса окна, к которому принадлежит указанное окно.<blockquote>[!Note]<br />Эта функция является устаревшей для любого использования, кроме <em>ниндекс</em> , в значение GCW_ATOM. Функция предоставляется только для обеспечения совместимости с 16-разрядными версиями Windows. Приложения должны использовать функцию <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>жеткласслонг</strong></a> .</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>сеткласслонг</strong></a> | Заменяет заданное 32-разрядное (<strong>длинное</strong>) значение по указанному смещению на дополнительную память класса или структуру <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>вндклассекс</strong></a> для класса, к которому принадлежит указанное окно.<blockquote>[!Note]<br />Эта функция была заменена функцией <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>сеткласслонгптр</strong></a> . чтобы написать код, совместимый как с 32-разрядными, так и с 64-разрядными версиями Windows, используйте <strong>сеткласслонгптр</strong>.</blockquote><br /><br /> | 




 

### <a name="window-class-structures"></a>Структуры классов окон



| Имя                             | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Содержит атрибуты класса Window, зарегистрированные функцией [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . <br/> Эта структура заменена структурой [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) , используемой с функцией [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Вы по-прежнему можете использовать [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) и [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) , если не нужно задавать маленький значок, связанный с классом Window.<br/>                                                  |
| [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Содержит сведения о классе окна. Он используется с функциями [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) и [**жетклассинфоекс**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  . <br/> Структура [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) похожа на структуру [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Существует два отличия. **Вндклассекс** включает элемент **кбсизе** , указывающий размер структуры, и элемент **хиконсм** , который содержит маркер небольшого значка, связанного с классом окна.<br/> |



 

 

 
