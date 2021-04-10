---
description: Реализация распределителя ресурсов COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Реализация распределителя ресурсов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142601"
---
# <a name="implementing-a-com-resource-dispenser"></a><span data-ttu-id="c2d0f-103">Реализация распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="c2d0f-103">Implementing a COM+ Resource Dispenser</span></span>

<span data-ttu-id="c2d0f-104">Следующие шаги описывают общую процедуру реализации распределителя ресурсов COM+:</span><span class="sxs-lookup"><span data-stu-id="c2d0f-104">The following steps outline a general procedure for implementing a COM+ resource dispenser:</span></span>

1.  <span data-ttu-id="c2d0f-105">Определите формат **рестипид** , который определяет, как ресурсы отличаются друг от друга.</span><span class="sxs-lookup"><span data-stu-id="c2d0f-105">Decide on **RESTYPID** format that categorizes how your resources differ from each other.</span></span>

2.  <span data-ttu-id="c2d0f-106">Используйте файл заголовка Мтксдм. h и библиотеку Мтксдм. lib соответственно.</span><span class="sxs-lookup"><span data-stu-id="c2d0f-106">Use the Mtxdm.h and Mtxdm.lib header file and library, respectively.</span></span>

3.  <span data-ttu-id="c2d0f-107">Создайте библиотеку DLL, которая реализует интерфейс [**идиспенсердривер**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) и API, которые требуется предоставить приложениям.</span><span class="sxs-lookup"><span data-stu-id="c2d0f-107">Build a DLL that implements the [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) interface and the API you want to expose to applications.</span></span>

4.  <span data-ttu-id="c2d0f-108">Во время запуска ([*DllMain*](/windows/desktop/Dlls/dllmain) или первый вызов API-интерфейса распределителя) вызовите функцию [**жетдиспенсерманажер**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) .</span><span class="sxs-lookup"><span data-stu-id="c2d0f-108">In the startup ([*DllMain*](/windows/desktop/Dlls/dllmain) or first call to the dispenser API), call the [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) function.</span></span> <span data-ttu-id="c2d0f-109">Он возвращает указатель на интерфейс [**идиспенсерманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) диспетчера распределителя.</span><span class="sxs-lookup"><span data-stu-id="c2d0f-109">This returns a pointer to the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>

5.  <span data-ttu-id="c2d0f-110">Вызовите метод [**идиспенсерманажер:: регистердиспенсер**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), передав ему указатель на реализацию [**идиспенсердривер**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span><span class="sxs-lookup"><span data-stu-id="c2d0f-110">Call [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passing a pointer to your implementation of [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span></span> <span data-ttu-id="c2d0f-111">В результате диспетчер распределителя создает держатель (диспетчер пула) для распределителя ресурсов, а затем возвращает указатель на интерфейс [**ихолдер**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .</span><span class="sxs-lookup"><span data-stu-id="c2d0f-111">This causes the dispenser manager to create a holder (pooling manager) for your resource dispenser and then return the pointer to your [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) interface.</span></span>

6.  <span data-ttu-id="c2d0f-112">Сохраните этот указатель, чтобы можно было вызывать [**ихолдер:: аллокресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) и [**Ихолдер:: фриресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span><span class="sxs-lookup"><span data-stu-id="c2d0f-112">Store this pointer so that you can call [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span>

7.  <span data-ttu-id="c2d0f-113">Теперь можно (в ответ на вызовы API) выполнять вызовы [**аллокресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) и [**фриресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span><span class="sxs-lookup"><span data-stu-id="c2d0f-113">You can now (in response to calls to your API) make calls to [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span> <span data-ttu-id="c2d0f-114">**Аллокресаурце** изначально реагирует на обратный вызов метода [**креатересаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , но последующие вызовы **аллокресаурце** обслуживаются из растущего пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2d0f-114">**AllocResource** initially responds by calling back to your [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) method, but later **AllocResource** calls are serviced from the growing pool of resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2d0f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c2d0f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2d0f-116">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="c2d0f-116">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="c2d0f-117">Интерфейсы распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="c2d0f-117">COM+ Resource Dispenser Interfaces</span></span>](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
