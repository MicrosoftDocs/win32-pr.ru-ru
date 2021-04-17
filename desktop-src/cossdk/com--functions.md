---
description: Ниже перечислены функции COM+.
ms.assetid: fdeb70ff-17ae-4ee4-a8b1-7fffb65ba2b2
title: Функции COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f7ce33e729a12c37ff1f2dcef516ab13d9b69a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105713342"
---
# <a name="com-functions"></a><span data-ttu-id="dc99b-103">Функции COM+</span><span class="sxs-lookup"><span data-stu-id="dc99b-103">COM+ Functions</span></span>

<span data-ttu-id="dc99b-104">Ниже перечислены функции COM+.</span><span class="sxs-lookup"><span data-stu-id="dc99b-104">The following are the COM+ functions.</span></span>



| <span data-ttu-id="dc99b-105">Функция</span><span class="sxs-lookup"><span data-stu-id="dc99b-105">Function</span></span>                                                                 | <span data-ttu-id="dc99b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="dc99b-106">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc99b-107">**кокреатеактивити**</span><span class="sxs-lookup"><span data-stu-id="dc99b-107">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)                             | <span data-ttu-id="dc99b-108">Создает действие синхронной или асинхронной пакетной работы, которое может использовать службы COM+ без необходимости создания компонента COM+.</span><span class="sxs-lookup"><span data-stu-id="dc99b-108">Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.</span></span> |
| [<span data-ttu-id="dc99b-109">**коентерсервицедомаин**</span><span class="sxs-lookup"><span data-stu-id="dc99b-109">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     | <span data-ttu-id="dc99b-110">Используется для ввода кода, который затем может использовать службы COM+.</span><span class="sxs-lookup"><span data-stu-id="dc99b-110">Used to enter code that can then use COM+ services.</span></span>                                                                                     |
| [<span data-ttu-id="dc99b-111">**кожетдефаултконтекст**</span><span class="sxs-lookup"><span data-stu-id="dc99b-111">**CoGetDefaultContext**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetdefaultcontext)                       | <span data-ttu-id="dc99b-112">Извлекает ссылку на контекст по умолчанию указанного апартамента.</span><span class="sxs-lookup"><span data-stu-id="dc99b-112">Retrieves a reference to the default context of the specified apartment.</span></span>                                                                |
| [<span data-ttu-id="dc99b-113">**колеавесервицедомаин**</span><span class="sxs-lookup"><span data-stu-id="dc99b-113">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)                     | <span data-ttu-id="dc99b-114">Используется для выхода из кода, использующего службы COM+.</span><span class="sxs-lookup"><span data-stu-id="dc99b-114">Used to leave code that uses COM+ services.</span></span>                                                                                             |
| <span data-ttu-id="dc99b-115">**комплускомплетекббсетуп**</span><span class="sxs-lookup"><span data-stu-id="dc99b-115">**ComPlusCompleteCbbSetup**</span></span>               | <span data-ttu-id="dc99b-116">Завершает миграцию каталога на конечном компьютере.</span><span class="sxs-lookup"><span data-stu-id="dc99b-116">Completes a catalog migration on the destination computer.</span></span>                                                                              |
| <span data-ttu-id="dc99b-117">**жеткомплуспаккажеинсталлстатус**</span><span class="sxs-lookup"><span data-stu-id="dc99b-117">**GetComPlusPackageInstallStatus**</span></span> | <span data-ttu-id="dc99b-118">Указывает, установлена ли 64-разрядная среда CLR.</span><span class="sxs-lookup"><span data-stu-id="dc99b-118">Indicates whether the 64-bit Common Language Runtime (CLR) is installed.</span></span>                                                                |
| [<span data-ttu-id="dc99b-119">**жетдиспенсерманажер**</span><span class="sxs-lookup"><span data-stu-id="dc99b-119">**GetDispenserManager**</span></span>](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager)                       | <span data-ttu-id="dc99b-120">Получает интерфейс [**идиспенсерманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) диспетчера распределителя.</span><span class="sxs-lookup"><span data-stu-id="dc99b-120">Retrieves the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>                                             |
| [<span data-ttu-id="dc99b-121">**жетманажедекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="dc99b-121">**GetManagedExtensions**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getmanagedextensions)                     | <span data-ttu-id="dc99b-122">Определяет, поддерживает ли установленная версия COM+ специальные функции, предоставляемые для управления обслуживаемыми компонентами (управляемые объекты).</span><span class="sxs-lookup"><span data-stu-id="dc99b-122">Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).</span></span>    |
| [<span data-ttu-id="dc99b-123">**Класс ObjectContext**</span><span class="sxs-lookup"><span data-stu-id="dc99b-123">**GetObjectContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)                             | <span data-ttu-id="dc99b-124">Извлекает ссылку на контекст, связанный с текущим объектом COM+.</span><span class="sxs-lookup"><span data-stu-id="dc99b-124">Retrieves a reference to the context that is associated with the current COM+ object.</span></span>                                                   |
| [<span data-ttu-id="dc99b-125">**мтскреатеактивити**</span><span class="sxs-lookup"><span data-stu-id="dc99b-125">**MTSCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-mtscreateactivity)                           | <span data-ttu-id="dc99b-126">Создает действие в однопотоковом подразделении для выполнения синхронной или асинхронной пакетной работы.</span><span class="sxs-lookup"><span data-stu-id="dc99b-126">Creates an activity in a single-threaded apartment to do synchronous or asynchronous batch work.</span></span>                                        |
| [<span data-ttu-id="dc99b-127">**рециклесуррогате**</span><span class="sxs-lookup"><span data-stu-id="dc99b-127">**RecycleSurrogate**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)                             | <span data-ttu-id="dc99b-128">Перезапускает вызывающий процесс.</span><span class="sxs-lookup"><span data-stu-id="dc99b-128">Recycles the calling process.</span></span>                                                                                                           |
| [<span data-ttu-id="dc99b-129">**сафереф**</span><span class="sxs-lookup"><span data-stu-id="dc99b-129">**SafeRef**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)                                               | <span data-ttu-id="dc99b-130">Устаревшие не используйте.</span><span class="sxs-lookup"><span data-stu-id="dc99b-130">Obsolete; do not use.</span></span>                                                                                                                   |



 

 

 



