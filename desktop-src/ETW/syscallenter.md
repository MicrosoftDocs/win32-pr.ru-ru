---
description: Этот класс является классом типа события для событий системного вызова Enter. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: Класс Сискаллентер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1497491de622e564b945e8a80fcb1d8755886f39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985700"
---
# <a name="syscallenter-class"></a><span data-ttu-id="f93eb-104">Класс Сискаллентер</span><span class="sxs-lookup"><span data-stu-id="f93eb-104">SysCallEnter class</span></span>

<span data-ttu-id="f93eb-105">Этот класс является классом типа события для событий системного вызова Enter.</span><span class="sxs-lookup"><span data-stu-id="f93eb-105">This class is the event type class for system call enter events.</span></span>

<span data-ttu-id="f93eb-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="f93eb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f93eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f93eb-107">Syntax</span></span>

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a><span data-ttu-id="f93eb-108">Участники</span><span class="sxs-lookup"><span data-stu-id="f93eb-108">Members</span></span>

<span data-ttu-id="f93eb-109">Класс **сискаллентер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f93eb-109">The **SysCallEnter** class has these types of members:</span></span>

-   [<span data-ttu-id="f93eb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f93eb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f93eb-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f93eb-111">Properties</span></span>

<span data-ttu-id="f93eb-112">Класс **сискаллентер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f93eb-112">The **SysCallEnter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f93eb-113">**сискалладдресс**</span><span class="sxs-lookup"><span data-stu-id="f93eb-113">**SysCallAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f93eb-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f93eb-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f93eb-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f93eb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f93eb-116">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="f93eb-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f93eb-117">Адрес вводимых вызовов функции NT.</span><span class="sxs-lookup"><span data-stu-id="f93eb-117">Address of the NT function call that is being entered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f93eb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f93eb-118">Requirements</span></span>



| <span data-ttu-id="f93eb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f93eb-119">Requirement</span></span> | <span data-ttu-id="f93eb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f93eb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f93eb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f93eb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f93eb-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f93eb-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f93eb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f93eb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f93eb-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f93eb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




