---
description: Приведите собственную транзакцию (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Приведите собственную транзакцию (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662098"
---
# <a name="bring-your-own-transaction-byot"></a><span data-ttu-id="71dde-103">Приведите собственную транзакцию (BYOT)</span><span class="sxs-lookup"><span data-stu-id="71dde-103">Bring Your Own Transaction (BYOT)</span></span>

<span data-ttu-id="71dde-104">Параметр BYOT позволяет создать компонент с или наследовать внешнюю транзакцию.</span><span class="sxs-lookup"><span data-stu-id="71dde-104">BYOT allows a component to be created with or to inherit an external transaction.</span></span> <span data-ttu-id="71dde-105">То есть компонент, который еще не имеет связанной транзакции, может получить транзакцию.</span><span class="sxs-lookup"><span data-stu-id="71dde-105">That is, a component that does not already have an associated transaction can acquire a transaction.</span></span> <span data-ttu-id="71dde-106">В настоящее время транзакции MTS выполняются автоматически; Указывает, находится ли экземпляр компонента в транзакции во время создания.</span><span class="sxs-lookup"><span data-stu-id="71dde-106">Currently, MTS transactions are automatic; whether a component instance lives in a transaction is determined at creation time.</span></span> <span data-ttu-id="71dde-107">Атрибуты транзакций компонента и его создатель определяют, какая транзакция связана с данным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="71dde-107">The transactional attributes of a component and its creator determine what transaction is associated with a given instance.</span></span> <span data-ttu-id="71dde-108">Во всех случаях MTS управляет временем существования транзакций.</span><span class="sxs-lookup"><span data-stu-id="71dde-108">In all cases, MTS controls transaction lifetimes.</span></span> <span data-ttu-id="71dde-109">COM+ расширяет это значение, позволяя задавать произвольную предварительно существующую транзакцию DTC или TIP в качестве свойства Transaction контекста нового компонента.</span><span class="sxs-lookup"><span data-stu-id="71dde-109">COM+ extends this to allow setting an arbitrary pre-existing DTC or TIP transaction as the transaction property of a new component's context.</span></span> <span data-ttu-id="71dde-110">Это позволяет связать настроенные компоненты с транзакциями, время существования которых регулируется монитором TP, OTS-или СУБД.</span><span class="sxs-lookup"><span data-stu-id="71dde-110">This allows configured components to be associated with transactions whose lifetimes are controlled by a TP monitor, OTS, or DBMS.</span></span>

> [!Note]  
> <span data-ttu-id="71dde-111">Транзакции BYOT следует использовать с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="71dde-111">BYOT transactions must be used with caution.</span></span> <span data-ttu-id="71dde-112">В некоторых ситуациях они могут привести к тому, что транзакция охватывает несколько доменов синхронизации, то есть они разрешают параллелизм с транзакцией, что приводит к условию взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="71dde-112">In certain situations, they can result in a transaction spanning multiple synchronization domains—that is, they allow parallelism with a transaction, causing a deadlock condition.</span></span> <span data-ttu-id="71dde-113">Автоматические транзакции, а не транзакции BYOT, являются предпочтительной моделью программирования для средств записи бизнес-компонентов.</span><span class="sxs-lookup"><span data-stu-id="71dde-113">Automatic transactions, rather than BYOT transactions, are the preferred programming model for writers of business components.</span></span>

 

<span data-ttu-id="71dde-114">Интерфейсы для транзакций BYOT включают интерфейс [**икреатевистрансактионекс**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) и интерфейс [**икреатевистиптрансактионекс**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) .</span><span class="sxs-lookup"><span data-stu-id="71dde-114">The interfaces for BYOT transactions include the [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) interface and the [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) interface.</span></span> <span data-ttu-id="71dde-115">Интерфейс **икреатевистрансактионекс** создает объект, который закрепляется в ручной транзакции.</span><span class="sxs-lookup"><span data-stu-id="71dde-115">The **ICreateWithTransactionEx** interface creates an object that is enlisted within a manual transaction.</span></span> <span data-ttu-id="71dde-116">Интерфейс **икреатевистиптрансактионекс** создает объект, который закрепляется в ручной транзакции с помощью протокола Интернета Transaction (TIP).</span><span class="sxs-lookup"><span data-stu-id="71dde-116">The **ICreateWithTipTransactionEx** interface creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71dde-117">См. также</span><span class="sxs-lookup"><span data-stu-id="71dde-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71dde-118">Наследование ручных транзакций</span><span class="sxs-lookup"><span data-stu-id="71dde-118">Inheriting Manual Transactions</span></span>](inheriting-manual-transactions.md)
</dt> </dl>

 

 



