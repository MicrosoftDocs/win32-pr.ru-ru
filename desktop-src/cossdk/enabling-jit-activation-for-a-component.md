---
description: Включение JIT-активации для компонента
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Включение JIT-активации для компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682352"
---
# <a name="enabling-jit-activation-for-a-component"></a><span data-ttu-id="f218d-103">Включение JIT-активации для компонента</span><span class="sxs-lookup"><span data-stu-id="f218d-103">Enabling JIT Activation for a Component</span></span>

<span data-ttu-id="f218d-104">Необходимо настроить JIT-активацию компонента только в том случае, если он правильно написан для поддержки службы JIT-активации COM+.</span><span class="sxs-lookup"><span data-stu-id="f218d-104">You should configure a component to be JIT activated only when it is correctly written to support the COM+ Just-in-Time (JIT) Activation service.</span></span> <span data-ttu-id="f218d-105">Если компонент деактивируется между вызовами метода, это приведет к потере любого связанного состояния.</span><span class="sxs-lookup"><span data-stu-id="f218d-105">If a component is deactivated between method calls, it will lose any associated state.</span></span> <span data-ttu-id="f218d-106">Учитывая поведение JIT-активации по умолчанию, это маловероятно, если вы не предполагаете его использовать, но необходимо знать о требованиях компонента перед изменением его конфигурации и ожиданиям клиентов, которые будут вызывать компонент.</span><span class="sxs-lookup"><span data-stu-id="f218d-106">Given the default behavior of JIT Activation, this is unlikely to occur when you don't expect it to, but you should be aware of a component's requirements prior to changing its configuration and of the expectations of clients that will be calling the component.</span></span>

> [!Note]  
> <span data-ttu-id="f218d-107">Если компонент настроен для использования транзакций, служба JIT-активации COM+ включается автоматически.</span><span class="sxs-lookup"><span data-stu-id="f218d-107">If a component is configured to require transactions, the COM+ JIT Activation service is enabled automatically.</span></span> <span data-ttu-id="f218d-108">В этом случае отключить ее нельзя.</span><span class="sxs-lookup"><span data-stu-id="f218d-108">You cannot disable it in this case.</span></span> <span data-ttu-id="f218d-109">Дополнительные сведения см. в разделе [Настройка транзакций](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="f218d-109">For more detail, see [Configuring Transactions](configuring-transactions.md).</span></span>

 

<span data-ttu-id="f218d-110">При включении JIT-активации для компонента его атрибут синхронизации устанавливается в значение обязательно для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="f218d-110">When you enable JIT Activation for a component, its synchronization attribute is set to required for that component.</span></span> <span data-ttu-id="f218d-111">В этом случае изменить параметр синхронизации нельзя.</span><span class="sxs-lookup"><span data-stu-id="f218d-111">You cannot change the synchronization setting in this case.</span></span> <span data-ttu-id="f218d-112">Дополнительные сведения см. в разделе [зависимости синхронизации](synchronization-dependencies.md).</span><span class="sxs-lookup"><span data-stu-id="f218d-112">For more detail, see [Synchronization Dependencies](synchronization-dependencies.md).</span></span>

<span data-ttu-id="f218d-113">**Включение JIT-активации**</span><span class="sxs-lookup"><span data-stu-id="f218d-113">**To enable JIT Activation**</span></span>

1.  <span data-ttu-id="f218d-114">В области сведений средства администрирования "службы компонентов" щелкните правой кнопкой мыши компонент, который необходимо настроить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="f218d-114">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="f218d-115">В диалоговом окне Свойства компонента перейдите на вкладку **Активация** .</span><span class="sxs-lookup"><span data-stu-id="f218d-115">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="f218d-116">Чтобы включить JIT-активацию для компонента, установите флажок **включить JIT** -активацию.</span><span class="sxs-lookup"><span data-stu-id="f218d-116">To enable JIT activation for the component, select the **Enable Just In Time Activation** check box.</span></span>

4.  <span data-ttu-id="f218d-117">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f218d-117">Click **OK**.</span></span>

<span data-ttu-id="f218d-118">При включении JIT-активации для компонента можно включить функцию автоматического завершения для любого метода, предоставляемого этим компонентом.</span><span class="sxs-lookup"><span data-stu-id="f218d-118">When you have enabled JIT Activation for a component, you have the option of enabling the auto-done feature for any method exposed by that component.</span></span> <span data-ttu-id="f218d-119">Дополнительные сведения см. [в разделе Включение автоматического завершения для метода](enabling-auto-done-for-a-method.md) .</span><span class="sxs-lookup"><span data-stu-id="f218d-119">See [Enabling Auto-Done for a Method](enabling-auto-done-for-a-method.md) for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f218d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f218d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f218d-121">Включение автоматического завершения для метода</span><span class="sxs-lookup"><span data-stu-id="f218d-121">Enabling Auto-Done for a Method</span></span>](enabling-auto-done-for-a-method.md)
</dt> <dt>

[<span data-ttu-id="f218d-122">Установка бита done</span><span class="sxs-lookup"><span data-stu-id="f218d-122">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



