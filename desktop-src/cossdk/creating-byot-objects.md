---
description: Создание объектов BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Создание объектов BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701212"
---
# <a name="creating-byot-objects"></a>Создание объектов BYOT

Новый объект BYOT создает объекты с ручными транзакциями. Два интерфейса, [**икреатевистрансактионекс**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) и [**икреатевистиптрансактионекс**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), имеют единственный метод **CreateInstance**, который принимает указатель интерфейса **ITransaction** и URL-адрес TIP соответственно. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) возвращает указатель интерфейса на только что созданный объект, который закрепляется в указанной транзакции.

При освобождении объекта с ручной транзакцией COM+ не пытается зафиксировать транзакцию. Транзакция управляется явным образом внешним диспетчером транзакций, который выдает транзакцию, в которой был создан этот объект.

> [!Note]  
> Объект BYOT. Бйотсерверекс необходимо импортировать в приложение COM+.

 

 

 



