---
description: При создании нового потока функцией CreateThread или Креатеремотесреад возвращается маркер потока.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Дескрипторы потоков и идентификаторы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501d449bdb34d158ad14e52409967d4ef17f62f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909672"
---
# <a name="thread-handles-and-identifiers"></a>Дескрипторы потоков и идентификаторы

При создании нового потока функцией [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) или [**креатеремотесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) возвращается маркер потока. По умолчанию этот обработчик имеет права полного доступа и — подлежит проверке доступа безопасности — может использоваться в любой функции, принимающей обработчик потока. Этот маркер может наследоваться дочерними процессами в зависимости от флага наследования, заданного при его создании. Этот маркер можно дублировать с помощью [**дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle), что позволяет создать обработчик потока с подмножеством прав доступа. Этот маркер действителен до закрытия, даже после завершения потока, который он представляет.

Функции [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) и [**креатеремотесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) также возвращают идентификатор, который уникальным образом идентифицирует поток во всей системе. Поток может использовать функцию [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) для получения собственного идентификатора потока. Идентификаторы действительны с момента создания потока до завершения потока. Обратите внимание, что идентификатор потока никогда не будет равен 0.

Если у вас есть идентификатор потока, можно получить его обработчик, вызвав функцию [**опенсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) . **Опенсреад** позволяет указать права доступа маркера и возможность наследования.

Поток может использовать функцию [**жеткуррентсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) для извлечения *псевдо-обработчика* в собственный объект потока. Этот псевдо-обработчик допустим только для вызывающего процесса; Он не может наследоваться или дублироваться для использования другими процессами. Чтобы получить реальный маркер для потока с учетом псевдо-обработчика, используйте функцию [**дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

Чтобы перечислить потоки процесса, используйте функции [**Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) и [**Thread32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next) .

 

 
