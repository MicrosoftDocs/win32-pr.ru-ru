---
description: При обработке ошибок используются следующие функции.
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: Функции обработки ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4cea391f05638310e17b9ef283e138204bc2cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140803"
---
# <a name="error-handling-functions"></a>Функции обработки ошибок

При обработке ошибок используются следующие функции.



| Функция                                                 | Описание                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Дача**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | Создает простые тона на динамике.                                                                                        |
| [**каптурестаккбакктраце**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | Фиксирует обратную трассировку стека, выполнив проход вверх по стеку и записывая сведения для каждого кадра.                             |
| [**фаталаппексит**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | Отображает окно сообщения и завершает приложение при закрытии окна сообщения.                                         |
| [**FlashWindow интерфейса**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | Один раз мигает указанное окно.                                                                                        |
| [**флашвиндовекс**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | Замигает указанное окно.                                                                                                 |
| [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | Форматирует строку сообщения.                                                                                                     |
| [**жетеррормоде**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | Возвращает режим ошибок для текущего процесса.                                                                             |
| [**Функция**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | Получает значение кода последней ошибки вызывающего потока.                                                                         |
| [**жетсреадеррормоде**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | Возвращает режим ошибок для вызывающего потока.                                                                              |
| [**мессажебип**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | Воспроизводит звуковой сигнал.                                                                                                       |
| [**ртллукупфунктионентри**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | Выполняет поиск записи, соответствующей указанному значению ПК, в таблицах активных функций.                                  |
| [**ртлнтстатустодосеррор**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | Возвращает код системной ошибки, соответствующий указанному коду ошибки NT.                                              |
| [**ртлпктофилехеадер**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | Получает базовый адрес образа, содержащего указанное значение ПК.                                                 |
| [**ртлунвинд**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | Инициирует очистку кадров вызова процедуры.                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | Инициирует очистку кадров вызова процедуры.                                                                                 |
| [**ртлунвиндекс**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | Инициирует очистку кадров вызова процедуры.                                                                                 |
| [**ртлвиртуалунвинд**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | Возвращает контекст вызова функции, предшествующей заданному контексту функции.                                |
| [**Функцию SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | Определяет, будет ли система обрабатывать заданные типы серьезных ошибок или будет ли процесс обрабатывать их.       |
| [**сетластеррор**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | Задает код последней ошибки для вызывающего потока.                                                                              |
| [**сетластеррорекс**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | Задает код последней ошибки для вызывающего потока.                                                                              |
| [**сетсреадеррормоде**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | Определяет, будет ли система управлять заданными типами серьезных ошибок или же они будут обработаны вызывающим потоком. |



 

 

 
