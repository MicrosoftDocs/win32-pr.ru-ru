---
description: Существует множество функций для получения сведений о процессах.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Получение дополнительных сведений о процессе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545479"
---
# <a name="obtaining-additional-process-information"></a>Получение дополнительных сведений о процессе

Существует множество функций для получения сведений о процессах. Некоторые из этих функций можно использовать только для вызывающего процесса, так как они не принимают в качестве параметра обработку обработки. Для получения сведений о других процессах можно использовать функции, которые используют обработчик процесса.

-   Чтобы получить строку командной строки для текущего процесса, используйте функцию [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) .
-   Чтобы получить структуру [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) , указанную при создании текущего процесса, используйте функцию [**жетстартупинфо**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) .
-   Чтобы получить сведения о версии из заголовка исполняемого файла, используйте функцию [**жетпроцессверсион**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) .
-   Чтобы получить полный путь и имя файла для исполняемого файла, содержащего код процесса, используйте функцию [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .
-   Чтобы получить количество дескрипторов для используемых объектов графического интерфейса пользователя, используйте функцию [**жетгуиресаурцес**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) .
-   Чтобы определить, выполняется ли отладка процесса, используйте функцию [**исдебугжерпресент**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .
-   Чтобы получить сведения об учетных данных для всех операций ввода-вывода, выполняемых процессом, используйте функцию [**жетпроцессиокаунтерс**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .

 

 
