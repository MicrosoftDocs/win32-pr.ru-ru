---
description: Интерфейсы распределителя ресурсов COM+
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: Интерфейсы распределителя ресурсов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a6ea5c5c09f67f86b42ebf5b881f1d19ad1501
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895625"
---
# <a name="com-resource-dispenser-interfaces"></a><span data-ttu-id="4b120-103">Интерфейсы распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="4b120-103">COM+ Resource Dispenser Interfaces</span></span>

<span data-ttu-id="4b120-104">Компоненты приложения используют распределитель ресурсов для доступа к общей информации.</span><span class="sxs-lookup"><span data-stu-id="4b120-104">Application components use resource dispensers to access shared information.</span></span> <span data-ttu-id="4b120-105">Интерфейсы, описанные в следующей таблице, содержат подробные справочные сведения для разработчиков распределительных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b120-105">The interfaces described in the following table provide detailed reference information for developers of resource dispensers.</span></span>



| <span data-ttu-id="4b120-106">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="4b120-106">Interfaces</span></span>                                                | <span data-ttu-id="4b120-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4b120-107">Description</span></span>                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b120-108">**идиспенсердривер**</span><span class="sxs-lookup"><span data-stu-id="4b120-108">**IDispenserDriver**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | <span data-ttu-id="4b120-109">Этот интерфейс вызывается держательом распределителя ресурсов для создания, прикрепления, вычисления и уничтожения ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b120-109">This interface is called by the resource dispenser holder to create, enlist, evaluate, and destroy a resource.</span></span><br/> |
| [<span data-ttu-id="4b120-110">**идиспенсерманажер**</span><span class="sxs-lookup"><span data-stu-id="4b120-110">**IDispenserManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | <span data-ttu-id="4b120-111">Распределитель ресурсов использует этот интерфейс для подключения к диспетчеру распределителя.</span><span class="sxs-lookup"><span data-stu-id="4b120-111">Resource dispensers use this interface to connect to the dispenser manager.</span></span><br/>                                    |
| [<span data-ttu-id="4b120-112">**ихолдер**</span><span class="sxs-lookup"><span data-stu-id="4b120-112">**IHolder**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | <span data-ttu-id="4b120-113">Этот интерфейс используется для подготовки и обработки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b120-113">This interface is used to prepare and handle resources.</span></span><br/>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="4b120-114">См. также</span><span class="sxs-lookup"><span data-stu-id="4b120-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b120-115">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="4b120-115">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="4b120-116">Типы, используемые в интерфейсах распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="4b120-116">Types Used in COM+ Resource Dispenser Interfaces</span></span>](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




