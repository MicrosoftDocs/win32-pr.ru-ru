---
description: Принудительная активация в контексте вызывающих объектов
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Принудительная активация в контексте вызывающих объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682338"
---
# <a name="enforcing-activation-in-the-callers-context"></a><span data-ttu-id="a550b-103">Принудительная активация в контексте вызывающего объекта</span><span class="sxs-lookup"><span data-stu-id="a550b-103">Enforcing Activation in the Caller's Context</span></span>

<span data-ttu-id="a550b-104">Можно указать, активируется ли объект в собственном контексте.</span><span class="sxs-lookup"><span data-stu-id="a550b-104">You can control whether an object gets activated in its own context.</span></span> <span data-ttu-id="a550b-105">При использовании средства администрирования "службы компонентов" для обязательной активации компонентов в контексте вызывающего объекта происходит следующее, когда COM+ активирует экземпляр компонента в контексте:</span><span class="sxs-lookup"><span data-stu-id="a550b-105">When you use the Component Services administrative tool to require component activation in the caller's context, the following occurs when COM+ activates an instance of the component in a context:</span></span>

-   <span data-ttu-id="a550b-106">Если это возможно, объект активируется в контексте создателя.</span><span class="sxs-lookup"><span data-stu-id="a550b-106">The object is activated in the creator's context if possible.</span></span>
-   <span data-ttu-id="a550b-107">Активация объекта завершается ошибкой, если требуется его собственный контекст; \_ \_ \_ Возвращается некоторая попытка \_ создания \_ внешнего \_ \_ контекста клиента.</span><span class="sxs-lookup"><span data-stu-id="a550b-107">Object activation fails if it requires its own context; CO\_E\_ATTEMPT\_TO\_CREATE\_OUTSIDE\_CLIENT\_CONTEXT is returned.</span></span>

<span data-ttu-id="a550b-108">Требуется ли объекту собственный контекст зависит от его конфигурации относительно текущего состояния свойств контекста вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="a550b-108">Whether or not the object requires its own context depends on its configuration relative to the current state of the caller's context properties.</span></span> <span data-ttu-id="a550b-109">Дополнительные сведения см. в разделе [контексты com+](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="a550b-109">For more detail, see [COM+ Contexts](com--contexts.md).</span></span>

<span data-ttu-id="a550b-110">Вы бы хотели контролировать активацию на этом уровне, если какой-либо аспект объекта не будет функционировать должным образом, если он имеет собственный контекст.</span><span class="sxs-lookup"><span data-stu-id="a550b-110">You would want to control activation at that fine a level if some aspect of your object would not function properly if it has its own context.</span></span> <span data-ttu-id="a550b-111">Например, если компонент не поддерживает упаковку и имеет собственный контекст, все вызовы этого метода завершатся ошибкой из-за перехвата вызовов между контекстами и выполнения упрощенного маршалинга.</span><span class="sxs-lookup"><span data-stu-id="a550b-111">For example, if the component does not support marshaling and it has its own context, any calls to it will fail because cross-context calls are intercepted and a lightweight marshal performed.</span></span>

<span data-ttu-id="a550b-112">**Принудительное применение активации в контексте вызывающего объекта**</span><span class="sxs-lookup"><span data-stu-id="a550b-112">**To enforce activation in the caller's context**</span></span>

1.  <span data-ttu-id="a550b-113">В области сведений средства администрирования "службы компонентов" щелкните правой кнопкой мыши компонент (расположенный в папке **Components** любого выбранного приложения COM+), для которого вы настраиваете свойства активации, и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="a550b-113">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) for which you are setting activation properties and then click **Properties**.</span></span>

2.  <span data-ttu-id="a550b-114">В диалоговом окне Свойства компонента перейдите на вкладку **Активация** .</span><span class="sxs-lookup"><span data-stu-id="a550b-114">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="a550b-115">Установите флажок **должен быть активирован в контексте вызывающих объектов** .</span><span class="sxs-lookup"><span data-stu-id="a550b-115">Select the **Must be activated in the callers context** check box.</span></span>

4.  <span data-ttu-id="a550b-116">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a550b-116">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a550b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a550b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a550b-118">Основные понятия JIT-активации COM+</span><span class="sxs-lookup"><span data-stu-id="a550b-118">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="a550b-119">Принудительная активация в контексте по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a550b-119">Enforcing Activation in the Default Context</span></span>](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



