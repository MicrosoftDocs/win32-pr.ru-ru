---
title: Видимые кучи дескрипторов шейдеров
description: Видимые кучи дескрипторов шейдеров — это кучи дескрипторов, на которые могут ссылаться шейдеры через таблицы дескрипторов.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105103"
---
# <a name="shader-visible-descriptor-heaps"></a><span data-ttu-id="276da-103">Видимые кучи дескрипторов шейдеров</span><span class="sxs-lookup"><span data-stu-id="276da-103">Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="276da-104">Видимые кучи дескрипторов шейдеров — это кучи дескрипторов, на которые могут ссылаться шейдеры через таблицы дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="276da-104">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span>

-   [<span data-ttu-id="276da-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="276da-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="276da-106">Пример</span><span class="sxs-lookup"><span data-stu-id="276da-106">An example</span></span>](#an-example)
-   [<span data-ttu-id="276da-107">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="276da-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="276da-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="276da-108">Overview</span></span>

<span data-ttu-id="276da-109">В кучах дескрипторов, на которые могут ссылаться шейдеры через таблицы дескрипторов, входят несколько разновидностей: один тип кучи, D3D12 \_ SRV \_ UAV CBV- \_ \_ куча дескрипторов \_ , может содержать представления ресурсов шейдера, неупорядоченные представления доступа и представления постоянного буфера, все смешанные.</span><span class="sxs-lookup"><span data-stu-id="276da-109">Descriptor heaps that can be referenced by shaders through descriptor tables come in a couple of flavors: One heap type, D3D12\_SRV\_UAV\_CBV\_DESCRIPTOR\_HEAP, can hold Shader Resource Views, Unordered Access Views, and Constant Buffer Views, all intermixed.</span></span> <span data-ttu-id="276da-110">Любое заданное расположение в куче может быть одним из перечисленных типов дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="276da-110">Any given location in the heap can be any one of the listed types of descriptors.</span></span> <span data-ttu-id="276da-111">Другой тип кучи, \_ \_ образец типа кучи дескрипторов D3D12 \_ \_ , хранит только образцы, отражающие факт, что для большинства оборудования Управление пробами осуществляется отдельно от СРВС, уавс, КБВС.</span><span class="sxs-lookup"><span data-stu-id="276da-111">Another heap type, D3D12\_DESCRIPTOR\_HEAP\_TYPE\_SAMPLER, only stores samplers, reflecting the fact that for the majority of hardware, samplers are managed separately from SRVs, UAVs, CBVs.</span></span>

<span data-ttu-id="276da-112">Кучи дескрипторов этих типов могут запрашиваться как видимые шейдером или нет при создании кучи (последний — невидимый). может быть полезен для промежуточного хранения дескрипторов ЦП.</span><span class="sxs-lookup"><span data-stu-id="276da-112">Descriptor heaps of these types may be requested to be shader visible or not when the heap is created (the latter – non shader visible - can be useful for staging descriptors on the CPU).</span></span> <span data-ttu-id="276da-113">Если запрос должен быть видимым шейдером, каждый из перечисленных выше типов кучи может иметь ограничение на размер оборудования для любого выделения отдельной кучи дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="276da-113">When requested to be shader visible, each of the above heap types may have a hardware size limit for any individual descriptor heap allocation.</span></span>

<span data-ttu-id="276da-114">Приложения могут создавать любое количество куч дескрипторов, а невидимые кучи дескрипторов не ограничиваются размером.</span><span class="sxs-lookup"><span data-stu-id="276da-114">Applications can create any number of descriptor heaps , and non shader visible descriptor heaps are not constrained in size.</span></span> <span data-ttu-id="276da-115">Если видимая куча дескрипторов шейдеров, созданная приложением, меньше, чем предельный размер оборудования, драйвер может выбрать подраспределение кучи дескрипторов из более крупной базовой кучи дескрипторов, чтобы в одной куче аппаратных дескрипторов поместилось несколько куч дескрипторов API.</span><span class="sxs-lookup"><span data-stu-id="276da-115">If a shader visible descriptor heap that is created by the application is smaller than the hardware size limit, the driver may choose to sub-allocate the descriptor heap out of a larger underlying descriptor heap so that multiple API descriptor heaps fit within one hardware descriptor heap.</span></span> <span data-ttu-id="276da-116">Причиной этого может быть то, что для некоторого оборудования при переключении между кучами дескрипторов оборудования во время выполнения требуется, чтобы GPU выполнял ожидание в режиме простоя (чтобы завершить работу ссылок GPU на ранее созданную кучу дескрипторов).</span><span class="sxs-lookup"><span data-stu-id="276da-116">The reason this may happen is that for some hardware, switching between hardware descriptor heaps during execution requires a GPU wait for idle (to ensure that GPU references to the previously descriptor heap are finished).</span></span> <span data-ttu-id="276da-117">Если все кучи дескрипторов, создаваемые приложением, соответствуют максимальной емкости аппаратной кучи, то такие ожидания не произойдет при переключении кучи дескрипторов API во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="276da-117">If all of the descriptor heaps that an application creates fit into the applicable hardware heap's maximum capacities, then no such waits will occur when switching API descriptor heaps during rendering.</span></span> <span data-ttu-id="276da-118">Однако приложения должны допускать возможность, что переключение текущей кучи дескрипторов может повлечь за собой ожидание простоя.</span><span class="sxs-lookup"><span data-stu-id="276da-118">Applications must allow for the possibility, however, that switching the current descriptor heap may incur a wait for idle.</span></span>

<span data-ttu-id="276da-119">Чтобы избежать появления такого возможного ожидания в случае неактивности на коммутаторе кучи дескрипторов, приложения могут воспользоваться преимуществами перерывов в отрисовке, которые приведут к неактивности GPU по другим причинам, так как время ожидания простоя происходит в любом случае.</span><span class="sxs-lookup"><span data-stu-id="276da-119">To avoid being impacted by this possible wait for idle on the descriptor heap switch, applications can take advantage of breaks in rendering that would cause the GPU to idle for other reasons as the time to do descriptor heap switches, since a wait for idle is happening anyway.</span></span>

<span data-ttu-id="276da-120">Механизм и семантика для идентификации куч дескриптора для шейдеров во время записи списка команд/пакетов описаны в справочнике по API.</span><span class="sxs-lookup"><span data-stu-id="276da-120">The mechanism and semantics for identifying descriptor heaps to shaders during command list / bundle recording are described in the API reference.</span></span>

## <a name="an-example"></a><span data-ttu-id="276da-121">Пример</span><span class="sxs-lookup"><span data-stu-id="276da-121">An example</span></span>

<span data-ttu-id="276da-122">На рисунке ниже показаны две кучи дескрипторов, ссылающиеся на две отдельные 2D-текстуры, которые хранятся в двух слотах большой кучи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="276da-122">The image below shows two descriptor heaps referencing two separate 2D textures being stored in two slots of a large default heap.</span></span> <span data-ttu-id="276da-123">Графический конвейер (включая шейдеры) может получить доступ к куче дескрипторов, которая является видимой для шейдера, и поэтому для конвейера доступна двухмерная текстура.</span><span class="sxs-lookup"><span data-stu-id="276da-123">The descriptor heap that is shader visible can be accessed by the graphics pipeline (including the shaders), and hence the 2D texture is available to the pipeline.</span></span>

![видимые и невидимые кучи дескрипторов](images/descriptor-heaps.png)

> [!Note]  
> <span data-ttu-id="276da-125">Часто существует ограничение на оборудование GPU, доступное для записи в локальную память GPU (которая называется общей памятью для записи) для куч дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="276da-125">There is often a limit on GPU hardware of the amount of GPU local memory writeable by the CPU (referred to as write-combined memory) for descriptor heaps.</span></span> <span data-ttu-id="276da-126">Обычно это ограничение обходится вокруг 96 МБ для всех процессов.</span><span class="sxs-lookup"><span data-stu-id="276da-126">Typically this limit is around 96MB for all processes.</span></span> <span data-ttu-id="276da-127">Например, в куче дескрипторов элементов 1 000 000, в которой в дескрипторах 32byte используется 32 МБ.</span><span class="sxs-lookup"><span data-stu-id="276da-127">A one million member descriptor heap, with 32byte descriptors, would use up 32MB, for example.</span></span> <span data-ttu-id="276da-128">При необходимости драйвер будет возвращаться к системной памяти, хотя рекомендуется не создавать большое количество куч большого размера.</span><span class="sxs-lookup"><span data-stu-id="276da-128">The driver will fall back on system memory if needed, though it is good practice not to create large numbers of large descriptor heaps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="276da-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="276da-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="276da-130">Кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="276da-130">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




