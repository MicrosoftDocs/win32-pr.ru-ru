---
title: Сведения о процессе
description: Система поддерживает список запущенных процессов. Идентификаторы для этих процессов можно получить, вызвав функцию EnumProcesses. Эта функция заполняет массив значений типа DWORD идентификаторами всех процессов в системе.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5facb72f094059997c271cb9f38beaea08981430bba40902d620a23e2875b26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094895"
---
# <a name="process-information"></a>Сведения о процессе

Система поддерживает список запущенных процессов. Идентификаторы для этих процессов можно получить, вызвав функцию [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Эта функция заполняет массив значений **типа DWORD** идентификаторами всех процессов в системе.

Многим функциям в PSAPI требуется обработчик процесса. Чтобы получить обработчик процесса для выполняющегося процесса, передайте его идентификатор процесса (полученный из [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) в функцию [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) . Не забудьте вызвать функцию [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) по завершении работы с обработчиком процесса.

 

 