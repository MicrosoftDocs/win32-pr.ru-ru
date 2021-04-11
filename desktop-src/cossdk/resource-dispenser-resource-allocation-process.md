---
description: Процесс выделения ресурсов распределителя ресурсов
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Процесс выделения ресурсов распределителя ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262619"
---
# <a name="resource-dispenser-resource-allocation-process"></a><span data-ttu-id="598d1-103">Процесс выделения ресурсов распределителя ресурсов</span><span class="sxs-lookup"><span data-stu-id="598d1-103">Resource Dispenser Resource Allocation Process</span></span>

<span data-ttu-id="598d1-104">Каждый раз, когда распределитель ресурсов выделяет ресурс из своего держателя, происходит следующее.</span><span class="sxs-lookup"><span data-stu-id="598d1-104">Each time a resource dispenser allocates a resource from its holder, the following occurs:</span></span>

1.  <span data-ttu-id="598d1-105">Распределитель ресурсов объявляет идентификатор типа ресурса (**рестипид**), описывающий требуемый тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="598d1-105">The resource dispenser declares a resource type identifier (**RESTYPID**), which describes the type of resource required.</span></span>

2.  <span data-ttu-id="598d1-106">Распределитель ресурсов вызывает метод [**ихолдер:: аллокресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) владельца, передав этот **рестипид**.</span><span class="sxs-lookup"><span data-stu-id="598d1-106">The resource dispenser calls the holder's [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method, passing this **RESTYPID**.</span></span>

3.  <span data-ttu-id="598d1-107">Держатель создает список кандидатов на основе доступных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="598d1-107">The holder generates a candidate list from the available resources.</span></span> <span data-ttu-id="598d1-108">Кандидаты — это ресурсы, которые не прикрепляются к транзакции или уже прикрепляются к транзакции вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="598d1-108">Candidates are resources that are either not enlisted in a transaction or already enlisted in the calling object's transaction.</span></span>

4.  <span data-ttu-id="598d1-109">Эти кандидаты по отдельности передаются методу [**идиспенсердривер:: ратересаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) , где они оцениваются (по шкале от 0 до 100), насколько хорошо ресурс-кандидат соответствует требуемому **рестипид**.</span><span class="sxs-lookup"><span data-stu-id="598d1-109">These candidates are individually passed to the [**IDispenserDriver::RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) method where they are rated (on a scale of 0 to 100) by how well the candidate resource matches the desired **RESTYPID**.</span></span>

5.  <span data-ttu-id="598d1-110">Держатель выбирает ресурс, который распределитель ресурсов оценивает как максимальный.</span><span class="sxs-lookup"><span data-stu-id="598d1-110">The holder chooses the resource that the resource dispenser rates as highest.</span></span>

6.  <span data-ttu-id="598d1-111">Распределитель ресурсов может завершить цикл оценки раньше, назначив ему рейтинг ресурсов 100 (идеально подходит).</span><span class="sxs-lookup"><span data-stu-id="598d1-111">The resource dispenser can terminate the rating loop early by assigning the candidate a resource rating of 100 (a perfect fit).</span></span> <span data-ttu-id="598d1-112">Оценка 100 обычно будет зарезервирована для ресурсов-кандидатов, которые уже должны быть прикреплены, если распределитель ресурсов не завершает это недорогое действие.</span><span class="sxs-lookup"><span data-stu-id="598d1-112">A rating of 100 would normally be reserved for candidate resources that are already properly enlisted, unless the resource dispenser concludes that enlistment is an inexpensive operation.</span></span> <span data-ttu-id="598d1-113">Если все потенциальные ресурсы (если таковые имеются) имеют оценку 0 (непригодный для использования), то новый ресурс создается путем вызова [**идиспенсердривер:: креатересаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span><span class="sxs-lookup"><span data-stu-id="598d1-113">If all candidate resources (if any) are rated 0 (unusable), a new resource is created by calling [**IDispenserDriver::CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span></span>

7.  <span data-ttu-id="598d1-114">Если выбранный ранее ресурс еще не прикреплен к транзакции вызывающего объекта, вызывается метод распределителя ресурсов [**идиспенсердривер:: енлистресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) .</span><span class="sxs-lookup"><span data-stu-id="598d1-114">If the resource chosen previously is not already enlisted in the calling object's transaction, the resource dispenser's [**IDispenserDriver::EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) method is called.</span></span>

8.  <span data-ttu-id="598d1-115">Вызов метода [**аллокресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) возвращается в распределитель ресурсов с прикрепленным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="598d1-115">The [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method call returns to the resource dispenser with the enlisted resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="598d1-116">См. также</span><span class="sxs-lookup"><span data-stu-id="598d1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="598d1-117">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="598d1-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="598d1-118">Прикрепление ресурса в транзакции</span><span class="sxs-lookup"><span data-stu-id="598d1-118">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[<span data-ttu-id="598d1-119">Отслеживание нераспределенных ресурсов</span><span class="sxs-lookup"><span data-stu-id="598d1-119">Tracking Non-Allocated Resources</span></span>](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



