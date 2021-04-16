---
description: Дочерний процесс может наследовать несколько свойств и ресурсов от своего родительского процесса.
ms.assetid: c530e723-2d40-4022-a259-dfc650604e44
title: Наследование (процессы и потоки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713fe398360b510fab3c66f5cf74dc07b642dac
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "105672427"
---
# <a name="inheritance"></a>Наследование

Дочерний процесс может наследовать несколько свойств и ресурсов от своего родительского процесса. Кроме того, дочерний процесс может не допустить наследования свойств родительского процесса. Может быть унаследовано следующее:

-   Открытые дескрипторы, возвращаемые функцией [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . К ним относятся дескрипторы файлов, Входные буферы консоли, буферы экранов консоли, именованные каналы, устройства с последовательным обменом данными и маилслотс.
-   Открытые дескрипторы для обработки, потока, мьютекса, события, семафора, именованного канала, анонимного канала и сопоставления файлов. Эти функции возвращаются с помощью функций [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa), [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**createsemaphore-**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), [**креатенамедпипе**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea), [**креатепипе**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)и [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) соответственно.
-   Переменные среды.
-   Текущий каталог.
-   Консоль, если процесс не отсоединяется или не создается новая консоль. Процесс дочерней консоли также может наследовать стандартные дескрипторы родительского элемента, а также доступ к входному буферу и активному буферу экрана.
-   Режим ошибки, заданный функцией [**функцию SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) .
-   Маска сходства процессоров.
-   Ассоциация с заданием.

Дочерний процесс не наследует следующие:

-   Класс Priority.
-   Дескрипторы, возвращаемые [**локалаллок**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**хеапкреате**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)и [**хеапаллок**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc).
-   Псевдо, как в дескрипторах, возвращаемых функцией [**жеткуррентпроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) или [**жеткуррентсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) . Эти дескрипторы допустимы только для вызывающего процесса.
-   Дескрипторы модуля DLL, возвращаемые функцией [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) .
-   GDI или пользовательские дескрипторы, такие как **хбитмап** или **HMENU**.

## <a name="inheriting-handles"></a>Наследование дескрипторов

Дочерний процесс может наследовать некоторые его дескрипторы родителя, но не наследовать другие. Чтобы вызвать наследование маркера, необходимо выполнить два действия:

-   Укажите, что маркер должен наследоваться при создании, открытии или дублировании маркера. Для этой цели в функциях создания обычно используется элемент **бинхерисандле** структуры [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . [**Дупликатехандле**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) использует параметр *бинхерисандлес* .
-   Укажите, что наследуемые дескрипторы наследуются путем установки для параметра *бинхерисандлес* значения true при вызове функции [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Кроме того, для наследования стандартных обработчиков ввода, стандартных выходных данных и стандартных дескрипторов ошибок элемент **dwFlags** структуры [**СТАРТУПИНФО**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) должен включать стартф \_ усестдхандлес.

Чтобы указать список дескрипторов, которые должны наследоваться конкретным дочерним процессом, вызовите функцию [**упдатепроксреадаттрибуте**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) с флагом *PROC_THREAD_ATTRIBUTE_HANDLE_LIST* .

Унаследованный обработчик ссылается на тот же объект в дочернем процессе, что и в родительском процессе. Он также имеет то же значение и привилегии доступа. Таким образом, когда один процесс изменяет состояние объекта, изменение влияет на оба процесса. Чтобы использовать маркер, дочерний процесс должен получить значение Handle и «знает» объект, к которому он относится. Как правило, родительский процесс передает эти сведения дочернему процессу через ее командную строку, блок среды или некоторую форму [межпроцессного взаимодействия](/windows/desktop/ipc/interprocess-communications).

Используйте функцию [**сесандлеинформатион**](/windows/win32/api/handleapi/nf-handleapi-sethandleinformation) для управления наследованием существующего маркера.

## <a name="inheriting-environment-variables"></a>Наследование переменных среды

По умолчанию дочерний процесс наследует переменные среды родительского процесса. Однако [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) позволяет родительскому процессу указывать другой блок переменных среды. Дополнительные сведения см. в разделе [переменные среды](environment-variables.md).

## <a name="inheriting-the-current-directory"></a>Наследование текущего каталога

Функция [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) извлекает текущий каталог вызывающего процесса. По умолчанию дочерний процесс наследует текущий каталог родительского процесса. Однако [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) позволяет родительскому процессу указывать другой текущий каталог для дочернего процесса. Чтобы изменить текущий каталог вызывающего процесса, используйте функцию [**сеткуррентдиректори**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) .
