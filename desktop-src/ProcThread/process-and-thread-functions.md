---
description: В этом разделе описываются функции процессов и потоков.
ms.assetid: 8c8e8af0-bf50-4a4b-945c-83bae1eff7dd
title: Функции процессов и потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebb1e281feb83b4a0da0c230792399d8e21684f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113121001"
---
# <a name="process-and-thread-functions"></a>Функции процессов и потоков

В этом разделе описываются функции процессов и потоков.

-   [Функция очереди диспетчеризации](#dispatch-queue-function)
-   [Функции обработки](#process-functions)
-   [Функции перечисления процессов](#process-enumeration-functions)
-   [Функции политики](#policy-functions)
-   [Функции потока](#thread-functions)
-   [Функции расширенных атрибутов процессов и потоков](#process-and-thread-extended-attribute-functions)
-   [Функции WOW64](#wow64-functions)
-   [Функции объекта задания](#job-object-functions)
-   [Функции пула потоков](#thread-pool-functions)
-   [Функции службы упорядочивания потоков](#thread-ordering-service-functions)
-   [Функции службы планировщика классов мультимедиа](#multimedia-class-scheduler-service-functions)
-   [Волоконные функции](#fiber-functions)
-   [Функции поддержки NUMA](#numa-support-functions)
-   [Функции процессора](#processor-functions)
-   [Функции планирования в режиме пользователя](#user-mode-scheduling-functions)
-   [Устаревшие функции](#obsolete-functions)

## <a name="dispatch-queue-function"></a>Функция очереди диспетчеризации

Следующая функция создает [диспатчеркуеуеконтроллер](/uwp/api/windows.system.dispatcherqueuecontroller).



| Функция                                                                   | Описание                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**креатедиспатчеркуеуеконтроллер**](/windows/desktop/api/DispatcherQueue/nf-dispatcherqueue-createdispatcherqueuecontroller) | Создает [диспатчеркуеуеконтроллер](/uwp/api/windows.system.dispatcherqueuecontroller) , который управляет временем существования объекта [DispatcherQueue](/uwp/api/windows.system.dispatcherqueue) , который запускает поставленные в очередь задачи в порядке приоритета в другом потоке. |



 

## <a name="process-functions"></a>Функции обработки

В [процессах](child-processes.md)используются следующие функции.



| Функция                                                                 | Описание                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)                                   | Создает новый процесс и его основной поток.                                                                                                                                                 |
| [**Параметр CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)                       | Создает новый процесс и его основной поток. Новый процесс выполняется в контексте безопасности пользователя, представленного указанным токеном.                                                    |
| [**креатепроцессвислогонв**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)               | Создает новый процесс и его основной поток. Затем новый процесс запускает указанный исполняемый файл в контексте безопасности указанных учетных данных (пользователя, домена и пароля).      |
| [**креатепроцессвистокенв**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithtokenw)               | Создает новый процесс и его основной поток. Новый процесс выполняется в контексте безопасности указанного токена.                                                                            |
| [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)                                       | Завершает вызывающий процесс и все его потоки.                                                                                                                                                 |
| [**флушпроцессвритебуфферс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushprocesswritebuffers)             | Очищает очередь записи каждого процессора, выполняющего поток текущего процесса.                                                                                                    |
| [**фриенвиронментстрингс**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa)                 | Освобождает блок строк среды.                                                                                                                                                         |
| [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)                                 | Получает строку командной строки для текущего процесса.                                                                                                                                    |
| [**жеткуррентпроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)                           | Извлекает псевдо-обработчик для текущего процесса.                                                                                                                                            |
| [**жеткуррентпроцессид**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid)                       | Получает идентификатор процесса вызывающего процесса.                                                                                                                                      |
| [**жеткуррентпроцессорнумбер**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)           | Возвращает номер процессора, на котором выполнялся текущий поток во время вызова этой функции.                                                                                     |
| [**жетенвиронментстрингс**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)                   | Извлекает блок среды для текущего процесса.                                                                                                                                      |
| [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)                 | Получает значение указанной переменной из блока среды вызывающего процесса.                                                                                              |
| [**жетекситкодепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)                         | Возвращает состояние завершения указанного процесса.                                                                                                                                    |
| [**жетгуиресаурцес**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)                               | Возвращает число дескрипторов графических объектов графического пользовательского интерфейса, используемых указанным процессом.                                                                                     |
| [**жетлогикалпроцессоринформатион**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Извлекает сведения о логических процессорах и связанном оборудовании.                                                                                                                          |
| [**жетприоритикласс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass)                             | Извлекает класс приоритета для указанного процесса.                                                                                                                                       |
| [**жетпроцессаффинитимаск**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask)                 | Извлекает маску сходства процесса для указанного процесса и маску сходства системы для системы.                                                                                      |
| [**жетпроцессграупаффинити**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)               | Возвращает сходство группы процессоров указанного процесса.                                                                                                                              |
| [**жетпроцесшандлекаунт**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)                   | Извлекает количество открытых дескрипторов, принадлежащих указанному процессу.                                                                                                                    |
| [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)                                     | Получает идентификатор процесса указанного процесса.                                                                                                                                    |
| [**жетпроцессидофсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread)                     | Возвращает идентификатор процесса, связанного с указанным потоком.                                                                                                         |
| [**жетпроцессиокаунтерс**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)                     | Извлекает данные учета для всех операций ввода-вывода, выполненных указанным процессом.                                                                                                   |
| [**жетпроцессмитигатионполици**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)         | Получает параметры политики устранения рисков для вызывающего процесса.                                                                                                                                 |
| [**жетпроцессприоритибуст**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost)               | Возвращает состояние управления повышением приоритета указанного процесса.                                                                                                                          |
| [**жетпроцессшутдовнпараметерс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessshutdownparameters)     | Получает параметры завершения работы для текущего вызывающего процесса.                                                                                                                              |
| [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes)                               | Извлекает сведения о времени для указанного процесса.                                                                                                                                 |
| [**жетпроцессверсион**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)                           | Извлекает основной и дополнительный номера версии системы, в которой заданный процесс должен выполняться.                                                                                    |
| [**жетпроцессворкингсетсизе**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)             | Возвращает минимальный и максимальный размеры рабочего набора указанного процесса.                                                                                                                 |
| [**жетпроцессворкингсетсизикс**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex)         | Возвращает минимальный и максимальный размеры рабочего набора указанного процесса.                                                                                                                 |
| [**жетпроцессорсистемциклетиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)       | Возвращает время цикла каждого процессора в указанной группе, затраченного на выполнение отложенных вызовов процедур (DPC) и процедур службы прерываний (ISR).                                         |
| [**жетстартупинфо**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)                                 | Извлекает содержимое структуры [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) , которая была указана при создании вызывающего процесса.                                                       |
| [**исиммерсивепроцесс**](/windows/desktop/api/Winuser/nf-winuser-isimmersiveprocess)                         | Определяет, принадлежит ли процесс к приложению Магазина Windows.                                                                                                                                |
| [**нидкуррентдиректорифорексепас**](/windows/win32/api/processenv/nf-processenv-needcurrentdirectoryforexepatha) | Определяет, следует ли включать текущий каталог в путь поиска для указанного исполняемого файла.                                                                                  |
| [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)                                       | Открывает существующий локальный объект процесса.                                                                                                                                                       |
| [**куерифуллпроцессимаженаме**](/windows/desktop/api/WinBase/nf-winbase-queryfullprocessimagenamea)           | Возвращает полное имя исполняемого образа для указанного процесса.                                                                                                                    |
| [**куерипроцессаффинитюпдатемоде**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprocessaffinityupdatemode) | Извлекает режим обновления сходства указанного процесса.                                                                                                                                  |
| [**куерипроцессциклетиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime)                   | Возвращает сумму времени цикла всех потоков указанного процесса.                                                                                                                  |
| [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)                 | Задает значение переменной среды для текущего процесса.                                                                                                                            |
| [**сетприоритикласс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass)                             | Задает класс приоритета для указанного процесса.                                                                                                                                            |
| [**сетпроцессаффинитимаск**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)                 | Задает маску сходства процессоров для потоков указанного процесса.                                                                                                                        |
| [**сетпроцессаффинитюпдатемоде**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessaffinityupdatemode)     | Задает режим обновления сходства указанного процесса.                                                                                                                                       |
| [**сетпроцессинформатион**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)                   | Задает сведения для указанного процесса.                                                                                                                                                   |
| [**сетпроцессмитигатионполици**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)         | Задает политику устранения рисков для вызывающего процесса.                                                                                                                                           |
| [**сетпроцессприоритибуст**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost)               | Отключает возможность системы временно увеличивать приоритет потоков указанного процесса.                                                                                 |
| [**сетпроцессрестриктионексемптион**](/windows/desktop/api/Winuser/nf-winuser-setprocessrestrictionexemption) | Исключает вызывающий процесс из ограничений, препятствующих взаимодействию рабочих процессов с средой приложения Магазина Windows. Эта функция используется средствами разработки и отладки. |
| [**сетпроцессшутдовнпараметерс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)     | Задает параметры завершения работы для текущего вызывающего процесса.                                                                                                                                   |
| [**сетпроцессворкингсетсизе**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize)             | Задает минимальный и максимальный размеры рабочего набора для указанного процесса.                                                                                                                     |
| [**сетпроцессворкингсетсизикс**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)         | Задает минимальный и максимальный размеры рабочего набора для указанного процесса.                                                                                                                     |
| [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)                             | Завершает указанный процесс и все его потоки.                                                                                                                                      |



 

## <a name="process-enumeration-functions"></a>Функции перечисления процессов

Для перечисления процессов используются следующие функции.



| Функция                                                    | Описание                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Получает идентификатор процесса для каждого объекта процесса в системе.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Извлекает сведения о первом процессе, обнаруженном в системном снимке.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Извлекает сведения о следующем процессе, записанном в системном снимке.        |
| [**втсенумератепроцессес**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Извлекает сведения об активных процессах на указанном сервере терминалов. |



 

## <a name="policy-functions"></a>Функции политики

Для политики уровня процесса используются следующие функции.



|  Функция                                                    |  Описание                                                     |
|------------------------------------------------------|-------------------------------------------------------|
| [**куерипротектедполици**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprotectedpolicy) | Запрашивает значение, связанное с защищенной политикой. |
| [**сетпротектедполици**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprotectedpolicy)     | Задает защищенную политику.                              |



 

## <a name="thread-functions"></a>Функции потока

В [потоках](multiple-threads.md)используются следующие функции.



| Функция                                                           | Описание                                                                                                                                               |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аттачсреадинпут**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)                     | Присоединяет механизм обработки ввода одного потока к другому потоку.                                                                          |
| [**креатеремотесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)                   | Создает поток, который выполняется в виртуальном адресном пространстве другого процесса.                                                                               |
| [**креатеремотесреадекс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)               | Создает поток, который выполняется в виртуальном адресном пространстве другого процесса и дополнительно задает расширенные атрибуты, такие как сходство групп процессоров. |
| [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)                               | Создает поток для выполнения в пределах виртуального адресного пространства вызывающего процесса.                                                                      |
| [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)                                   | Завершает вызывающий поток.                                                                                                                                  |
| [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)                       | Извлекает псевдо-обработчик для текущего потока.                                                                                                         |
| [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)                   | Получает идентификатор потока вызывающего потока.                                                                                                    |
| [**жетекситкодесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)                     | Возвращает состояние завершения указанного потока.                                                                                                 |
| [**жетсреаддескриптион**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-getthreaddescription)               | Извлекает описание, назначенное потоку путем вызова [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription).                                  |
| [**жетсреадграупаффинити**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)           | Возвращает соответствие группы процессоров указанному потоку.                                                                                           |
| [**GetThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadid)                                 | Возвращает идентификатор потока указанного потока.                                                                                                  |
| [**жетсреадидеалпроцессорекс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)     | Возвращает номер процессора идеального процессора для указанного потока.                                                                           |
| [**жетсреадинформатион**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadinformation)               | Извлекает сведения об указанном потоке.                                                                                                         |
| [**жетсреадиопендингфлаг**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadiopendingflag)           | Определяет, имеет ли указанный поток ожидающие запросы ввода-вывода.                                                                                       |
| [**жетсреадприорити**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)                     | Возвращает значение приоритета для указанного потока.                                                                                                    |
| [**жетсреадприоритибуст**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost)           | Возвращает состояние элемента управления повышением приоритета указанного потока.                                                                                       |
| [**жетсреадтимес**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadtimes)                           | Извлекает сведения о времени для указанного потока.                                                                                                    |
| [**опенсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)                                   | Открывает существующий объект потока.                                                                                                                          |
| [**куеридлепроцессорциклетиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime) | Возвращает время цикла для бездействующего потока каждого процессора в системе.                                                                             |
| [**куерисреадциклетиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime)               | Возвращает время цикла для указанного потока.                                                                                                        |
| [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)                               | Уменьшает значение счетчика приостановки потока.                                                                                                                      |
| [**сетсреадаффинитимаск**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)             | Задает маску сходства процессоров для указанного потока.                                                                                                  |
| [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)               | Присваивает описание потоку.                                                                                                                        |
| [**сетсреадграупаффинити**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)           | Задает сходство групп процессоров для указанного потока.                                                                                               |
| [**сетсреадидеалпроцессор**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor)         | Указывает предпочтительный процессор для потока.                                                                                                             |
| [**сетсреадидеалпроцессорекс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)     | Задает идеальный процессор для указанного потока и при необходимости извлекает предыдущий идеальный процессор.                                                  |
| [**сетсреадинформатион**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation)               | Задает сведения для указанного потока.                                                                                                                |
| [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)                     | Задает значение приоритета для указанного потока.                                                                                                         |
| [**сетсреадприоритибуст**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost)           | Отключает возможность системы временно увеличивать приоритет потока.                                                                         |
| [**сетсреадстаккгуаранти**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee)         | Задает гарантию стека для вызывающего потока.                                                                                                          |
| [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep)                                             | Приостанавливает выполнение текущего потока в течение заданного интервала.                                                                                    |
| [**слипекс**](/windows/win32/api/synchapi/nf-synchapi-sleepex)                                         | Приостанавливает текущий поток до тех пор, пока не будет выполнено указанное условие.                                                                                         |
| [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)                             | Приостанавливает указанный поток.                                                                                                                            |
| [**свитчтосреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)                           | Позволяет вызвавшему потоку передать выполнение другому потоку, готовому к использованию на текущем процессоре.                                             |
| [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)                         | Завершает поток.                                                                                                                                      |
| [**среадпрок**](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))                                   | Определяемая приложением функция, служащая начальным адресом для потока.                                                                         |
| [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc)                                       | Выделяет индекс локального хранилища потока (TLS).                                                                                                             |
| [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree)                                         | Освобождает индекс TLS.                                                                                                                                     |
| [**тлсжетвалуе**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue)                                 | Получает значение в слоте TLS вызывающего потока для указанного индекса TLS.                                                                           |
| [**тлссетвалуе**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue)                                 | Сохраняет значение в слоте TLS вызывающего потока для указанного индекса TLS.                                                                                |
| [**ваитфоринпутидле**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle)                       | Ожидает, пока указанный процесс не ждет ввода пользователя, не ожидая ввода, или до истечения интервала времени ожидания.                            |



 

## <a name="process-and-thread-extended-attribute-functions"></a>Функции расширенных атрибутов процессов и потоков

Следующие функции используются для задания расширенных атрибутов для создания процессов и потоков.



| Функция                                                                       | Описание                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**делетепроксреадаттрибутелист**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist)         | Удаляет указанный список атрибутов для создания процессов и потоков.                            |
| [**инитиализепроксреадаттрибутелист**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist) | Инициализирует указанный список атрибутов для создания процессов и потоков.                        |
| [**упдатепроксреадаттрибуте**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute)                 | Обновляет указанный атрибут в указанном списке атрибутов для создания процесса и потока. |



 

## <a name="wow64-functions"></a>Функции WOW64

С [WOW64](../winprog64/running-32-bit-applications.md)используются следующие функции.



| Функция                                         | Описание                                                                                                                            |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**IsWow64Message**](/windows/desktop/api/Winuser/nf-winuser-iswow64message)         | Определяет, поступило ли Последнее сообщение, считанное из очереди текущего потока, из процесса WOW64.                              |
| [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)         | Определяет, выполняется ли указанный процесс в эмуляторе WOW64.                                                                       |
| [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2)       | Определяет, выполняется ли указанный процесс в эмуляторе WOW64; также возвращает дополнительные сведения о процессе и архитектуре компьютера. |
| [**Wow64SuspendThread**](/windows/desktop/api/WinBase/nf-winbase-wow64suspendthread) | Приостанавливает указанный поток WOW64.                                                                                                   |



 

## <a name="job-object-functions"></a>Функции объекта задания

Для [объектов заданий](job-objects.md)используются следующие функции.



| Функция                                                       | Описание                                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**ассигнпроцесстожобобжект**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)   | Связывает процесс с существующим объектом Job.                                                    |
| [**креатежобобжект**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)                     | Создает или открывает объект задания.                                                                       |
| [**испроцессинжоб**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)                       | Определяет, выполняется ли процесс в указанном задании.                                      |
| [**опенжобобжект**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta)                         | Открывает существующий объект задания.                                                                        |
| [**куеринформатионжобобжект**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) | Получает сведения о пределу и состоянии задания из объекта задания.                                       |
| [**сетинформатионжобобжект**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)     | Задайте ограничения для объекта задания.                                                                         |
| [**терминатежобобжект**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject)               | Завершает все процессы, связанные в данный момент с заданием.                                          |
| [**усерхандлегрантакцесс**](/windows/desktop/api/Winuser/nf-winuser-userhandlegrantaccess)         | Предоставляет или запрещает доступ к обработчику объекта пользователя для задания с ограничением пользовательского интерфейса. |



 

## <a name="thread-pool-functions"></a>Функции пула потоков

Для [пулов потоков](thread-pools.md)используются следующие функции.



| Функция                                                                                   | Описание                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallbackMayRunLong**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong)                                           | Указывает, что обратный вызов может не возвращаться быстро.                                                                                                                                                                                                 |
| [**канцелсреадпулио**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio)                                           | Отменяет уведомление от функции [**стартсреадпулио**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio) .                                                                                                                                                          |
| [**клосесреадпул**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool)                                                 | Закрывает указанный пул потоков.                                                                                                                                                                                                                   |
| [**клосесреадпулклеанупграуп**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup)                         | Закрывает указанную группу очистки.                                                                                                                                                                                                                 |
| [**CloseThreadpoolCleanupGroupMembers**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers)           | Освобождает члены указанной группы очистки, ожидает завершения всех функций обратного вызова и при необходимости отменяет все невыполненные функции обратного вызова.                                                                                       |
| [**клосесреадпулио**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio)                                             | Освобождает указанный объект завершения ввода-вывода.                                                                                                                                                                                                       |
| [**клосесреадпултимер**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer)                                       | Освобождает указанный объект Timer.                                                                                                                                                                                                                |
| [**клосесреадпулваит**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait)                                         | Освобождает указанный объект Wait.                                                                                                                                                                                                                 |
| [**клосесреадпулворк**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork)                                         | Освобождает указанный рабочий объект.                                                                                                                                                                                                                 |
| [**креатесреадпул**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool)                                               | Выделяет новый пул потоков для выполнения обратных вызовов.                                                                                                                                                                                               |
| [**креатесреадпулклеанупграуп**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup)                       | Создает группу очистки, которую приложения могут использовать для мониторинга одного или нескольких обратных вызовов пула потоков.                                                                                                                                                       |
| [**креатесреадпулио**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio)                                           | Создает новый объект завершения ввода-вывода.                                                                                                                                                                                                                |
| [**креатесреадпултимер**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)                                     | Создает новый объект Timer.                                                                                                                                                                                                                         |
| [**креатесреадпулваит**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait)                                       | Создает новый объект Wait.                                                                                                                                                                                                                          |
| [**креатесреадпулворк**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork)                                       | Создает новый рабочий объект.                                                                                                                                                                                                                          |
| [**дестройсреадпуленвиронмент**](/windows/desktop/api/WinBase/nf-winbase-destroythreadpoolenvironment)                       | Удаляет указанную среду ответного вызова. Вызывайте эту функцию, когда среда ответного вызова больше не требуется для создания новых объектов пула потоков.                                                                                              |
| [**DisassociateCurrentThreadFromCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback)     | Удаляет связь между выполняемой в данный момент функцией обратного вызова и объектом, который инициировал обратный вызов. Текущий поток больше не будет считаться результатом выполнения обратного вызова от имени объекта.                                      |
| [**фрилибраривхенкаллбаккретурнс**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns)                   | Указывает библиотеку DLL, которую пул потоков будет выгружать после завершения текущего обратного вызова.                                                                                                                                                             |
| [**инитиализесреадпуленвиронмент**](/windows/desktop/api/WinBase/nf-winbase-initializethreadpoolenvironment)                 | Инициализирует среду ответного вызова.                                                                                                                                                                                                                 |
| [**иссреадпултимерсет**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset)                                       | Определяет, установлен ли в данный момент указанный объект таймера.                                                                                                                                                                                     |
| [**леавекритикалсектионвхенкаллбаккретурнс**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns) | Указывает критическую секцию, которую пул потоков будет выпустить после завершения текущего обратного вызова.                                                                                                                                               |
| [**куерисреадпулстаккинформатион**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)                 | Возвращает размеры резерва стека и фиксации для потоков в указанном пуле потоков.                                                                                                                                                              |
| [**релеасемутексвхенкаллбаккретурнс**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns)                 | Указывает мьютекс, который пул потоков будет освобождать после завершения текущего обратного вызова.                                                                                                                                                          |
| [**релеасесемафоревхенкаллбаккретурнс**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns)         | Указывает семафор, который пул потоков будет освобождать после завершения текущего обратного вызова.                                                                                                                                                      |
| [**сетевентвхенкаллбаккретурнс**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns)                         | Указывает событие, которое пул потоков будет задавать при завершении текущего обратного вызова.                                                                                                                                                              |
| [**сетсреадпулкаллбаккклеанупграуп**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackcleanupgroup)             | Связывает указанную группу очистки с заданной средой ответного вызова.                                                                                                                                                                     |
| [**сетсреадпулкаллбакклибрари**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbacklibrary)                       | Гарантирует, что указанная библиотека DLL останется загруженной, пока есть необработанные Обратные вызовы.                                                                                                                                                           |
| [**сетсреадпулкаллбаккперсистент**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)                 | Указывает, что обратный вызов должен выполняться в постоянном потоке.                                                                                                                                                                                      |
| [**сетсреадпулкаллбаккпул**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpool)                             | Задает пул потоков, используемый при создании обратных вызовов.                                                                                                                                                                                          |
| [**сетсреадпулкаллбаккприорити**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)                     | Указывает приоритет функции обратного вызова относительно других рабочих элементов в том же пуле потоков.                                                                                                                                                 |
| [**SetThreadpoolCallbackRunsLong**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackrunslong)                     | Указывает, что обратные вызовы, связанные с этой средой ответного вызова, не могут быстро возвращаться.                                                                                                                                                          |
| [**сетсреадпулстаккинформатион**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)                     | Устанавливает размер резервирования и фиксации стека для новых потоков в указанном пуле потоков.                                                                                                                                                               |
| [**SetThreadpoolThreadMaximum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum)                           | Задает максимальное число потоков, которые заданный пул потоков может выделить для обработки обратных вызовов.                                                                                                                                                |
| [**SetThreadpoolThreadMinimum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum)                           | Задает минимальное число потоков, которые указанный пул потоков должен сделать доступными для обработки обратных вызовов.                                                                                                                                         |
| [**сетсреадпултимерекс**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimerex)                                       | Задает объект Timer. Рабочий поток вызывает обратный вызов объекта Timer по истечении заданного времени ожидания.                                                                                                                                       |
| [**SetThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer)                                           | Задает объект Timer. Рабочий поток вызывает обратный вызов объекта Timer по истечении заданного времени ожидания.                                                                                                                                       |
| [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)                                             | Задает объект Wait. Рабочий поток вызывает функцию обратного вызова объекта wait после того, как дескриптор станет сигнальным или после истечения заданного времени ожидания.                                                                                           |
| [**сетсреадпулваитекс**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex)                                         | Задает объект Wait. Рабочий поток вызывает функцию обратного вызова объекта wait после того, как дескриптор станет сигнальным или после истечения заданного времени ожидания.                                                                                           |
| [**стартсреадпулио**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                             | Уведомляет пул потоков о том, что операции ввода-вывода могут начинаться для указанного объекта завершения ввода-вывода. Рабочий поток вызывает функцию обратного вызова объекта завершения ввода-вывода после завершения операции над маркером файла, привязанным к этому объекту. |
| [**SubmitThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork)                                       | Отправляет рабочий объект в пул потоков. Рабочий поток вызывает функцию обратного вызова рабочего объекта.                                                                                                                                                  |
| [**тпинитиализекаллбаккенвирон**](/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron)                         | Инициализирует среду ответного вызова для пула потоков.                                                                                                                                                                                             |
| [**тпдестройкаллбаккенвирон**](/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron)                               | Удаляет указанную среду ответного вызова. Вызывайте эту функцию, когда среда ответного вызова больше не требуется для создания новых объектов пула потоков.                                                                                              |
| [**тпсеткаллбаккактиватионконтекст**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext)                   | Назначает контекст активации среде ответного вызова.                                                                                                                                                                                          |
| [**тпсеткаллбаккклеанупграуп**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup)                             | Связывает указанную группу очистки с заданной средой ответного вызова.                                                                                                                                                                     |
| [**тпсеткаллбаккфинализатионкаллбакк**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback)             | Указывает функцию, вызываемую при завершении работы среды обратного вызова.                                                                                                                                                                            |
| [**тпсеткаллбакклонгфунктион**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction)                             | Указывает, что обратные вызовы, связанные с этой средой ответного вызова, не могут быстро возвращаться.                                                                                                                                                          |
| [**тпсеткаллбаккноактиватионконтекст**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext)               | Указывает, что среда ответного вызова не имеет контекста активации.                                                                                                                                                                                  |
| [**тпсеткаллбаккперсистент**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent)                                 | Указывает, что обратный вызов должен выполняться в постоянном потоке.                                                                                                                                                                                      |
| [**тпсеткаллбаккприорити**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority)                                     | Указывает приоритет функции обратного вызова относительно других рабочих элементов в том же пуле потоков.                                                                                                                                                 |
| [**тпсеткаллбаккрацевисдлл**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll)                               | Гарантирует, что указанная библиотека DLL останется загруженной, пока есть необработанные Обратные вызовы.                                                                                                                                                           |
| [**тпсеткаллбакксреадпул**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool)                                 | Назначает пул потоков среде ответного вызова.                                                                                                                                                                                                    |
| [**TrySubmitThreadpoolCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback)                         | Запрашивает, что рабочий поток пула потоков вызывает указанную функцию обратного вызова.                                                                                                                                                                     |
| [**ваитфорсреадпулиокаллбаккс**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks)                       | Ожидает завершения незавершенных обратных вызовов завершения ввода-вывода и при необходимости отменяет ожидающие обратные вызовы, которые еще не запущены для выполнения.                                                                                                           |
| [**ваитфорсреадпултимеркаллбаккс**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks)                 | Ожидает завершения ожидающих обратных вызовов таймера и при необходимости отменяет ожидающие обратные вызовы, которые еще не запущены для выполнения.                                                                                                                    |
| [**ваитфорсреадпулваиткаллбаккс**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks)                   | Ожидает завершения ожидающих обратных вызовов ожидания, а при необходимости отменяет ожидающие обратные вызовы, которые еще не запущены для выполнения.                                                                                                                     |
| [**WaitForThreadpoolWorkCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks)                   | Ожидает завершения невыполненных рабочих обратных вызовов и при необходимости отменяет ожидающие обратные вызовы, которые еще не запущены для выполнения.                                                                                                                     |



 

Следующие функции являются частью исходного API [пула потоков](thread-pooling.md) .



| Функция                                                            | Описание                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)        | Связывает порт завершения ввода-вывода, принадлежащий пулу потоков, с указанным маркером файла. По завершении запроса ввода-вывода, включающего этот файл, Рабочий поток, не связанный с вводом-выводом, выполнит указанную функцию обратного вызова. |
| [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                      | Помещает рабочий элемент в очередь в рабочий поток в пуле потоков.                                                                                                                                                              |
| [**RegisterWaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) | Направляет поток ожидания в пуле потоков для ожидания объекта.                                                                                                                                                        |
| [**UnregisterWaitEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-unregisterwaitex)                       | Ожидает, пока один или все указанные объекты не помещаются в сигнальное состояние или не истечет интервал времени ожидания.                                                                                                            |



 

## <a name="thread-ordering-service-functions"></a>Функции службы упорядочивания потоков

В [службе упорядочивания потоков](thread-ordering-service.md)используются следующие функции.



| Функция                                                                   | Описание                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**авкуерисистемреспонсивенесс**](/windows/desktop/api/Avrt/nf-avrt-avquerysystemresponsiveness)         | Получает параметр скорости реагирования системы, используемый службой "Планировщик классов мультимедиа". |
| [**аврткреатесреадордерингграуп**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup)     | Создает группу упорядочения потоков.                                                            |
| [**аврткреатесреадордерингграупекс**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroupexa) | Создает группу упорядочения потоков и связывает серверный поток с задачей.               |
| [**авртделетесреадордерингграуп**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup)     | Удаляет указанную группу упорядочения потоков, созданную вызывающим объектом.                          |
| [**авртжоинсреадордерингграуп**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup)         | Присоединяет клиентские потоки к группе упорядочения потоков.                                            |
| [**авртлеавесреадордерингграуп**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup)       | Позволяет клиентским потокам оставлять группу упорядочения потоков.                                    |
| [**авртваитонсреадордерингграуп**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup)     | Позволяет клиентским потокам группы упорядочения потоков ожидать выполнения.        |



 

## <a name="multimedia-class-scheduler-service-functions"></a>Функции службы планировщика классов мультимедиа

Следующие функции используются со [службой планировщика классов мультимедиа](multimedia-class-scheduler-service.md).



| Функция                                                                   | Описание                                                                                           |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**авревертммсреадчарактеристикс**](/windows/desktop/api/Avrt/nf-avrt-avrevertmmthreadcharacteristics) | Указывает, что поток больше не выполняет работу, связанную с указанной задачей.              |
| [**авсетмммакссреадчарактеристикс**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) | Связывает вызывающий поток с указанными задачами.                                               |
| [**авсетммсреадчарактеристикс**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa)       | Связывает вызывающий поток с указанной задачей.                                                |
| [**авсетммсреадприорити**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)                     | Корректирует приоритет потока вызывающего потока относительно других потоков, выполняющих ту же задачу. |



 

## <a name="fiber-functions"></a>Волоконные функции

С [волокнами](fibers.md)используются следующие функции.



| Функция                                                 | Описание                                                                                                  |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**конвертфибертосреад**](/windows/desktop/api/WinBase/nf-winbase-convertfibertothread)     | Преобразует текущее волокное в поток.                                                                    |
| [**конвертсреадтофибер**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber)     | Преобразует текущий поток в волокно.                                                                    |
| [**конвертсреадтофиберекс**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiberex) | Преобразует текущий поток в волокно.                                                                    |
| [**креатефибер**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                       | Выделяет объект Fiber, назначает его стек и настраивает выполнение, начиная с указанного начального адреса. |
| [**креатефиберекс**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)                   | Выделяет объект Fiber, назначает его стек и настраивает выполнение, начиная с указанного начального адреса. |
| [**делетефибер**](/windows/desktop/api/WinBase/nf-winbase-deletefiber)                       | Удаляет существующее волокно.                                                                                   |
| [**фиберпрок**](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine)                           | Определяемая приложением функция, используемая с функцией [**креатефибер**](/windows/desktop/api/WinBase/nf-winbase-createfiber) .                   |
| [**флсаллок**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc)                             | Выделяет индекс оптоволоконного локального хранилища (ФЛС).                                                                 |
| [**флсфри**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree)                               | Освобождает индекс ФЛС.                                                                                       |
| [**флсжетвалуе**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)                       | Извлекает значение для указанного индекса ФЛС в вызываемом сегменте ФЛС Fiber.                               |
| [**флссетвалуе**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)                       | Сохраняет значение в слоте ФЛС в вызывающем Волоке для указанного индекса ФЛС.                                    |
| [**иссреадафибер**](/windows/win32/api/fibersapi/nf-fibersapi-isthreadafiber)                 | Определяет, является ли текущий поток волокным.                                                            |
| [**свитчтофибер**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber)                   | Планирует волокно.                                                                                           |



 

## <a name="numa-support-functions"></a>Функции поддержки NUMA

Следующие функции обеспечивают [поддержку NUMA](numa-support.md).



| Функция                                                                 | Описание                                                                                                                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аллокатеусерфисикалпажеснума**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)  | Резервирует или фиксирует область памяти в пределах виртуального адресного пространства указанного процесса и указывает узел NUMA для физической памяти. |
| [**жетлогикалпроцессоринформатион**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Извлекает сведения о логических процессорах и связанном оборудовании.                                                                                   |
| [**жетнумааваилаблемемориноде**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)         | Извлекает объем памяти, доступный в указанном узле.                                                                                        |
| [**жетнумааваилаблемеморинодикс**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)     | Извлекает объем памяти, доступный в указанном узле, в виде значения USHORT.                                                              |
| [**жетнумахигхестноденумбер**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)             | Возвращает узел, в котором в настоящее время имеется наибольший номер.                                                                                              |
| [**жетнуманоденумберфромхандле**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)       | Извлекает узел NUMA, связанный с базовым устройством, для маркера файла.                                                                       |
| [**жетнуманодепроцессормаск**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)             | Извлекает маску процессора для указанного узла.                                                                                                   |
| [**жетнуманодепроцессормаскекс**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)         | Извлекает маску процессора для указанного узла NUMA в виде значения USHORT.                                                                            |
| [**жетнумапроцессорноде**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                     | Возвращает номер узла для указанного процессора.                                                                                                 |
| [**жетнумапроцессорнодикс**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                 | Получает номер узла указанного логического процессора в виде значения USHORT.                                                                        |
| [**жетнумапроксимитиноде**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                     | Возвращает номер узла для указанного идентификатора близости.                                                                                      |
| [**жетнумапроксимитинодикс**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                 | Получает номер узла в виде значения USHORT для указанного идентификатора близости.                                                                    |
| [**виртуалаллоцекснума**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                        | Резервирует или фиксирует область памяти в пределах виртуального адресного пространства указанного процесса и указывает узел NUMA для физической памяти. |



 

## <a name="processor-functions"></a>Функции процессора

Следующие функции используются с логическими процессорами и [группами процессоров](processor-groups.md).



| Функция                                                                     | Описание                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**жетактивепроцессоркаунт**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)                   | Возвращает число активных процессоров в группе процессоров или в системе.                                       |
| [**жетактивепроцессорграупкаунт**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)         | Возвращает число активных групп процессоров в системе.                                                         |
| [**жеткуррентпроцессорнумбер**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)               | Возвращает номер процессора, на котором выполнялся текущий поток во время вызова этой функции.            |
| [**жеткуррентпроцессорнумберекс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)           | Извлекает группу процессоров и номер логического процессора, в котором выполняется вызывающий поток.            |
| [**жетлогикалпроцессоринформатион**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Извлекает сведения о логических процессорах и связанном оборудовании.                                                 |
| [**жетлогикалпроцессоринформатионекс**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Извлекает сведения о связях логических процессоров и связанного оборудования.                            |
| [**жетмаксимумпроцессоркаунт**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)                 | Возвращает максимальное число логических процессоров, которое может иметь группа процессоров или система.                      |
| [**жетмаксимумпроцессорграупкаунт**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)       | Возвращает максимальное число групп процессоров, которое может иметь система.                                             |
| [**куеридлепроцессорциклетиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime)           | Возвращает время цикла для бездействующего потока каждого процессора в системе.                                        |
| [**куеридлепроцессорциклетимикс**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)       | Извлекает накопленное время цикла для бездействующего потока на каждом логическом процессоре в указанной группе процессоров. |



 

## <a name="user-mode-scheduling-functions"></a>Функции планирования User-Mode

Следующие функции используются с планированием в пользовательском режиме (UMS).



| Функция                                                               | Описание                                                                                               |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**креатеумскомплетионлист**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)             | Создает список завершения UMS.                                                                            |
| [**креатеумссреадконтекст**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)               | Создает контекст потока UMS для представления рабочего потока UMS.                                            |
| [**делетеумскомплетионлист**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)             | Удаляет указанный список завершения UMS. Список должен быть пустым.                                        |
| [**делетеумссреадконтекст**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)               | Удаляет указанный контекст потока UMS. Поток должен быть завершен.                                  |
| [**декуеуеумскомплетионлиститемс**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) | Извлекает рабочие потоки UMS из указанного списка завершения UMS.                                      |
| [**ентерумссчедулингмоде**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)               | Преобразует вызывающий поток в поток планировщика UMS.                                                  |
| [**ексекутеумссреад**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)                           | Запускает указанный рабочий поток UMS.                                                                     |
| [**жеткуррентумссреад**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)                     | Возвращает контекст потока UMS вызывающего потока UMS.                                                 |
| [**жетнекстумслиститем**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)                       | Возвращает следующий контекст потока UMS в списке контекстов потоков UMS.                                     |
| [**жетумскомплетионлистевент**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)         | Извлекает маркер события, связанного с указанным списком завершения UMS.                        |
| [**жетумссистемсреадинформатион**](/windows/desktop/api/WinBase/nf-winbase-getumssystemthreadinformation) | Запрашивает, является ли указанный поток потоком планировщика UMS, рабочим потоком UMS или потоком, не являющимся UMS. |
| [**куерюмссреадинформатион**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)         | Извлекает сведения о указанном рабочем потоке UMS.                                              |
| [**сетумссреадинформатион**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)             | Задает зависящую от приложения контекстную информацию для указанного рабочего потока UMS.                        |
| [*умссчедулерпрок*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)                             | Определяемая приложением функция точки входа планировщика UMS, связанная с списком завершения UMS.         |
| [**умссреадиелд**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)                               | Передает управление потоку планировщика UMS, в котором работает вызывающий рабочий поток UMS.             |



 

## <a name="obsolete-functions"></a>Устаревшие функции

-   [**нтжеткуррентпроцессорнумбер**](ntgetcurrentprocessornumber.md)
-   [**нткуеринформатионпроцесс**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationprocess)
-   [**нткуеринформатионсреад**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationthread)
-   [**винексек**](/windows/desktop/api/WinBase/nf-winbase-winexec)
-   [**звкуеринформатионпроцесс**](zwqueryinformationprocess.md)

 

 
