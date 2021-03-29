---
title: Точки синхронизации
description: Если наборы свойств поддерживаются на том же объекте, что и IStorage, важно помнить о точках синхронизации между базовым хранилищем и хранилищем свойств.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780102"
---
# <a name="synchronization-points"></a>Точки синхронизации

Если наборы свойств поддерживаются на том же объекте, что и [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), важно помнить о точках синхронизации между базовым хранилищем и хранилищем свойств.

В хранилище набора свойств хранится поток набора свойств во внутреннем буфере до тех пор, пока этот буфер не будет зафиксирован с помощью метода [**ипропертистораже:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) . Это верно, когда [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) был открыт в режиме транзакций или в режиме прямого подключения.

 

 




