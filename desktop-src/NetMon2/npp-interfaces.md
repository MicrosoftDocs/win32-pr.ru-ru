---
description: Поставщики сетевых пакетов (НППС) предоставляют COM-интерфейсы, которые вызываются приложениями НПП, и сетевой монитор.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Интерфейсы НПП
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662577"
---
# <a name="npp-interfaces"></a><span data-ttu-id="1c9bc-103">Интерфейсы НПП</span><span class="sxs-lookup"><span data-stu-id="1c9bc-103">NPP Interfaces</span></span>

<span data-ttu-id="1c9bc-104">Поставщики сетевых пакетов (НППС) предоставляют COM-интерфейсы, которые вызываются приложениями НПП, и сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-104">Network packet providers (NPPs) provide COM interfaces that are called by NPP applications, and Network Monitor.</span></span> <span data-ttu-id="1c9bc-105">При вызове [креатенппинтерфаце](createnppinterface.md)Помните, что каждый НПП представлен как единый внутрипроцессный COM-объект.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-105">When you call [CreateNPPInterface](createnppinterface.md), remember that each NPP is represented as a single in-process COM object.</span></span> <span data-ttu-id="1c9bc-106">Приложения могут создавать экземпляры любого числа объектов НПП.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-106">Applications can instantiate any number of NPP objects.</span></span> <span data-ttu-id="1c9bc-107">Однако каждый экземпляр объекта должен использовать один (и только один) из пяти интерфейсов НПП.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-107">However, each instantiated object must use one—and only one—of the five NPP interfaces.</span></span>

<span data-ttu-id="1c9bc-108">Обратите внимание, что различные интерфейсы НПП предоставляют сетевые данные в различных формах.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-108">Note also that different NPP interfaces provide network data in various forms.</span></span> <span data-ttu-id="1c9bc-109">Например, сетевой монитор использует интерфейс **иделайдк** для записи сетевого трафика и его сохранения в файл записи; в то время как мониторы используют интерфейс **ИРТК** для записи сетевого трафика в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-109">For example, Network Monitor uses the **IDelaydC** interface to capture network traffic and save it to a capture file; while monitors use the **IRTC** interface to capture real time network traffic.</span></span> <span data-ttu-id="1c9bc-110">В следующей таблице описаны сетевой монитор интерфейсов НПП.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-110">The following table describes Network Monitor NPP interfaces.</span></span>



| <span data-ttu-id="1c9bc-111">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="1c9bc-111">Interface</span></span>                | <span data-ttu-id="1c9bc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1c9bc-112">Description</span></span>                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c9bc-113">иделайдк</span><span class="sxs-lookup"><span data-stu-id="1c9bc-113">IDelaydC</span></span>](idelaydc.md) | <span data-ttu-id="1c9bc-114">Захватывает сетевой трафик, хранящийся в файле записи.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-114">Captures network traffic that is stored in a capture file.</span></span> <span data-ttu-id="1c9bc-115">Этот интерфейс используется приложениями сетевой монитор и НПП.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-115">This interface is used by Network Monitor and NPP applications.</span></span>                                          |
| [<span data-ttu-id="1c9bc-116">иесп</span><span class="sxs-lookup"><span data-stu-id="1c9bc-116">IESP</span></span>](iesp.md)         | <span data-ttu-id="1c9bc-117">Захватывает сетевой трафик, хранящийся в файле записи, и обеспечивает расширенную статистику в особом формате файла ESP.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-117">Captures network traffic that is stored in a capture file and provides enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="1c9bc-118">Этот интерфейс используется приложениями НПП</span><span class="sxs-lookup"><span data-stu-id="1c9bc-118">This interface is used by NPP applications</span></span> |
| [<span data-ttu-id="1c9bc-119">иртк</span><span class="sxs-lookup"><span data-stu-id="1c9bc-119">IRTC</span></span>](irtc.md)         | <span data-ttu-id="1c9bc-120">Захватывает сетевой трафик в реальном времени и активирует события при их возникновении.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-120">Captures real time network traffic and triggers events when they occur.</span></span> <span data-ttu-id="1c9bc-121">Этот интерфейс используется [*мониторами*](m.md) и НПП приложениями.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-121">This interface is used by [*monitors*](m.md) and NPP applications.</span></span>     |
| [<span data-ttu-id="1c9bc-122">истатс</span><span class="sxs-lookup"><span data-stu-id="1c9bc-122">IStats</span></span>](istats.md)     | <span data-ttu-id="1c9bc-123">Получает статистику в виде необработанных данных, а не кадров.</span><span class="sxs-lookup"><span data-stu-id="1c9bc-123">Retrieves statistics as raw data rather than frames.</span></span> <span data-ttu-id="1c9bc-124">Этот интерфейс используется приложениями НПП, такими как [*perfmon*](p.md).</span><span class="sxs-lookup"><span data-stu-id="1c9bc-124">This interface is used by NPP applications such as [*Perfmon*](p.md).</span></span>                     |



 

 

 



