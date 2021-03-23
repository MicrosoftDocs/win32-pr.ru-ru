---
title: Таблицы дескрипторов
description: Таблица дескрипторов логически представляет собой набор дескрипторов.
ms.assetid: 5faf294f-acd5-4b39-92f4-1d6b2abe3040
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10414f8458006029f3279203e949b43410911fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103915"
---
# <a name="descriptor-tables"></a><span data-ttu-id="385c3-103">Таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="385c3-103">Descriptor Tables</span></span>

<span data-ttu-id="385c3-104">Таблица дескрипторов логически представляет собой набор дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="385c3-104">A descriptor table is logically an array of descriptors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="385c3-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="385c3-105">In this section</span></span>



| <span data-ttu-id="385c3-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="385c3-106">Topic</span></span>                                                                                 | <span data-ttu-id="385c3-107">Описание</span><span class="sxs-lookup"><span data-stu-id="385c3-107">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="385c3-108">Общие сведения о таблицах дескрипторов</span><span class="sxs-lookup"><span data-stu-id="385c3-108">Descriptor Tables Overview</span></span>](descriptor-tables-overview.md)<br/>               | <span data-ttu-id="385c3-109">Каждая таблица дескрипторов хранит дескрипторы одного или нескольких типов — СРВС, уаве, КБВС и пробы.</span><span class="sxs-lookup"><span data-stu-id="385c3-109">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="385c3-110">Таблица дескрипторов не является выделением памяти; Это просто смещение и длина в куче дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="385c3-110">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span><br/> |
| [<span data-ttu-id="385c3-111">Использование таблиц дескрипторов</span><span class="sxs-lookup"><span data-stu-id="385c3-111">Using Descriptor Tables</span></span>](using-descriptor-tables.md)<br/>                     | <span data-ttu-id="385c3-112">Таблицы дескрипторов, каждый из которых идентифицирует диапазон в куче дескрипторов, привязываются к слотам, определенным текущей корневой подписью в списке команд.</span><span class="sxs-lookup"><span data-stu-id="385c3-112">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span> <br/>                                                               |
| [<span data-ttu-id="385c3-113">Расширенное использование таблиц дескрипторов</span><span class="sxs-lookup"><span data-stu-id="385c3-113">Advanced Use of Descriptor Tables</span></span>](advanced-use-of-descriptor-tables.md)<br/> | <span data-ttu-id="385c3-114">В следующих разделах приводятся сведения о расширенном использовании таблиц дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="385c3-114">The following sections provide information about the advanced use of descriptor tables.</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="385c3-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="385c3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="385c3-116">Кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="385c3-116">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="385c3-117">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="385c3-117">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="385c3-118">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="385c3-118">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





