---
description: Несколько процессов могут иметь дескрипторы одного и того же события, мьютекса, семафора или объекта таймера, поэтому эти объекты можно использовать для выполнения синхронизации между процессами.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Синхронизация между процессами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0caf4818a05d526a70a1e3257ec6f86d0279f39ce3cf05a4411e49991db6ba15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886354"
---
# <a name="interprocess-synchronization"></a>Синхронизация между процессами

Несколько процессов могут иметь дескрипторы одного и того же события, мьютекса, семафора или объекта таймера, поэтому эти объекты можно использовать для выполнения синхронизации между процессами. Процесс, создающий объект, может использовать маркер, возвращенный функцией создания ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemaphore-**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)или [**сбой createwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). Другие процессы могут открыть обработчик для объекта, используя его имя или наследование или дублирование. Дополнительные сведения см. в следующих разделах:

-   [Имена объектов](object-names.md)
-   [Наследование объектов](object-inheritance.md)
-   [Дублирование объектов](object-duplication.md)

 

 
