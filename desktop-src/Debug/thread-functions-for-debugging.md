---
description: Научитесь использовать функцию CreateThread для создания нового потока для процесса. Отладчикам обычно требуется проверять или изменять содержимое регистров потока.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Функции потока для отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403987"
---
# <a name="thread-functions-for-debugging"></a>Функции потока для отладки

Функция [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) создает новый поток для процесса. Отладчикам обычно требуется проверять или изменять содержимое регистров потока. Для этого отладчик должен получить обработчик для потока с помощью функции [**дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) и указать соответствующий доступ к потоку ( \_ \_ контекст Get, контекст набора потоков \_ \_ или и то, и другое). Функция [**опенсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) позволяет отладчику получить идентификатор существующего потока.

Процесс с соответствующим доступом к потоку может проверить регистры потока с помощью функции [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) и установить содержимое регистров потока с помощью функции [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .

Процесс также может получить доступ к потоку \_ приостановки потока \_ . Этот тип доступа позволяет отладчику управлять выполнением потока с помощью функций [**суспендсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) и [**ресумесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) . Дополнительные сведения о потоках см. в разделе [процессы и потоки](../procthread/processes-and-threads.md).

 

 
