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
# <a name="creating-byot-objects"></a><span data-ttu-id="41da6-103">Создание объектов BYOT</span><span class="sxs-lookup"><span data-stu-id="41da6-103">Creating BYOT Objects</span></span>

<span data-ttu-id="41da6-104">Новый объект BYOT создает объекты с ручными транзакциями.</span><span class="sxs-lookup"><span data-stu-id="41da6-104">A new BYOT object creates objects with manual transactions.</span></span> <span data-ttu-id="41da6-105">Два интерфейса, [**икреатевистрансактионекс**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) и [**икреатевистиптрансактионекс**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), имеют единственный метод **CreateInstance**, который принимает указатель интерфейса **ITransaction** и URL-адрес TIP соответственно.</span><span class="sxs-lookup"><span data-stu-id="41da6-105">The two interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) and [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), have a single method, **CreateInstance**, which take an **ITransaction** interface pointer and TIP URL, respectively.</span></span> <span data-ttu-id="41da6-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) возвращает указатель интерфейса на только что созданный объект, который закрепляется в указанной транзакции.</span><span class="sxs-lookup"><span data-stu-id="41da6-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) returns an interface pointer to the newly created object, which is enlisted within the specified transaction.</span></span>

<span data-ttu-id="41da6-107">При освобождении объекта с ручной транзакцией COM+ не пытается зафиксировать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="41da6-107">When an object with a manual transaction is released, COM+ does not attempt to commit the transaction.</span></span> <span data-ttu-id="41da6-108">Транзакция управляется явным образом внешним диспетчером транзакций, который выдает транзакцию, в которой был создан этот объект.</span><span class="sxs-lookup"><span data-stu-id="41da6-108">The transaction is controlled explicitly by the external transaction manager that dispensed the transaction under which this object had been created.</span></span>

> [!Note]  
> <span data-ttu-id="41da6-109">Объект BYOT. Бйотсерверекс необходимо импортировать в приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="41da6-109">The Byot.ByotServerEx object needs to be imported into a COM+ application.</span></span>

 

 

 



