---
description: Транзакции и JIT-активация COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Транзакции и JIT-активация COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896318"
---
# <a name="transactions-and-com-jit-activation"></a><span data-ttu-id="ba38d-103">Транзакции и JIT-активация COM+</span><span class="sxs-lookup"><span data-stu-id="ba38d-103">Transactions and COM+ JIT Activation</span></span>

<span data-ttu-id="ba38d-104">JIT-активация COM+ тесно связана с автоматическими транзакциями.</span><span class="sxs-lookup"><span data-stu-id="ba38d-104">COM+ JIT Activation is closely bound to automatic transactions.</span></span> <span data-ttu-id="ba38d-105">При настройке компонента таким образом, чтобы он требовал транзакции или для него требуется новая транзакция, JIT-активация также включается автоматически.</span><span class="sxs-lookup"><span data-stu-id="ba38d-105">When you configure a component so that it requires a transaction or requires a new transaction, JIT Activation is automatically enabled as well.</span></span> <span data-ttu-id="ba38d-106">Эти две функции естественным образом работают в сочетании.</span><span class="sxs-lookup"><span data-stu-id="ba38d-106">The two features naturally work in conjunction.</span></span> <span data-ttu-id="ba38d-107">Компоненты, активируемые с помощью JIT-активации, имеют следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="ba38d-107">Transactional, JIT-activated components share the following characteristics:</span></span>

-   <span data-ttu-id="ba38d-108">Стателесснесс.</span><span class="sxs-lookup"><span data-stu-id="ba38d-108">Statelessness.</span></span> <span data-ttu-id="ba38d-109">Состояние, которое нарушает изоляцию транзакции, не должно быть заблокировано, а состояние, которое будет потеряно при деактивации объекта, будет утрачено.</span><span class="sxs-lookup"><span data-stu-id="ba38d-109">You would not hold state that would violate transaction isolation nor would you hold state that would be lost on object deactivation.</span></span>

-   <span data-ttu-id="ba38d-110">Быстрое использование.</span><span class="sxs-lookup"><span data-stu-id="ba38d-110">Rapid use.</span></span> <span data-ttu-id="ba38d-111">Шаблон канонического использования для объекта, выполняющего работу в автоматической транзакции, заключается в выполнении некоторых небольших единиц работы, голосования и выходов.</span><span class="sxs-lookup"><span data-stu-id="ba38d-111">The canonical use pattern for an object performing work in an automatic transaction is to do some small unit of work, vote, and exit.</span></span>

    > [!Note]  
    > <span data-ttu-id="ba38d-112">Способы проголосовать за транзакции и сигналы, выполняемые COM+ для JIT-активации, также тесно связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="ba38d-112">The ways that you vote in COM+ transactions and signal doneness for JIT Activation are also closely bound together.</span></span> <span data-ttu-id="ba38d-113">Дополнительные сведения см. [в разделе Установка бита done](setting-the-done-bit.md).</span><span class="sxs-lookup"><span data-stu-id="ba38d-113">For more information, see [Setting the Done Bit](setting-the-done-bit.md).</span></span>

     

-   <span data-ttu-id="ba38d-114">Многократное использование.</span><span class="sxs-lookup"><span data-stu-id="ba38d-114">Repeated use.</span></span> <span data-ttu-id="ba38d-115">Если транзакционная работа правильно разбивается, клиенты используют одни и те же объекты для выполнения небольшого числа атомарных операций.</span><span class="sxs-lookup"><span data-stu-id="ba38d-115">When transactional work is properly broken up, clients use the same objects over and over to perform little parcels of atomic work.</span></span>

-   <span data-ttu-id="ba38d-116">Деактивируется при фиксации или прекращении.</span><span class="sxs-lookup"><span data-stu-id="ba38d-116">Deactivated on commit or abort.</span></span> <span data-ttu-id="ba38d-117">В COM+ все объекты внутри границы транзакции отключаются при фиксации или прерывании транзакции.</span><span class="sxs-lookup"><span data-stu-id="ba38d-117">In COM+, all objects within the transaction boundary are deactivated when the transaction commits or aborts.</span></span>

<span data-ttu-id="ba38d-118">В сочетании с транзакционными компонентами COM+ JIT-активация служит значительным улучшением производительности за счет поддержания канала открытым в качестве клиентов, содержащих долгосрочные ссылки на объекты транзакций.</span><span class="sxs-lookup"><span data-stu-id="ba38d-118">In conjunction with COM+ transactional components, JIT activation serves as a big performance enhancement by keeping the channel open as clients hold long-lived references to transactional objects.</span></span> <span data-ttu-id="ba38d-119">В качестве дополнительных усовершенствований можно выбрать использование пула объектов транзакций для повторного использования ресурсов, которые они содержат, ускорить повторную активацию объектов и управлять использованием ресурсов памяти для заданных объектов.</span><span class="sxs-lookup"><span data-stu-id="ba38d-119">As further enhancements, you can elect to pool the transactional objects to reuse the resources they hold, speed object reactivation time, and closely manage how you use memory resources for given objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba38d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="ba38d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba38d-121">Основные понятия JIT-активации COM+</span><span class="sxs-lookup"><span data-stu-id="ba38d-121">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="ba38d-122">Включение JIT-активации для компонента</span><span class="sxs-lookup"><span data-stu-id="ba38d-122">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="ba38d-123">Объединение объектов в пул и JIT-активация COM+</span><span class="sxs-lookup"><span data-stu-id="ba38d-123">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



