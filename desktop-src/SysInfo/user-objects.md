---
description: Объекты пользовательского интерфейса поддерживают только один обработчик для каждого объекта. Процессы не могут наследовать или дублировать дескрипторы для объектов пользователей. Процессы в одном сеансе не могут ссылаться на пользовательский обработчик в другом сеансе.
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: Пользовательские объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ed8afcf0f1d0e4c232cf503bc2c7ba86dca42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553559"
---
# <a name="user-objects"></a>Пользовательские объекты

Объекты пользовательского интерфейса поддерживают только один обработчик для каждого объекта. Процессы не могут наследовать или дублировать дескрипторы для объектов пользователей. Процессы в одном сеансе не могут ссылаться на пользовательский обработчик в другом сеансе.

Существует теоретический предел в 65 536 пользовательских дескрипторов на сеанс. Однако максимальное число дескрипторов пользователей, которые могут быть открыты для каждого сеанса, обычно меньше, так как на него влияет доступная память. Существует также ограничение по умолчанию для каждого процесса дескрипторов пользователей. Чтобы изменить это ограничение, задайте следующее значение реестра:

**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **усерпроцесшандлекуота**

Для этого значения можно задать число от 200 до 18 000.

## <a name="handles-to-user-objects"></a>Дескрипторы объектов пользователей

Дескрипторы объектов пользователей являются общедоступными для всех процессов. То есть любой процесс может использовать пользовательский обработчик объекта при условии, что этот процесс имеет доступ к этому объекту.

На следующем рисунке приложение создает объект Window. Функция [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) создает объект Window и возвращает маркер объекта.

![приложение, создающее объект Window](images/cshob-01.png)

После создания объекта Window приложение может использовать маркер окна для вывода или изменения окна. Этот маркер остается действительным до тех пор, пока не будет уничтожен объект Window.

На следующем рисунке приложение уничтожает объект Window. Функция [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) удаляет объект Window из памяти, что делает недействительным маркер окна.

![уничтожение объекта окна](images/cshob-02.png)

## <a name="managing-user-objects"></a>Управление объектами пользователей

В следующей таблице перечислены объекты пользователей, а также функции создателя и уничтожения каждого объекта. Функции Creator создают объект и обработчик объекта или просто возвращают существующий объектный обработчик. Функции уничтожения удаляют объект из памяти, что делает недействительным обработку объекта.



| Объект-пользователь       | Функция Creator                                                                                                                                                                                                                                                              | Функция уничтожения                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Таблица сочетаний клавиш | [**креатеакцелератортабле**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**дестройакцелератортабле**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| Курсор             | [**креатекарет**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**дестройкарет**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| Курсор            | [**Креатекурсор**](/windows/win32/api/winuser/nf-winuser-createcursor), [**лоадкурсор**](/windows/win32/api/winuser/nf-winuser-loadcursora), [**лоадимаже**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                                   | [**дестройкурсор**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| Беседа DDE  | [**Ддеконнект**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect), [ **ддеконнектлист**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**Ддедисконнект**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect), [ **ддедисконнектлист**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| Ключ              | [**сетвиндовшукекс**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**унхуквиндовшукекс**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| Значок              | [**Креатеикониндирект**](/windows/win32/api/winuser/nf-winuser-createiconindirect), [**лоадикон**](/windows/win32/api/winuser/nf-winuser-loadicona), [**лоадимаже**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                           | [**дестройикон**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| Меню              | [**Креатемену**](/windows/win32/api/winuser/nf-winuser-createmenu), [**креатепопупмену**](/windows/win32/api/winuser/nf-winuser-createpopupmenu), [**лоадмену**](/windows/win32/api/winuser/nf-winuser-loadmenua), [**лоадменуиндирект**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta)                                                                                          | [**дестроймену**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| Окно            | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa), [**креатедиалогпарам**](/windows/win32/api/winuser/nf-winuser-createdialogparama), [**креатедиалогиндиректпарам**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama), [**креатемдивиндов**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) | [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| Расположение окна   | [**бегиндефервиндовпос**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**енддефервиндовпос**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
