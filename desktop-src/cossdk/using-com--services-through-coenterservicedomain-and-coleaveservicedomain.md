---
description: Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141977"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a><span data-ttu-id="b2443-103">Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин</span><span class="sxs-lookup"><span data-stu-id="b2443-103">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>

<span data-ttu-id="b2443-104">[**Коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) и [**колеавесервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) используются вместе для заключения в область кода, которая выполняется в собственном контексте и может использовать службы COM+ без необходимости в компонентах COM+.</span><span class="sxs-lookup"><span data-stu-id="b2443-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) are used together to surround an area of code that runs in its own context and can use COM+ services without the need for COM+ components.</span></span> <span data-ttu-id="b2443-105">Службы COM+, используемые в этом контексте, настраиваются с помощью объекта [**ксервицеконфиг**](cserviceconfig.md) , который передается в **коентерсервицедомаин**.</span><span class="sxs-lookup"><span data-stu-id="b2443-105">The COM+ services that are used in this context are configured through the [**CServiceConfig**](cserviceconfig.md) object that is passed in to **CoEnterServiceDomain**.</span></span> <span data-ttu-id="b2443-106">Код, окруженный **коентерсервицедомаин** и **колеавесервицедомаин** , ведет себя так, как будто это метод, который вызывается для объекта, созданного в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="b2443-106">The code that is surrounded by **CoEnterServiceDomain** and **CoLeaveServiceDomain** behaves as though it were a method that is called on an object created within this context.</span></span>

<span data-ttu-id="b2443-107">Приложение для работы со скриптами может использовать эту пару функций для обеспечения поддержки времени выполнения служб COM+ без компонентов.</span><span class="sxs-lookup"><span data-stu-id="b2443-107">A scripting application can use this pair of functions to provide run-time support of COM+ services without components.</span></span> <span data-ttu-id="b2443-108">Например, приложение для создания сценариев может быть разработано для предоставления тегов, позволяющих создателям сценариев вводить и оставлять в скрипте домен службы.</span><span class="sxs-lookup"><span data-stu-id="b2443-108">For example, a scripting application can be developed to provide tags that allow the script writers to enter and leave a service domain within the script.</span></span> <span data-ttu-id="b2443-109">Когда обработчик скриптов обрабатывает скрипт и обнаруживает теги, он может вызвать [**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) с предварительно настроенным объектом [**ксервицеконфиг**](cserviceconfig.md) , запустить необходимый код и затем вызвать [**колеавесервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="b2443-109">When the scripting engine processes the script and encounters the tags, it can call [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) with a preconfigured [**CServiceConfig**](cserviceconfig.md) object, run the necessary code, and then call [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="b2443-110">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="b2443-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="b2443-111">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="b2443-111">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="b2443-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b2443-112">Visual Basic</span></span>

<span data-ttu-id="b2443-113">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="b2443-113">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="b2443-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="b2443-114">C/C++</span></span>

<span data-ttu-id="b2443-115">В следующем фрагменте кода показано, как использовать службы COM+ между вызовами [**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) и [**колеавесервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="b2443-115">The following code fragment illustrates how to use COM+ services between calls to [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span> <span data-ttu-id="b2443-116">Обработка ошибок опущена для краткости.</span><span class="sxs-lookup"><span data-stu-id="b2443-116">Error handling is omitted for brevity.</span></span> <span data-ttu-id="b2443-117">Этот фрагмент кода использует объект [**ксервицеконфиг**](cserviceconfig.md) , который был создан и настроен в [настройке служб COM+ с помощью ксервицеконфиг](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="b2443-117">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a><span data-ttu-id="b2443-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b2443-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2443-119">**коентерсервицедомаин**</span><span class="sxs-lookup"><span data-stu-id="b2443-119">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="b2443-120">**колеавесервицедомаин**</span><span class="sxs-lookup"><span data-stu-id="b2443-120">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="b2443-121">Настройка служб COM+ с помощью Ксервицеконфиг</span><span class="sxs-lookup"><span data-stu-id="b2443-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="b2443-122">**ксервицеконфиг**</span><span class="sxs-lookup"><span data-stu-id="b2443-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="b2443-123">Использование служб COM+ через Кокреатеактивити</span><span class="sxs-lookup"><span data-stu-id="b2443-123">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



