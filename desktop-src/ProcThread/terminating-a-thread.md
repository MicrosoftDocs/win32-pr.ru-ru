---
description: 'Завершение потока приводит к следующим результатам: все ресурсы, принадлежащие потоку, например окна и перехватчики, освобождаются. Код завершения потока задан. Объект потока получает сигнал. Если поток является единственным активным потоком в процессе, процесс завершается. Дополнительные сведения см. в разделе Завершение процесса.'
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: "  Завершение потока"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada421356666316072aabff8281787cc140ad114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673732"
---
# <a name="terminating-a-thread"></a>  Завершение потока

Завершение потока приводит к следующим результатам.

-   Все ресурсы, принадлежащие потоку, например Windows и перехватчики, освобождаются.
-   Код завершения потока задан.
-   Объект потока получает сигнал.
-   Если поток является единственным активным потоком в процессе, процесс завершается. Дополнительные сведения см. в разделе [Завершение процесса](terminating-a-process.md).

Функция [**жетекситкодесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) возвращает состояние завершения потока. Во время выполнения потока его состояние завершения остается \_ активным. Когда поток завершается, его состояние завершения изменяется с по-прежнему \_ активным на код выхода потока.

Когда поток завершается, состояние объекта потока изменяется на сигнальное, освобождая все потоки, ожидающие завершения потока. Дополнительные сведения о синхронизации см. в разделе [Синхронизация выполнения нескольких потоков](synchronizing-execution-of-multiple-threads.md).

Когда поток завершается, его объект потока не освобождается, пока все открытые дескрипторы потока не будут закрыты.

## <a name="how-threads-are-terminated"></a>Завершение потоков

Поток выполняется до тех пор, пока не произойдет одно из следующих событий:

-   Поток вызывает функцию [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) .
-   Любой поток процесса вызывает функцию [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) .
-   Функция потока возвращает.
-   Любой поток вызывает функцию [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) с помощью обработчика потока.
-   Любой поток вызывает функцию [**терминатепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) с помощью обработчика для процесса.

Кодом выхода для потока является либо значение, указанное в вызове [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)или [**терминатепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), либо значение, возвращаемое функцией потока.

Если поток завершается с помощью [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), система вызывает функцию точки входа каждой ПРИСОЕДИНЕННОЙ библиотеки DLL со значением, указывающим, что поток отсоединяется от библиотеки DLL (если только не вызвана функция [**дисаблесреадлибрарикаллс**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) ). Если поток завершается с помощью [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), функции точки входа библиотеки DLL вызываются один раз, чтобы указать, что процесс отсоединяется. Библиотеки DLL не получают уведомления при завершении потока с помощью [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) или [**терминатепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Дополнительные сведения о библиотеках DLL см. в разделе [библиотеки динамической компоновки](../dlls/dynamic-link-libraries.md).

Функции [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) и [**терминатепроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) следует использовать только в экстремальных обстоятельствах, так как они не допускают очистки потоков, не уведомляют подключенные библиотеки DLL и не освобождают начальный стек. Кроме того, дескрипторы объектов, принадлежащих потоку, не закрываются до завершения процесса. Следующие шаги обеспечивают лучшее решение:

-   Создайте объект события с помощью функции [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .
-   Создайте потоки.
-   Каждый поток отслеживает состояние события, вызывая функцию [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) . Используйте нулевой интервал времени ожидания.
-   Каждый поток завершает свое собственное выполнение, если событие установлено в сигнальное состояние ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) ВОЗВРАЩАЕТ \_ объект ожидания \_ 0).

 

 
