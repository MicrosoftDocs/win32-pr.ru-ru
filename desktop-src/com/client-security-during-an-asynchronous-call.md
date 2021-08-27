---
title: Client Security во время асинхронного вызова
description: Client Security во время асинхронного вызова
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4c25e17712d0164938f3de9895d1e6b02582f2d86cba9957297e23aa4e7f1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071044"
---
# <a name="client-security-during-an-asynchronous-call"></a>Client Security во время асинхронного вызова

Диспетчер прокси-сервера, созданный MIDL для объектов, использующих стандартный маршалирование, реализует интерфейс [**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Клиенты могут управлять безопасностью упакованных вызовов, запрашивая **иклиентсекурити** на объекте Call и получая или изменяя параметры безопасности.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Выполнение асинхронного вызова](making-an-asynchronous-call.md)
</dt> </dl>

 

 




