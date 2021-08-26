---
title: Реализация Server-Sideного канала
description: Серверным программам для распределенных приложений, использующих каналы, не требуется реализовывать какие-либо функции push, Pull или Alloc.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5cf7a928c58890e618c9a62cf1df77fe3d00a7ef9d013240d66e57e88a1584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017698"
---
# <a name="server-side-pipe-implementation"></a>Реализация Server-Sideного канала

Серверным программам для распределенных приложений, использующих каналы, не требуется реализовывать какие-либо функции push, Pull или Alloc. Они должны содержать процедуры, которые клиенты могут вызывать удаленно для инициации передачи данных. В следующих разделах в этом разделе объясняется, как можно реализовать удаленные процедуры на сервере.

-   [Реализация входных каналов на сервере](implementing-input-pipes-on-the-server.md)
-   [Реализация выходных каналов на сервере](implementing-output-pipes-on-the-server.md)

 

 




