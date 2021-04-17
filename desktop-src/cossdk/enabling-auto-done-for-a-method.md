---
description: Функцию автоматического завершения можно включить для любого метода, предоставляемого компонентом, для которого включена JIT-активация COM+. Если JIT-активация отключена, автозавершение недоступно.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Включение автоматического завершения для метода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710777"
---
# <a name="enabling-auto-done-for-a-method"></a><span data-ttu-id="41a14-104">Включение автоматического завершения для метода</span><span class="sxs-lookup"><span data-stu-id="41a14-104">Enabling Auto-Done for a Method</span></span>

<span data-ttu-id="41a14-105">Функцию автоматического завершения можно включить для любого метода, предоставляемого компонентом, для которого включена JIT-активация COM+.</span><span class="sxs-lookup"><span data-stu-id="41a14-105">You can enable the auto-done feature for any method exposed by a component for which COM+ JIT activation is enabled.</span></span> <span data-ttu-id="41a14-106">Если JIT-активация отключена, автозавершение недоступно.</span><span class="sxs-lookup"><span data-stu-id="41a14-106">If JIT activation is disabled, auto-done is unavailable.</span></span>

<span data-ttu-id="41a14-107">Необходимо включить Автозаполнение только для метода, который намеренно написал, чтобы воспользоваться его преимуществами, поскольку эта функция потенциально может изменить ожидаемое поведение метода.</span><span class="sxs-lookup"><span data-stu-id="41a14-107">You should enable auto-done only for a method that has intentionally been written to take advantage of it because this feature can potentially change the expected behavior of the method.</span></span>

<span data-ttu-id="41a14-108">При включении функции автозавершения изменяется поведение JIT-активации и автоматических транзакций для этого метода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41a14-108">When you enable auto-done, you are changing the default behavior of both JIT activation and automatic transactions for that method.</span></span> <span data-ttu-id="41a14-109">Вы можете использовать эту функцию, так как она может устранить необходимость явного объявления согласованности и завершения.</span><span class="sxs-lookup"><span data-stu-id="41a14-109">You may want to use this feature because it can remove the necessity to explicitly declare consistency and doneness.</span></span> <span data-ttu-id="41a14-110">Это можно сделать, просто возвращая HRESULT, если включено автозаполнение.</span><span class="sxs-lookup"><span data-stu-id="41a14-110">This can instead be done by simply returning an HRESULT when auto-done is enabled.</span></span> <span data-ttu-id="41a14-111">По сути, при включении автоматического завершения вы указываете COM+ сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="41a14-111">Essentially, when you enable auto-done, you are instructing COM+ to do the following:</span></span>

-   <span data-ttu-id="41a14-112">Установите бит done равным true по умолчанию для контекста, в котором объект выполняется при каждом вызове метода.</span><span class="sxs-lookup"><span data-stu-id="41a14-112">Set the done bit to True by default on the context in which the object runs whenever this method is called.</span></span>
-   <span data-ttu-id="41a14-113">Проверьте значение HRESULT, возвращенное методом. Если оно указывает на успешное выполнение или сбой, задайте соответствующим образом бит согласованности.</span><span class="sxs-lookup"><span data-stu-id="41a14-113">Inspect the HRESULT returned by the method; if it indicates SUCCESS or FAILURE, set the consistency bit accordingly.</span></span> <span data-ttu-id="41a14-114">Это может привести к автоматическому вызову [**иобжектконтекст:: сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) или [**Иобжектконтекст:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), в зависимости от того, что делает метод внутренним.</span><span class="sxs-lookup"><span data-stu-id="41a14-114">This can result in an automatic call to [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) or [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), depending also on what the method does internally.</span></span>

<span data-ttu-id="41a14-115">**Включение автоматического завершения для метода**</span><span class="sxs-lookup"><span data-stu-id="41a14-115">**To enable auto-done for a method**</span></span>

1.  <span data-ttu-id="41a14-116">В области сведений средства администрирования "службы компонентов" щелкните правой кнопкой мыши метод, который необходимо настроить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="41a14-116">In the details pane of the Component Services administrative tool, right-click the method that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="41a14-117">В диалоговом окне Свойства метода перейдите на вкладку **Общие** .</span><span class="sxs-lookup"><span data-stu-id="41a14-117">In the method properties dialog box, click the **General** tab.</span></span>

3.  <span data-ttu-id="41a14-118">Чтобы включить автозавершение, установите флажок **автоматически Деактивировать этот объект при возврате из этого метода** .</span><span class="sxs-lookup"><span data-stu-id="41a14-118">To enable auto-done, select the **Automatically deactivate this object when this method returns** check box.</span></span> <span data-ttu-id="41a14-119">Если флажок недоступен, необходимо сначала включить JIT-активацию для компонента.</span><span class="sxs-lookup"><span data-stu-id="41a14-119">If the check box is unavailable, you must first enable JIT Activation for the component.</span></span> <span data-ttu-id="41a14-120">(Подробные инструкции см.[в разделе Включение JIT-активации для компонента](enabling-jit-activation-for-a-component.md) .)</span><span class="sxs-lookup"><span data-stu-id="41a14-120">(See[Enabling JIT Activation for a Component](enabling-jit-activation-for-a-component.md) for detailed instructions.)</span></span>

4.  <span data-ttu-id="41a14-121">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="41a14-121">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41a14-122">См. также</span><span class="sxs-lookup"><span data-stu-id="41a14-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41a14-123">Основные понятия JIT-активации COM+</span><span class="sxs-lookup"><span data-stu-id="41a14-123">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="41a14-124">Включение JIT-активации для компонента</span><span class="sxs-lookup"><span data-stu-id="41a14-124">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="41a14-125">Установка бита done</span><span class="sxs-lookup"><span data-stu-id="41a14-125">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



