---
title: Реализация Server-Sideного канала
description: Серверным программам для распределенных приложений, использующих каналы, не требуется реализовывать какие-либо функции push, Pull или Alloc.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6927350e10061850c5fac0ab0db7c18570dd2bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068232"
---
# <a name="server-side-pipe-implementation"></a>Реализация Server-Sideного канала

Серверным программам для распределенных приложений, использующих каналы, не требуется реализовывать какие-либо функции push, Pull или Alloc. Они должны содержать процедуры, которые клиенты могут вызывать удаленно для инициации передачи данных. В следующих разделах в этом разделе объясняется, как можно реализовать удаленные процедуры на сервере.

-   [Реализация входных каналов на сервере](implementing-input-pipes-on-the-server.md)
-   [Реализация выходных каналов на сервере](implementing-output-pipes-on-the-server.md)

 

 




