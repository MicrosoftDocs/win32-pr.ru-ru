---
description: Типы, используемые в интерфейсах распределителя ресурсов COM+
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: Типы, используемые в интерфейсах распределителя ресурсов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c4d0f62ec7c61a9bc0f189c1ee02d1868a3242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807631"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a><span data-ttu-id="97835-103">Типы, используемые в интерфейсах распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="97835-103">Types Used in COM+ Resource Dispenser Interfaces</span></span>

<span data-ttu-id="97835-104">В интерфейсах распределителя ресурсов используются следующие типы.</span><span class="sxs-lookup"><span data-stu-id="97835-104">The following types are used in the resource dispenser interfaces.</span></span>



| <span data-ttu-id="97835-105">Тип</span><span class="sxs-lookup"><span data-stu-id="97835-105">Type</span></span>           | <span data-ttu-id="97835-106">Описание</span><span class="sxs-lookup"><span data-stu-id="97835-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97835-107">**рестипид**</span><span class="sxs-lookup"><span data-stu-id="97835-107">**RESTYPID**</span></span>   | <span data-ttu-id="97835-108">**DWORD** , определяющий тип ресурса, а не конкретный ресурс.</span><span class="sxs-lookup"><span data-stu-id="97835-108">A **DWORD** that identifies a type of resource, not a particular resource.</span></span> <span data-ttu-id="97835-109">**Рестипид** обычно является указателем на структуру в памяти распределительной панели, описывающей тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="97835-109">A **RESTYPID** is usually a pointer to a structure in the dispenser's memory that describes the resource type.</span></span> <span data-ttu-id="97835-110">Диспетчер распределителя не понимает (и не нуждается в понимании) этой структуры в памяти распределителя ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97835-110">The dispenser manager does not understand (and does not need to understand) this structure within the resource dispenser's memory.</span></span> <span data-ttu-id="97835-111">Диспетчер распределителя использует **рестипид** только для ссылки на тип ресурса в распределителе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97835-111">The dispenser manager uses **RESTYPID** only to refer to a resource type within a resource dispenser.</span></span>                                                                                                                                   |
| <span data-ttu-id="97835-112">**RESID**</span><span class="sxs-lookup"><span data-stu-id="97835-112">**RESID**</span></span>      | <span data-ttu-id="97835-113">**DWORD** , определяющий конкретный ресурс, в отличие от типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="97835-113">A **DWORD** that identifies a particular resource, as opposed to a type of resource.</span></span> <span data-ttu-id="97835-114">**RESID** обычно представляет собой (**void \* *_), указывающий на структуру в памяти распределителя ресурсов, которая представляет ресурс. Диспетчеру распределителя не нужно понимать эту структуру в памяти распределителя ресурсов. Диспетчер распределителя использует _* RESID** для ссылки на конкретный ресурс в распределителе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97835-114">A **RESID** is usually a (**void \**_) that points to a structure in the resource dispenser's memory that represents the resource. The dispenser manager does not need to understand this structure within the resource dispenser's memory. The dispenser manager uses _\* RESID*\* to refer to a particular resource within a resource dispenser.</span></span>                                                                                                                                 |
| <span data-ttu-id="97835-115">**сресид**</span><span class="sxs-lookup"><span data-stu-id="97835-115">**SRESID**</span></span>     | <span data-ttu-id="97835-116">Строковая версия **RESID** в Юникоде, используемая в методах [**Ихолдер:: траккресаурцес**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) и [**ихолдер:: унтраккресаурцес**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) .</span><span class="sxs-lookup"><span data-stu-id="97835-116">A Unicode string version of **RESID**, used in the [**IHolder::TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) and [**IHolder::UntrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) methods.</span></span> <span data-ttu-id="97835-117">Строки иногда полезны, когда необходимо записать только небольшой объем информации о ресурсе, и полное описание ресурса может содержаться в **сресид**.</span><span class="sxs-lookup"><span data-stu-id="97835-117">Strings are sometimes useful when only a small amount of information needs to be recorded about a resource and the entire description of the resource can be contained in the **SRESID**.</span></span> <span data-ttu-id="97835-118">В частности, использование **сресид** может избавиться от необходимости сопоставления в распределителе ресурсов, когда ресурс представляет связь между двумя (или более) объектами.</span><span class="sxs-lookup"><span data-stu-id="97835-118">In particular, using the **SRESID** can sometimes eliminate the need for a map in the resource dispenser when the resource represents a relationship between two (or more) things.</span></span> |
| <span data-ttu-id="97835-119">**трансид**</span><span class="sxs-lookup"><span data-stu-id="97835-119">**TRANSID**</span></span>    | <span data-ttu-id="97835-120">Определяет транзакцию.</span><span class="sxs-lookup"><span data-stu-id="97835-120">Identifies a transaction.</span></span> <span data-ttu-id="97835-121">Этот тип может быть приведен к интерфейсу **ITransaction** .</span><span class="sxs-lookup"><span data-stu-id="97835-121">This type may be cast to the **ITransaction** interface.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="97835-122">**тимеинсекс**</span><span class="sxs-lookup"><span data-stu-id="97835-122">**TIMEINSECS**</span></span> | <span data-ttu-id="97835-123">Указывает, как долго ресурс может быть неактивным до его уничтожения.</span><span class="sxs-lookup"><span data-stu-id="97835-123">Indicates how long a resource can be inactive before it is destroyed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="97835-124">См. также</span><span class="sxs-lookup"><span data-stu-id="97835-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97835-125">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="97835-125">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="97835-126">Интерфейсы распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="97835-126">COM+ Resource Dispenser Interfaces</span></span>](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



