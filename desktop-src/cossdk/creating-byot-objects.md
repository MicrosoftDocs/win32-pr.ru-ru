---
description: Создание объектов BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Создание объектов BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c2f0f999cb758a46dc779d29dac9fdfc71d2dbc245a84d1ca86060108e5663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128769"
---
# <a name="creating-byot-objects"></a>Создание объектов BYOT

Новый объект BYOT создает объекты с ручными транзакциями. Два интерфейса, [**икреатевистрансактионекс**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) и [**икреатевистиптрансактионекс**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), имеют единственный метод **CreateInstance**, который принимает указатель интерфейса **ITransaction** и URL-адрес TIP соответственно. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) возвращает указатель интерфейса на только что созданный объект, который закрепляется в указанной транзакции.

При освобождении объекта с ручной транзакцией COM+ не пытается зафиксировать транзакцию. Транзакция управляется явным образом внешним диспетчером транзакций, который выдает транзакцию, в которой был создан этот объект.

> [!Note]  
> Объект BYOT. Бйотсерверекс необходимо импортировать в приложение COM+.

 

 

 



