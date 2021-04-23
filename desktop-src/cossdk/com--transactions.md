---
description: Транзакции COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Транзакции COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423401"
---
# <a name="com-transactions"></a><span data-ttu-id="6a306-103">Транзакции COM+</span><span class="sxs-lookup"><span data-stu-id="6a306-103">COM+ Transactions</span></span>

<span data-ttu-id="6a306-104">При покупке книги из Интернет-магазина вы используете кредитную карту для торговли денег на книгу.</span><span class="sxs-lookup"><span data-stu-id="6a306-104">When you purchase a book from an online bookstore, you use a credit card to trade money for a book.</span></span> <span data-ttu-id="6a306-105">После отправки заказа серия связанных операций (Проверка кредитной карты, проверка доступности запасов и т. д.) гарантирует, что вы получаете книгу и ваш магазин получает деньги.</span><span class="sxs-lookup"><span data-stu-id="6a306-105">After you submit your order, a series of related operations (validation of your credit card, verification of inventory availability, and so forth) ensures that you get the book and that the bookstore gets your money.</span></span> <span data-ttu-id="6a306-106">Если одна операция в ряде завершается сбоем во время обмена, происходит сбой всего обмена.</span><span class="sxs-lookup"><span data-stu-id="6a306-106">If a single operation in the series fails during the exchange, the entire exchange fails.</span></span> <span data-ttu-id="6a306-107">Вы не получаете книгу, и книжный магазин не получает денег.</span><span class="sxs-lookup"><span data-stu-id="6a306-107">You do not get the book, and the bookstore does not get your money.</span></span>

<span data-ttu-id="6a306-108">Технология, ответственная за обеспечение сбалансированного и предсказуемого подключения Exchange в Интернете, называется *обработкой транзакций*.</span><span class="sxs-lookup"><span data-stu-id="6a306-108">The technology responsible for making this online exchange balanced and predictable is called *transaction processing*.</span></span> <span data-ttu-id="6a306-109">В программном виде *транзакция* — это единица работы, в которой выполняется ряд операций.</span><span class="sxs-lookup"><span data-stu-id="6a306-109">Programmatically, a *transaction* is a unit of work in which a series of operations occur.</span></span> <span data-ttu-id="6a306-110">COM+ использует программные транзакции, чтобы гарантировать, что ресурсы не обновляются постоянно, пока все операции в рамках транзакции не будут успешно выполнены.</span><span class="sxs-lookup"><span data-stu-id="6a306-110">COM+ uses programmatic transactions to ensure that resources are not permanently updated unless all operations within the transaction complete successfully.</span></span> <span data-ttu-id="6a306-111">Привязывая набор связанных операций вместе в транзакцию COM+, которая полностью завершается успешно или полностью завершается сбоем, можно значительно упростить восстановление после ошибок.</span><span class="sxs-lookup"><span data-stu-id="6a306-111">By binding a set of related operations together in a COM+ transaction that either completely succeeds or completely fails, you can vastly simplify error recovery.</span></span>

<span data-ttu-id="6a306-112">В следующих разделах приводится описание общей теории обработки транзакций, более подробное рассмотрение транзакций в COM+ и представлены практические советы по написанию транзакционных компонентов.</span><span class="sxs-lookup"><span data-stu-id="6a306-112">The following topics introduce general transaction processing theory, provide a closer look at transactions in COM+, and present practical tips for writing transactional components.</span></span>



| <span data-ttu-id="6a306-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="6a306-113">Topic</span></span>                                                                   | <span data-ttu-id="6a306-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6a306-114">Description</span></span>                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="6a306-115">Концепции транзакций COM+</span><span class="sxs-lookup"><span data-stu-id="6a306-115">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)<br/> | <span data-ttu-id="6a306-116">Представляет основные термины и понятия.</span><span class="sxs-lookup"><span data-stu-id="6a306-116">Presents basic terms and concepts.</span></span><br/>                                  |
| [<span data-ttu-id="6a306-117">Задачи транзакций COM+</span><span class="sxs-lookup"><span data-stu-id="6a306-117">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)<br/>       | <span data-ttu-id="6a306-118">Предоставляет практическую информацию о написании транзакционных компонентов.</span><span class="sxs-lookup"><span data-stu-id="6a306-118">Provides practical information on writing transactional components.</span></span><br/> |



 

 

 




