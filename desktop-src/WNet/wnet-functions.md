---
title: Функции Внет
description: Windows Сетевые функции предоставляют сведения и служебные программы для управления сетевыми ресурсами.
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771974bcc2967ddba32439bb655173f62b8478ad367e086e620ca02825a2567f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330789"
---
# <a name="wnet-functions"></a>Функции Внет

Windows Сетевые функции предоставляют сведения и служебные программы для управления сетевыми ресурсами. Windows сетевые функции можно группировать следующим образом:

-   [Функции подключения](#connection-functions)
-   [Функции перечисления](#enumeration-functions)
-   [Информационные функции](#information-functions)
-   [Пользовательские функции](#user-functions)

## <a name="connection-functions"></a>Функции подключения

Вызовите следующие функции подключения Внет, чтобы подключить локальное устройство к сетевому ресурсу и отменить сетевые подключения.



| Функция                                                                     | Описание                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**мултинетжетконнектионперформанце**](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | Возвращает сведения о ожидаемой производительности подключения к сетевому ресурсу.                                                                                                                                      |
| [**внетаддконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | Подключает локальное устройство к сетевому ресурсу. (Предоставляется для совместимости с 16-разрядными версиями Windows.)                                                                                                                   |
| [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | Подключает локальное устройство к сетевому ресурсу.                                                                                                                                                                                 |
| [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | Подключает локальное устройство к сетевому ресурсу. Эта функция включает еще один параметр, чем функция **WNetAddConnection2** — обработчик, который сетевой поставщик может использовать в качестве окна-владельца для диалоговых окон. |
| [**внетканцелконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | Отменяет сетевое подключение. (Предоставляется для совместимости с 16-разрядными версиями Windows.)                                                                                                                                    |
| [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | Отменяет сетевое подключение, предоставляя возможность обновления профиля пользователя сведениями о постоянных подключениях.                                                                                                  |
| [**внетконнектиондиалог**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | Открывает общее диалоговое окно обзора для подключения к сетевым ресурсам.                                                                                                                                                      |
| [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | Открывает общее диалоговое окно обзора для подключения к сетевым ресурсам с помощью структуры [**коннектдлгструкт**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .                                                                                  |
| [**внетдисконнектдиалог**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | Открывает общее диалоговое окно обзора для отключения от сетевых ресурсов.                                                                                                                                                 |
| [**WNetDisconnectDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | Открывает общее диалоговое окно обзора для отключения от сетевых ресурсов с помощью структуры [**дискдлгструкт**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa) .                                                                                   |
| [**внетжетконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | Возвращает имя сетевого ресурса, связанного с локальным устройством.                                                                                                                                                     |
| [**внетжетуниверсалнаме**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | При наличии пути на основе диска для сетевого ресурса возвращает более универсальную форму имени.                                                                                                                               |
| [**внетрестореконнектионв**](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | Восстанавливает подключение к сетевому ресурсу, запрашивая пользователя, если это необходимо, для имени и пароля.                                                                                                                      |
| [**внетусеконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | Подключает локальное устройство к сетевому ресурсу; автоматически выбирает неиспользуемое локальное устройство для перенаправления к сетевому ресурсу.                                                                                               |



 

> [!Note]  
> функции [**внетаддконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) и [**внетканцелконнектион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) поддерживаются для обеспечения совместимости с Windows для рабочих групп. Однако новые приложения должны использовать [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) или [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)и [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

 

## <a name="enumeration-functions"></a>Функции перечисления

Чтобы перечислить сетевые ресурсы, вызовите следующие функции Внет.



| Функция                                     | Описание                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**внетклосинум**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | Завершает перечисление сетевых ресурсов.                                                    |
| [**внетенумресаурце**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | Возобновляет перечисление сетевых ресурсов, запущенных функцией **внетопененум** . |
| [**внетопененум**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | Запускает перечисление сетевых ресурсов.                                             |



 

## <a name="information-functions"></a>Информационные функции

Вызовите следующие информационные и служебные функции Внет, чтобы получить поставщик сети и другие сведения.



| Функция                                                         | Описание                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**внетжетластеррор**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | Возвращает самый последний код ошибки, заданный функцией Внет, полученной от поставщика сети.  |
| [**внетжетнетворкинформатион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | Возвращает расширенные сведения о конкретном поставщике сети.                                     |
| [**внетжетпровидернаме**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | Возвращает имя поставщика для определенного типа сети.                                           |
| [**внетжетресаурцеинформатион**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | Возвращает поставщика сети, владеющего ресурсом, и получает сведения о типе ресурса. |
| [**внетжетресаурцепарент**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | Возвращает родителя сетевого ресурса.                                                           |



 

## <a name="user-functions"></a>Пользовательские функции

Вызовите следующую функцию Внет, чтобы получить имя пользователя, связанного с локальным устройством.



| Функция                           | Описание                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [**внетжетусер**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | Возвращает текущее имя пользователя по умолчанию или имя пользователя, который установил соединение. |



 

Многие функции Внет используют структуру [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) для хранения информации о сетевом ресурсе.

 

 