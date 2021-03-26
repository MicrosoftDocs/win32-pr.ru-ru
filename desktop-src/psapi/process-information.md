---
title: Сведения о процессе
description: Система поддерживает список запущенных процессов. Идентификаторы для этих процессов можно получить, вызвав функцию EnumProcesses. Эта функция заполняет массив значений типа DWORD идентификаторами всех процессов в системе.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338033"
---
# <a name="process-information"></a>Сведения о процессе

Система поддерживает список запущенных процессов. Идентификаторы для этих процессов можно получить, вызвав функцию [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Эта функция заполняет массив значений **типа DWORD** идентификаторами всех процессов в системе.

Многим функциям в PSAPI требуется обработчик процесса. Чтобы получить обработчик процесса для выполняющегося процесса, передайте его идентификатор процесса (полученный из [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) в функцию [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) . Не забудьте вызвать функцию [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) по завершении работы с обработчиком процесса.

 

 