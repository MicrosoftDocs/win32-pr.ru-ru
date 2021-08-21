---
description: 'Завершение процесса приводит к следующим результатам: все оставшиеся потоки в процессе отмечаются для завершения. Освобождаются все ресурсы, выделенные процессом. Все объекты ядра закрыты. Код процесса удаляется из памяти. Код завершения процесса задан. Объект процесса получает сигнал.'
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: Завершение процесса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d1a97b2b7342b67eaab72cae244b188df4cfeafbf2875d3bd62136ab6139748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081304"
---
# <a name="terminating-a-process"></a>Завершение процесса

Завершение процесса приводит к следующим результатам.

-   Все оставшиеся потоки в процессе помечаются для завершения.
-   Освобождаются все ресурсы, выделенные процессом.
-   Все объекты ядра закрыты.
-   Код процесса удаляется из памяти.
-   Код завершения процесса задан.
-   Объект процесса получает сигнал.

Хотя открытые дескрипторы для объектов ядра закрываются автоматически при завершении процесса, сами объекты существуют до тех пор, пока не будут закрыты все открытые дескрипторы. Таким образом, объект останется действительным после завершения процесса, который его использует, если другой процесс имеет открытый для него маркер.

Функция [**жетекситкодепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) возвращает состояние завершения процесса. Во время выполнения процесса его состояние завершения остается \_ активным. Когда процесс завершается, его состояние завершения меняется с \_ активного на код выхода процесса.

Когда процесс завершается, состояние объекта процесса получает значение "сигнал", освобождая потоки, ожидающие завершения процесса. Дополнительные сведения о синхронизации см. в разделе [Синхронизация выполнения нескольких потоков](synchronizing-execution-of-multiple-threads.md).

Когда система завершает процесс, она не завершает никакие дочерние процессы, созданные процессом. При завершении процесса не создаются уведомления, которые представляют собой \_ процедуры-обработчики CBT.

Используйте функцию [**сетпроцессшутдовнпараметерс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) , чтобы указать определенные аспекты завершения процесса при завершении работы системы, например, когда процесс должен завершаться относительно других процессов в системе.

## <a name="how-processes-are-terminated"></a>Как прерываются процессы

Процесс выполняется до тех пор, пока не произойдет одно из следующих событий:

-   Любой поток процесса вызывает функцию [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) . Обратите внимание, что некоторые реализации библиотеки времени выполнения C (CRT) вызывают **ExitProcess** , если основной поток процесса возвращает.
-   Последний поток процесса завершается.
-   Любой поток вызывает функцию [**терминатепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) с помощью обработчика для процесса.
-   Для процессов консоли [обработчик управления консоли](/windows/console/console-control-handlers) по умолчанию вызывает [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) , когда консоль получает сигналы CTRL + C или Ctrl + Break.
-   Пользователь завершает работу системы или выходит из нее.

Не завершайте процесс, если его потоки не находятся в известных состояниях. Если поток ожидает объект ядра, он не будет завершен до завершения ожидания. Это может привести к тому, что приложение перестает отвечать на запросы.

Основной поток может избежать завершения других потоков, направляя их для вызова [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) перед завершением процесса (Дополнительные сведения см. в разделе [завершение потока](terminating-a-thread.md)). Основной поток по-прежнему может вызвать [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) , чтобы убедиться, что все потоки завершаются.

Код выхода для процесса — это либо значение, указанное в вызове [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) или [**терминатепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), либо значение, возвращаемое функцией Main или [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) процесса. Если процесс завершается из-за неустранимого исключения, код выхода — это значение исключения, вызвавшего завершение. Кроме того, это значение используется в качестве кода выхода для всех потоков, которые выполнялись в момент возникновения исключения.

Если процесс завершается с помощью [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), система вызывает функцию точки входа каждой ПРИСОЕДИНЕННОЙ библиотеки DLL со значением, указывающим, что процесс отсоединяется от библиотеки DLL. Библиотеки DLL не уведомляются, когда процесс завершается [**терминатепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Дополнительные сведения о библиотеках DLL см. в разделе [библиотеки динамической компоновки](../dlls/dynamic-link-libraries.md).

Если процесс завершается [**терминатепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), все потоки процесса немедленно завершаются без возможности запуска дополнительного кода. Это означает, что поток не выполняет код в блоках обработчика завершения. Кроме того, подключенные библиотеки DLL не уведомляются о том, что процесс отсоединяется. Если требуется, чтобы один процесс завершил другой процесс, выполните следующие шаги, чтобы получить лучшее решение:

-   Оба процесса вызывают функцию [**регистервиндовмессаже**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) для создания частного сообщения.
-   Один процесс может завершить другой процесс, выполнив широковещательную передачу частного сообщения с помощью функции [**броадкастсистеммессаже**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) следующим образом:

    ``` syntax
     DWORD dwRecipients = BSM_APPLICATIONS;
        UINT uMessage = PM_MYMSG;
        WPARAM wParam = 0;
        LPARAM lParam = 0;

        BroadcastSystemMessage( 
            BSF_IGNORECURRENTTASK, // do not send message to this process
            &dwRecipients,         // broadcast only to applications
            uMessage,              // registered private message
            wParam,                // message-specific value
            lParam );              // message-specific value
    ```

-   Процесс, получающий закрытое сообщение, вызывает [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) для завершения выполнения.

Выполнение функций [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**креатеремотесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)и [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) сериализуется в адресном пространстве. Применяются следующие ограничения:

-   Во время запуска процесса и подпрограмм инициализации DLL новые потоки могут быть созданы, но они не начинают выполнение до тех пор, пока инициализация DLL не будет завершена для процесса.
-   Только один поток за раз может находиться в подпрограммых инициализации или отсоединения DLL.
-   Функция [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) не возвращает значение, пока в подпрограммы инициализации или отсоединения DLL нет потоков.

 

 
