---
description: Несколько процессов могут иметь дескрипторы одного и того же события, мьютекса, семафора или объекта таймера, поэтому эти объекты можно использовать для выполнения синхронизации между процессами.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Синхронизация между процессами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c18fb26d6a64fdc2d785d16c7bccb8b007c3f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663882"
---
# <a name="interprocess-synchronization"></a>Синхронизация между процессами

Несколько процессов могут иметь дескрипторы одного и того же события, мьютекса, семафора или объекта таймера, поэтому эти объекты можно использовать для выполнения синхронизации между процессами. Процесс, создающий объект, может использовать маркер, возвращенный функцией создания ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemaphore-**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)или [**сбой createwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). Другие процессы могут открыть обработчик для объекта, используя его имя или наследование или дублирование. Дополнительные сведения см. в следующих разделах:

-   [Имена объектов](object-names.md)
-   [Наследование объектов](object-inheritance.md)
-   [Дублирование объектов](object-duplication.md)

 

 
