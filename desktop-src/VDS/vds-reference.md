---
description: В этом разделе описывается интерфейс программирования приложений для службы виртуальных дисков (VDS).
ms.assetid: d00fc772-331f-4d71-a418-e34acdfb6652
title: Ссылка на службу VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369111add0b3f4b7e2742c764a6cbf8b1d8bfdd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673880"
---
# <a name="vds-reference"></a><span data-ttu-id="55529-103">Ссылка на службу VDS</span><span class="sxs-lookup"><span data-stu-id="55529-103">VDS Reference</span></span>

<span data-ttu-id="55529-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="55529-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="55529-105">В этом разделе описывается интерфейс программирования приложений для службы виртуальных дисков (VDS).</span><span class="sxs-lookup"><span data-stu-id="55529-105">This section describes the application programming interface to the Virtual Disk Service (VDS).</span></span>

<span data-ttu-id="55529-106">Разработчики приложений используют интерфейсы, структуры, перечисления и символьные константы в этом API для запроса и настройки хранилища — от дисков до массивов хранения.</span><span class="sxs-lookup"><span data-stu-id="55529-106">Application developers use the interfaces, structures, enumerations, and symbolic constants in this API to query and configure storage—from disks to storage arrays.</span></span> <span data-ttu-id="55529-107">Подробный обзор отношений между типами VDS см. в разделе [объектная модель VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="55529-107">For a detailed look at the relationship among VDS types, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="55529-108">Производители хранилища реализуют множество интерфейсов, определенных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="55529-108">Storage manufacturers implement many of the interfaces defined in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="55529-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="55529-109">In this Section</span></span>

<dl> <dt>

[<span data-ttu-id="55529-110">Константы службы VDS</span><span class="sxs-lookup"><span data-stu-id="55529-110">VDS Constants</span></span>](vds-constants.md)
</dt> <dd>

<span data-ttu-id="55529-111">Список символьных констант в API службы VDS.</span><span class="sxs-lookup"><span data-stu-id="55529-111">Lists the symbolic constants in the VDS API.</span></span>

</dd> <dt>

[<span data-ttu-id="55529-112">Типы данных VDS</span><span class="sxs-lookup"><span data-stu-id="55529-112">VDS Data Types</span></span>](vds-data-types.md)
</dt> <dd>

<span data-ttu-id="55529-113">Список типов данных, используемых службой VDS.</span><span class="sxs-lookup"><span data-stu-id="55529-113">Lists the data types used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="55529-114">Перечисления VDS</span><span class="sxs-lookup"><span data-stu-id="55529-114">VDS Enumerations</span></span>](vds-enumerations.md)
</dt> <dd>

<span data-ttu-id="55529-115">Описывает перечисления, используемые с VDS.</span><span class="sxs-lookup"><span data-stu-id="55529-115">Describes the enumerations used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="55529-116">Интерфейсы VDS</span><span class="sxs-lookup"><span data-stu-id="55529-116">VDS Interfaces</span></span>](vds-interfaces.md)
</dt> <dd>

<span data-ttu-id="55529-117">Описание интерфейсов VDS и методов, которые они предоставляют.</span><span class="sxs-lookup"><span data-stu-id="55529-117">Describes VDS interfaces and the methods they expose.</span></span>

</dd> <dt>

[<span data-ttu-id="55529-118">Структуры VDS</span><span class="sxs-lookup"><span data-stu-id="55529-118">VDS Structures</span></span>](vds-structures.md)
</dt> <dd>

<span data-ttu-id="55529-119">Описывает структуры, передаваемые в качестве параметров методам VDS.</span><span class="sxs-lookup"><span data-stu-id="55529-119">Describes the structures passed as parameters to VDS methods.</span></span>

</dd> <dt>

[<span data-ttu-id="55529-120">Общие коды возврата для службы виртуальных дисков</span><span class="sxs-lookup"><span data-stu-id="55529-120">Virtual Disk Service Common Return Codes</span></span>](virtual-disk-service-common-return-codes.md)
</dt> <dd>

<span data-ttu-id="55529-121">Описание наиболее распространенных кодов ошибок, характерных для VDS.</span><span class="sxs-lookup"><span data-stu-id="55529-121">Describes the most common error codes that are specific to VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="55529-122">Глоссарий службы виртуальных дисков</span><span class="sxs-lookup"><span data-stu-id="55529-122">Virtual Disk Service Glossary</span></span>](virtual-disk-service-glossary-all.md)
</dt> <dd>

<span data-ttu-id="55529-123">Глоссарий технических терминов, используемых в документации по службе VDS.</span><span class="sxs-lookup"><span data-stu-id="55529-123">Glossary of technical terms used in VDS documentation.</span></span>

</dd> </dl>

 

 
