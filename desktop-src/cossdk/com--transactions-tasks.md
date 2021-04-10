---
description: Задачи транзакций COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Задачи транзакций COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142007"
---
# <a name="com-transactions-tasks"></a><span data-ttu-id="ba338-103">Задачи транзакций COM+</span><span class="sxs-lookup"><span data-stu-id="ba338-103">COM+ Transactions Tasks</span></span>

<span data-ttu-id="ba338-104">Хотя автоматическая обработка транзакций в COM+ позволяет тратить более продуктивное время на создание и настройку объектов, которые вы хотите участвовать в автоматических транзакциях, существуют некоторые задачи программирования, которые можно выполнять для адаптации поведения транзакций к требованиям приложения.</span><span class="sxs-lookup"><span data-stu-id="ba338-104">While automatic transaction processing in COM+ allows you to spend more productive development time in creating and configuring objects that you want to participate in automatic transactions, there are some programming tasks you can perform to tailor transaction behavior to your application requirements.</span></span>

<span data-ttu-id="ba338-105">В следующих разделах рассматриваются конкретные параметры программирования, связанные с обработкой транзакций.</span><span class="sxs-lookup"><span data-stu-id="ba338-105">The following topics discuss specific programming options related to transaction processing.</span></span>



| <span data-ttu-id="ba338-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="ba338-106">Topic</span></span>                                                                                             | <span data-ttu-id="ba338-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ba338-107">Description</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba338-108">Установка атрибута Transaction</span><span class="sxs-lookup"><span data-stu-id="ba338-108">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)<br/>             | <span data-ttu-id="ba338-109">Описывает, как устанавливать значения атрибутов транзакции для объектов транзакции.</span><span class="sxs-lookup"><span data-stu-id="ba338-109">Describes how to set transaction attribute values for your transaction objects.</span></span><br/>         |
| [<span data-ttu-id="ba338-110">Установка уровня изоляции транзакций</span><span class="sxs-lookup"><span data-stu-id="ba338-110">Setting the Transaction Isolation Level</span></span>](setting-the-transaction-isolation-level.md)<br/> | <span data-ttu-id="ba338-111">Описывает, как задать уровни изоляции транзакций для объектов транзакции.</span><span class="sxs-lookup"><span data-stu-id="ba338-111">Describes how to set the transaction isolation levels for your transaction objects.</span></span><br/>     |
| [<span data-ttu-id="ba338-112">Задание времени ожидания транзакции</span><span class="sxs-lookup"><span data-stu-id="ba338-112">Setting the Transaction Time-Out</span></span>](setting-the-transaction-time-out.md)<br/>               | <span data-ttu-id="ba338-113">Описывает, как задать интервалы времени ожидания для транзакций.</span><span class="sxs-lookup"><span data-stu-id="ba338-113">Describes how to set time-out intervals for your transactions.</span></span><br/>                          |
| [<span data-ttu-id="ba338-114">Установка флагов consistent и Done</span><span class="sxs-lookup"><span data-stu-id="ba338-114">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)<br/>     | <span data-ttu-id="ba338-115">Показывает, как использовать флаги consistent и Done для управления результатом транзакции.</span><span class="sxs-lookup"><span data-stu-id="ba338-115">Shows how to use the consistent and done flags to control the outcome of a transaction.</span></span><br/> |
| [<span data-ttu-id="ba338-116">Создание объектов BYOT</span><span class="sxs-lookup"><span data-stu-id="ba338-116">Creating BYOT Objects</span></span>](creating-byot-objects.md)<br/>                                     | <span data-ttu-id="ba338-117">Описывает, как создавать объекты, чтобы можно было создать собственную транзакцию (BYOT).</span><span class="sxs-lookup"><span data-stu-id="ba338-117">Describes how to create objects so you can Bring Your Own Transaction (BYOT).</span></span><br/>           |



 

> [!Note]  
> <span data-ttu-id="ba338-118">Как правило, любой компонент, который обновляет постоянное состояние, должен поддерживать транзакции.</span><span class="sxs-lookup"><span data-stu-id="ba338-118">As a general rule, any component that updates persistent state should support transactions.</span></span> <span data-ttu-id="ba338-119">Компоненты, сочетающие операции двух или более объектов в одной задаче, должны использовать транзакции для упрощения восстановления после ошибок.</span><span class="sxs-lookup"><span data-stu-id="ba338-119">Components that combine the operations of two or more objects into a single task should use transactions to simplify error recovery.</span></span> <span data-ttu-id="ba338-120">Кроме того, для освобождения ресурсов, таких как подключения к базам данных, транзакции в COM+ должны быть как можно более короткими.</span><span class="sxs-lookup"><span data-stu-id="ba338-120">Also, to release resources, such as database connections, transactions in COM+ should be as short as you can make them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ba338-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ba338-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba338-122">Концепции транзакций COM+</span><span class="sxs-lookup"><span data-stu-id="ba338-122">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)
</dt> </dl>

 

 




