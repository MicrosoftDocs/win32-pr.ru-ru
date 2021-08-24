---
title: Оконные функции и рабочие станции
description: Приложения могут использовать следующие функции с объектами Windows Station.
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccda67841508081444f7025e457c9a778195b99d0ab67ebb585362d7a3b22cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810404"
---
# <a name="window-station-and-desktop-functions"></a>Оконные функции и рабочие станции

Приложения могут использовать следующие функции с объектами [Windows Station](window-stations.md) .



| Функция                                                     | Описание                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**клосевиндовстатион**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | Закрывает обработчик открытой оконной станции.                                                                           |
| [**креатевиндовстатион**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | Создает объект Windows Station, связывает его с текущим процессом и назначает его текущему сеансу. |
| [**енумвиндовстатионс**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | Перечисление всех оконных станций в текущем сеансе.                                                          |
| [**жетпроцессвиндовстатион**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | Извлекает маркер текущей оконной станции для вызывающего процесса.                                       |
| [**жетусеробжектинформатион**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Извлекает сведения об указанной рабочей станции или объекте рабочего стола.                                     |
| [**жетусеробжектсекурити**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Извлекает сведения о безопасности для указанной рабочей станции или объекта рабочего стола.                              |
| [**опенвиндовстатион**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | Открывает указанную станцию окна.                                                                             |
| [**сетпроцессвиндовстатион**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | Назначает указанную станцию окна вызывающему процессу.                                                    |
| [**сетусеробжектинформатион**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Задает сведения об указанной рабочей станции или объекте рабочего стола.                                          |
| [**сетусеробжектсекурити**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Задает сведения о безопасности для указанной рабочей станции или объекта рабочего стола.                                   |



 

Приложения могут использовать следующие функции с объектами [рабочего стола](desktops.md) .



| Функция                                                     | Описание                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**клоседесктоп**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | Закрывает открытый маркер для объекта Desktop.                                                                                         |
| [**креатедесктоп**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | Создает новый рабочий стол, связывает его с текущей станцией окна вызывающего процесса и назначает его вызывающему потоку. |
| [**креатедесктопекс**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | Создает новый рабочий стол, связывает его с текущей станцией окна вызывающего процесса и назначает его вызывающему потоку. |
| [**енумдесктопс**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | Перечисляет все настольные компьютеры, связанные с текущей рабочей станцией вызывающего процесса.                                         |
| [**енумдесктопвиндовс**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | Перечисление всех окон верхнего уровня, связанных с указанным рабочим столом.                                                            |
| [**жетсреаддесктоп**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | Извлекает маркер рабочего стола, назначенный указанному потоку.                                                                |
| [**жетусеробжектинформатион**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Возвращает сведения о рабочей станции или объекте рабочего стола.                                                                         |
| [**жетусеробжектсекурити**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Возвращает сведения о безопасности для объекта рабочей станции или рабочего стола.                                                                  |
| [**опендесктоп**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | Открывает указанный объект Desktop.                                                                                                |
| [**опенинпутдесктоп**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | Открывает Рабочий стол, который получает входные данные пользователя.                                                                                        |
| [**сетсреаддесктоп**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | Назначает указанный рабочий стол вызывающему потоку.                                                                               |
| [**сетусеробжектинформатион**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Задает сведения о рабочей станции или объекте рабочего стола.                                                                         |
| [**сетусеробжектсекурити**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Задает сведения о безопасности для объекта рабочей станции или рабочего стола.                                                                  |
| [**свитчдесктоп**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | Делает Рабочий стол видимым и активирует его. Это позволяет рабочему столу принимать входные данные от пользователя.                                 |



 

 

 