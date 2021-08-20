---
description: При отладке используются следующие функции.
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: Функции отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfafdf5a453d262e75c4ab87356cbe34cfbb8574b520d353de0e66057903087f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162675"
---
# <a name="debugging-functions"></a>Функции отладки

При отладке используются следующие функции.



| Функция                                                           | Описание                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**чеккремотедебугжерпресент**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | Определяет, выполняется ли отладка указанного процесса.                         |
| [**континуедебужевент**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | Позволяет отладчику продолжить поток, который ранее сообщил о событии отладки. |
| [**дебугактивепроцесс**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | Позволяет отладчику подключаться к активному процессу и выполнять его отладку.                     |
| [**дебугактивепроцессстоп**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | Останавливает отладку указанного процесса отладчиком.                            |
| [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | Приводит к возникновению исключения точки останова в текущем процессе.                      |
| [**дебугбреакпроцесс**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | Приводит к возникновению исключения точки останова в указанном процессе.                    |
| [**дебугсетпроцесскиллонексит**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | Задает действие, выполняемое при выходе из вызывающего потока.                      |
| [**фаталексит**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | Передает управление выполнением отладчику.                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | Очищает кэш инструкций для указанного процесса.                            |
| [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | Возвращает контекст указанного потока.                                      |
| [**жетсреадселекторентри**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | Извлекает запись таблицы дескрипторов для указанного селектора и потока.           |
| [**исдебугжерпресент**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | Определяет, отлаживается ли вызывающий процесс отладчиком пользовательского режима.   |
| [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | Отправляет в отладчик строку для вывода.                                         |
| [**реадпроцессмемори**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | Считывает данные из области памяти в указанном процессе.                           |
| [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | Задает контекст для указанного потока.                                          |
| [**ваитфордебужевент**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | Ожидает возникновения события отладки в отлаживаемом процессе.                   |
| [**Wow64GetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | Возвращает контекст указанного потока WOW64.                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | Извлекает запись таблицы дескрипторов для указанного селектора и потока WOW64.     |
| [**Wow64SetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | Задает контекст указанного потока WOW64.                                     |
| [**вритепроцессмемори**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | Записывает данные в область памяти в указанном процессе.                            |



 

 

 
