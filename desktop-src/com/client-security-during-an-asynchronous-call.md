---
title: Client Security во время асинхронного вызова
description: Client Security во время асинхронного вызова
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778473"
---
# <a name="client-security-during-an-asynchronous-call"></a>Client Security во время асинхронного вызова

Диспетчер прокси-сервера, созданный MIDL для объектов, использующих стандартный маршалирование, реализует интерфейс [**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Клиенты могут управлять безопасностью упакованных вызовов, запрашивая **иклиентсекурити** на объекте Call и получая или изменяя параметры безопасности.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Выполнение асинхронного вызова](making-an-asynchronous-call.md)
</dt> </dl>

 

 




