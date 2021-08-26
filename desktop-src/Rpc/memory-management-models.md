---
title: Модели Memory-Management
description: Модели Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a985158f54bf09d149e04c7eebc5853417e39191ca0bb854cb7d1ba5de1e5d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019984"
---
# <a name="memory-management-models"></a>Модели Memory-Management

Как разработчик, у вас есть несколько вариантов выделения и освобождения памяти. Рассмотрим сложную структуру данных, состоящую из узлов, связанных с указателями, таких как связанный список или дерево. Можно применять атрибуты, которые выбирают одну из следующих моделей:

-   [Выделение и освобождение узлов по](node-by-node-allocation-and-deallocation.md)узлам.
-   [Один линейный буфер, выделенный заглушкой для всего дерева](stub-allocated-buffers.md).
-   [Управление памятью заглушки сервера](server-stub-memory-management.md)
-   [Один линейный буфер, выделенный клиентским приложением для всего дерева](application-allocated-buffer.md).
-   [Постоянное хранилище на сервере](persistent-storage-on-the-server.md).

 

 




