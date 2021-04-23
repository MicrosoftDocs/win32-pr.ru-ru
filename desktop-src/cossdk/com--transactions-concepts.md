---
description: Концепции транзакций COM+
ms.assetid: e2198514-c403-4b31-8c8c-0b1c83c4f936
title: Концепции транзакций COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775537128aa0419d02ad3ab614a3ba2ec5eb5b2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142010"
---
# <a name="com-transactions-concepts"></a><span data-ttu-id="01a89-103">Концепции транзакций COM+</span><span class="sxs-lookup"><span data-stu-id="01a89-103">COM+ Transactions Concepts</span></span>

<span data-ttu-id="01a89-104">Хотя COM+ обрабатывает много трудоемких сведений о программировании, связанных с обработкой транзакций, полезно иметь концептуальное представление о теории транзакций, когда необходимо программировать транзакции в COM+.</span><span class="sxs-lookup"><span data-stu-id="01a89-104">Although COM+ handles many of the tedious programming details associated with transaction processing, it is useful to have a conceptual understanding of transaction theory when you need to program transactions in COM+.</span></span>

<span data-ttu-id="01a89-105">В разделах, приведенных в следующей таблице, рассматриваются понятия, относящиеся к обработке транзакций.</span><span class="sxs-lookup"><span data-stu-id="01a89-105">The topics described in the following table cover the concepts that apply to transaction processing.</span></span>



| <span data-ttu-id="01a89-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="01a89-106">Topic</span></span>                                                                                                                     | <span data-ttu-id="01a89-107">Описание</span><span class="sxs-lookup"><span data-stu-id="01a89-107">Description</span></span>                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01a89-108">Свойства ACID</span><span class="sxs-lookup"><span data-stu-id="01a89-108">ACID Properties</span></span>](acid-properties.md)<br/>                                                                         | <span data-ttu-id="01a89-109">Описывает атомарные, последовательные, изолированные и устойчивые свойства транзакций.</span><span class="sxs-lookup"><span data-stu-id="01a89-109">Describes the atomic, consistent, isolated, and durable properties of transactions.</span></span><br/>                                                                                              |
| [<span data-ttu-id="01a89-110">Настройка транзакций</span><span class="sxs-lookup"><span data-stu-id="01a89-110">Configuring Transactions</span></span>](configuring-transactions.md)<br/>                                                       | <span data-ttu-id="01a89-111">Описывает значения атрибутов транзакций, которые можно назначить компонентам для определения степени защиты транзакций, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="01a89-111">Describes the transaction attribute values that you can assign to your components to determine the degree of transaction protection to be enforced.</span></span><br/>                              |
| [<span data-ttu-id="01a89-112">Настройка уровней изоляции транзакций</span><span class="sxs-lookup"><span data-stu-id="01a89-112">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)<br/>                       | <span data-ttu-id="01a89-113">Описывает уровни изоляции, которые можно назначить транзакциям, что позволяет увеличивать или уменьшать параллелизм в зависимости от требований к производительности и масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="01a89-113">Describes the isolation levels you can assign to your transactions, enabling you to increase or decrease concurrency depending on your performance and scalability requirements.</span></span><br/> |
| [<span data-ttu-id="01a89-114">Управление автоматическими транзакциями в COM+</span><span class="sxs-lookup"><span data-stu-id="01a89-114">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)<br/>                         | <span data-ttu-id="01a89-115">Обзор автоматизированного процесса транзакций, поддерживаемого COM+.</span><span class="sxs-lookup"><span data-stu-id="01a89-115">Overview of the automated transaction process supported by COM+.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="01a89-116">Использование нетранзакционных компонентов в транзакции</span><span class="sxs-lookup"><span data-stu-id="01a89-116">Using Non-Transactional Components in a Transaction</span></span>](using-non-transactional-components-in-a-transaction.md)<br/> | <span data-ttu-id="01a89-117">Описывает использование нетранзакционных компонентов в транзакции и их использование.</span><span class="sxs-lookup"><span data-stu-id="01a89-117">Describes how to use non-transactional components in a transaction and when you would use them.</span></span><br/>                                                                                  |
| [<span data-ttu-id="01a89-118">Приведите собственную транзакцию (BYOT)</span><span class="sxs-lookup"><span data-stu-id="01a89-118">Bring Your Own Transaction (BYOT)</span></span>](bring-your-own-transaction--byot-.md)<br/>                                     | <span data-ttu-id="01a89-119">Описывает, как разрешить компоненту наследовать внешнюю транзакцию.</span><span class="sxs-lookup"><span data-stu-id="01a89-119">Describes how to allow a component inherit an external transaction.</span></span><br/>                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="01a89-120">См. также</span><span class="sxs-lookup"><span data-stu-id="01a89-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01a89-121">Задачи транзакций COM+</span><span class="sxs-lookup"><span data-stu-id="01a89-121">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)
</dt> </dl>

 

 




