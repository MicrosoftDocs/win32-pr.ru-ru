---
description: Этот класс является классом типа события для событий выхода из системного вызова. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: Класс Сискаллексит
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985697"
---
# <a name="syscallexit-class"></a><span data-ttu-id="35e18-104">Класс Сискаллексит</span><span class="sxs-lookup"><span data-stu-id="35e18-104">SysCallExit class</span></span>

<span data-ttu-id="35e18-105">Этот класс является классом типа события для событий выхода из системного вызова.</span><span class="sxs-lookup"><span data-stu-id="35e18-105">This class is the event type class for system call exit events.</span></span>

<span data-ttu-id="35e18-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="35e18-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e18-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35e18-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a><span data-ttu-id="35e18-108">Участники</span><span class="sxs-lookup"><span data-stu-id="35e18-108">Members</span></span>

<span data-ttu-id="35e18-109">Класс **сискаллексит** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="35e18-109">The **SysCallExit** class has these types of members:</span></span>

-   [<span data-ttu-id="35e18-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="35e18-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35e18-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="35e18-111">Properties</span></span>

<span data-ttu-id="35e18-112">Класс **сискаллексит** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="35e18-112">The **SysCallExit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35e18-113">**сискаллнтстатус**</span><span class="sxs-lookup"><span data-stu-id="35e18-113">**SysCallNtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e18-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35e18-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35e18-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="35e18-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e18-116">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="35e18-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="35e18-117">Код состояния, возвращенный системным вызовом NT.</span><span class="sxs-lookup"><span data-stu-id="35e18-117">Status code returned by the NT system call.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35e18-118">Требования</span><span class="sxs-lookup"><span data-stu-id="35e18-118">Requirements</span></span>



| <span data-ttu-id="35e18-119">Требование</span><span class="sxs-lookup"><span data-stu-id="35e18-119">Requirement</span></span> | <span data-ttu-id="35e18-120">Значение</span><span class="sxs-lookup"><span data-stu-id="35e18-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35e18-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35e18-121">Minimum supported client</span></span><br/> | <span data-ttu-id="35e18-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35e18-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35e18-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35e18-123">Minimum supported server</span></span><br/> | <span data-ttu-id="35e18-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35e18-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




