---
description: Этот класс является классом типа события для разбиения событий ввода-вывода. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: Класс SplitIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 469c8f04664f72b88e5a4378cb318b52f32fba24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912599"
---
# <a name="splitio_info-class"></a><span data-ttu-id="7457a-104">\_Класс сведений сплитио</span><span class="sxs-lookup"><span data-stu-id="7457a-104">SplitIo\_Info class</span></span>

<span data-ttu-id="7457a-105">Этот класс является классом типа события для разбиения событий ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="7457a-105">This class is the event type class for split IO events.</span></span>

<span data-ttu-id="7457a-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="7457a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7457a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7457a-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a><span data-ttu-id="7457a-108">Участники</span><span class="sxs-lookup"><span data-stu-id="7457a-108">Members</span></span>

<span data-ttu-id="7457a-109">Класс **\_ сведений сплитио** содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7457a-109">The **SplitIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="7457a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7457a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7457a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7457a-111">Properties</span></span>

<span data-ttu-id="7457a-112">Класс **\_ сведений сплитио** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7457a-112">The **SplitIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7457a-113">**чилдирп**</span><span class="sxs-lookup"><span data-stu-id="7457a-113">**ChildIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7457a-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7457a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7457a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7457a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7457a-116">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="7457a-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7457a-117">Пакет запроса дочернего ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="7457a-117">Child IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="7457a-118">**парентирп**</span><span class="sxs-lookup"><span data-stu-id="7457a-118">**ParentIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7457a-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7457a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7457a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7457a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7457a-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="7457a-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7457a-122">Пакет запроса родительского ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="7457a-122">Parent IO request packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7457a-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="7457a-123">Remarks</span></span>

<span data-ttu-id="7457a-124">Указывает, что диспетчер томов разделяет IRP на два запроса IRP.</span><span class="sxs-lookup"><span data-stu-id="7457a-124">Indicates that the volume manager split the IRP into two IRPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="7457a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7457a-125">Requirements</span></span>



| <span data-ttu-id="7457a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7457a-126">Requirement</span></span> | <span data-ttu-id="7457a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7457a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7457a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7457a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7457a-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7457a-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7457a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7457a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7457a-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7457a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




