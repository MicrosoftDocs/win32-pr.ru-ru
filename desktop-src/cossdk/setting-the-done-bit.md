---
description: Установка бита done
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Установка бита done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701264"
---
# <a name="setting-the-done-bit"></a><span data-ttu-id="eaee4-103">Установка бита done</span><span class="sxs-lookup"><span data-stu-id="eaee4-103">Setting the Done Bit</span></span>

<span data-ttu-id="eaee4-104">COM+ будет деактивировать активируемый JIT-компилятором объект на основе состояния свойства контекста, установленного бита, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eaee4-104">COM+ will deactivate a JIT-activated object based on the status of a context property, the done bit, as follows:</span></span>

-   <span data-ttu-id="eaee4-105">Если для установленного бита задано значение true, COM+ деактивирует объект при возврате текущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="eaee4-105">When the done bit is set to True, COM+ deactivates the object when the current method call returns.</span></span>
-   <span data-ttu-id="eaee4-106">Если для установленного бита задано значение false, то объект остается активным при возврате текущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="eaee4-106">When the done bit is set to False, the object remains active when the current method call returns.</span></span>

<span data-ttu-id="eaee4-107">По умолчанию в качестве бита завершения задано значение false при создании объекта и инициализации его контекста.</span><span class="sxs-lookup"><span data-stu-id="eaee4-107">By default, the done bit is set to False when an object is created and its context initialized.</span></span> <span data-ttu-id="eaee4-108">(Любой JIT-активируемый объект создается в собственном контексте, поэтому для него задается собственный бит done.) Однако этот параметр по умолчанию можно изменить отдельно для каждого метода с помощью свойства Автозаполнение.</span><span class="sxs-lookup"><span data-stu-id="eaee4-108">(Any JIT-activated object is created in its own context so that it has its own done bit to set.) However, you can change this default setting on a per-method basis by using the auto-done property.</span></span> <span data-ttu-id="eaee4-109">Установить бит завершения можно следующими способами.</span><span class="sxs-lookup"><span data-stu-id="eaee4-109">You can set the done bit in the following ways:</span></span>

-   <span data-ttu-id="eaee4-110">Использование [ **иконтекстстате**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="eaee4-110">Using [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span></span>
-   <span data-ttu-id="eaee4-111">Использование [ **иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="eaee4-111">Using [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span></span>
-   <span data-ttu-id="eaee4-112">Использование свойства автоматического завершения</span><span class="sxs-lookup"><span data-stu-id="eaee4-112">Using the auto-done property</span></span>

## <a name="using-icontextstate"></a><span data-ttu-id="eaee4-113">Использование Иконтекстстате</span><span class="sxs-lookup"><span data-stu-id="eaee4-113">Using IContextState</span></span>

<span data-ttu-id="eaee4-114">Можно использовать [**иконтекстстате:: сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) , чтобы задать для бита done значение true или false.</span><span class="sxs-lookup"><span data-stu-id="eaee4-114">You can use [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) to set the done bit to True or False.</span></span>

<span data-ttu-id="eaee4-115">Вы можете использовать [**иконтекстстате:: жетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) для получения текущего состояния завершенного бита из контекста объекта.</span><span class="sxs-lookup"><span data-stu-id="eaee4-115">You can use [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) to get the current status of the done bit from the object context.</span></span>

## <a name="using-iobjectcontext"></a><span data-ttu-id="eaee4-116">Использование Иобжектконтекст</span><span class="sxs-lookup"><span data-stu-id="eaee4-116">Using IObjectContext</span></span>

<span data-ttu-id="eaee4-117">Вы можете использовать следующие методы в [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) для установки установленного бита при одновременной установке одинакового бита, используемого для голосования в транзакциях:</span><span class="sxs-lookup"><span data-stu-id="eaee4-117">You can use the following methods on [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) to set the done bit while simultaneously setting the consistent bit used for voting in transactions:</span></span>

-   <span data-ttu-id="eaee4-118">[**Сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) сигнализирует, что вы сделали, и проголосуем за фиксацию текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="eaee4-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signals both that you are done and that you vote to commit the current transaction.</span></span> <span data-ttu-id="eaee4-119">Он устанавливает для битов и последовательный бит значение true.</span><span class="sxs-lookup"><span data-stu-id="eaee4-119">It sets both the done bit and the consistent bit to True.</span></span>
-   <span data-ttu-id="eaee4-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) сигнализирует о завершении и думс текущую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="eaee4-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signals that you are done and dooms the current transaction.</span></span> <span data-ttu-id="eaee4-121">Он устанавливает для аргумента Done значение true, а для бита — значение false.</span><span class="sxs-lookup"><span data-stu-id="eaee4-121">It sets the done bit to True and the consistent bit to False.</span></span>
-   <span data-ttu-id="eaee4-122">[**Енаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) сигнализирует о том, что вы не сделали, но проголосуем за фиксацию транзакции.</span><span class="sxs-lookup"><span data-stu-id="eaee4-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signals that you are not done but that you vote to commit the transaction.</span></span> <span data-ttu-id="eaee4-123">Он устанавливает для аргумента Done значение false, а для бита — значение true.</span><span class="sxs-lookup"><span data-stu-id="eaee4-123">It sets the done bit to False and the consistent bit to True.</span></span>
-   <span data-ttu-id="eaee4-124">[**Дисаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) сигнализирует о том, что вы не сделали, и вы не зафиксировали транзакцию в данный момент, обычно потому, что состояние не согласуется.</span><span class="sxs-lookup"><span data-stu-id="eaee4-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signals that you are not done and that you vote not to commit the transaction at this time, usually because the state is inconsistent.</span></span> <span data-ttu-id="eaee4-125">Он устанавливает как бит завершения, так и последовательный бит в значение false.</span><span class="sxs-lookup"><span data-stu-id="eaee4-125">It sets both the done bit and the consistent bit to False.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaee4-126">См. также</span><span class="sxs-lookup"><span data-stu-id="eaee4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaee4-127">Основные понятия JIT-активации COM+</span><span class="sxs-lookup"><span data-stu-id="eaee4-127">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="eaee4-128">Включение JIT-активации для компонента</span><span class="sxs-lookup"><span data-stu-id="eaee4-128">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="eaee4-129">Объединение объектов в пул и JIT-активация COM+</span><span class="sxs-lookup"><span data-stu-id="eaee4-129">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[<span data-ttu-id="eaee4-130">Транзакции и JIT-активация COM+</span><span class="sxs-lookup"><span data-stu-id="eaee4-130">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



