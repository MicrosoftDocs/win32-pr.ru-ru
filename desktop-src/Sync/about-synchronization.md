---
description: Чтобы синхронизировать доступ к ресурсу, используйте один из объектов синхронизации в одной из функций ожидания.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Сведения о синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8bca156eec523b30d8f28df8b18a24d9691a33598f5dfe985e4b6b9756ffe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886408"
---
# <a name="about-synchronization"></a>Сведения о синхронизации

Чтобы синхронизировать доступ к ресурсу, используйте один из [объектов синхронизации](synchronization-objects.md) в одной из [функций ожидания](wait-functions.md). Состояние объекта синхронизации — « *сигнальный* » или « *несигнальный*». Функции Wait позволяют потоку блокировать свое выполнение, пока для заданного несигнального объекта не будет установлено сигнальное состояние. Дополнительные сведения см. в разделе [межпроцессная синхронизация](interprocess-synchronization.md).

Ниже приведены другие механизмы синхронизации.

-   [перекрывающиеся входные и выходные данные](synchronization-and-overlapped-input-and-output.md)
-   [асинхронные вызовы процедур](asynchronous-procedure-calls.md)
-   [объекты критических секций](critical-section-objects.md)
-   [переменные условий](condition-variables.md)
-   [Упрощенные блокировки потоков чтения/записи](slim-reader-writer--srw--locks.md)
-   [однократная инициализация](one-time-initialization.md)
-   [доступ к блокируемым переменным](interlocked-variable-access.md)
-   [взаимозаблокированные однонаправленные списки](interlocked-singly-linked-lists.md)
-   [очереди таймера](timer-queues.md)
-   макрос [**меморибарриер**](/windows/win32/api/winnt/nf-winnt-memorybarrier)

Дополнительные сведения о синхронизации см. в разделе [проблемы синхронизации и многопроцессорной обработки](synchronization-and-multiprocessor-issues.md).

 

 
