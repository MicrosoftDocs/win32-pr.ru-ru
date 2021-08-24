---
title: Точки синхронизации
description: Если наборы свойств поддерживаются на том же объекте, что и IStorage, важно помнить о точках синхронизации между базовым хранилищем и хранилищем свойств.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf924458d81003e2cc211ff810ebb714399ac28e91189586491b584cff6a3390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034884"
---
# <a name="synchronization-points"></a>Точки синхронизации

Если наборы свойств поддерживаются на том же объекте, что и [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), важно помнить о точках синхронизации между базовым хранилищем и хранилищем свойств.

В хранилище набора свойств хранится поток набора свойств во внутреннем буфере до тех пор, пока этот буфер не будет зафиксирован с помощью метода [**ипропертистораже:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) . Это верно, когда [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) был открыт в режиме транзакций или в режиме прямого подключения.

 

 




