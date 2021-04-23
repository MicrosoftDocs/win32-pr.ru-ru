---
description: Типы данных, поддерживаемые службой VDS, возвращают возвращаемые функцией значения, параметры функций и члены структуры. Типы данных определяют размер и смысл этих элементов.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Типы данных VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693592"
---
# <a name="vds-data-types"></a><span data-ttu-id="d6b7e-104">Типы данных VDS</span><span class="sxs-lookup"><span data-stu-id="d6b7e-104">VDS Data Types</span></span>

<span data-ttu-id="d6b7e-105">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d6b7e-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="d6b7e-106">Типы данных, поддерживаемые службой VDS, возвращают возвращаемые функцией значения, параметры функций и члены структуры.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-106">The data types supported by VDS define function return values, function parameters, and structure members.</span></span> <span data-ttu-id="d6b7e-107">Типы данных определяют размер и смысл этих элементов.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-107">Data types define the size and meaning of these elements.</span></span>



| <span data-ttu-id="d6b7e-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d6b7e-108">Data type</span></span>                                                                                      | <span data-ttu-id="d6b7e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d6b7e-109">Description</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b7e-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_ИД объекта \_ VDS**</span><span class="sxs-lookup"><span data-stu-id="d6b7e-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS\_OBJECT\_ID**</span></span><br/> | <span data-ttu-id="d6b7e-111">Идентификатор объекта VDS.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-111">VDS object ID.</span></span> <span data-ttu-id="d6b7e-112">Эти значения не обязательно должны быть уникальными во всех перезагрузках.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-112">These values are not guaranteed to be unique across reboots.</span></span> <br/> <span data-ttu-id="d6b7e-113">Этот тип объявлен в службе VDS. h (Вдшвпрв. h для поставщиков оборудования) как GUID.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-113">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a GUID.</span></span> <br/> |
| <span data-ttu-id="d6b7e-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**\_ИД пути к службе VDS \_**</span><span class="sxs-lookup"><span data-stu-id="d6b7e-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS\_PATH\_ID**</span></span><br/>       | <span data-ttu-id="d6b7e-115">ИДЕНТИФИКАТОР пути службы VDS для Multipath I/O (MPIO).</span><span class="sxs-lookup"><span data-stu-id="d6b7e-115">VDS path ID for multipath I/O (MPIO).</span></span> <br/> <span data-ttu-id="d6b7e-116">Этот тип объявлен в службе VDS. h (Вдшвпрв. h для поставщиков оборудования) как UINT64.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-116">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a UINT64.</span></span><br/>                                      |



 

 

