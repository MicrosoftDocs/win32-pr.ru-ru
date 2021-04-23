---
description: Этот класс является классом типа событий для событий окончания ожидания ALPC. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: Класс ALPC_Unwait
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542767"
---
# <a name="alpc_unwait-class"></a><span data-ttu-id="17dd1-104">Класс "ALPC — \_ Ожидание"</span><span class="sxs-lookup"><span data-stu-id="17dd1-104">ALPC\_Unwait class</span></span>

<span data-ttu-id="17dd1-105">Этот класс является классом типа событий для событий окончания ожидания ALPC.</span><span class="sxs-lookup"><span data-stu-id="17dd1-105">This class is the event type class for ALPC end wait events.</span></span>

<span data-ttu-id="17dd1-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="17dd1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="17dd1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17dd1-107">Syntax</span></span>

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="17dd1-108">Участники</span><span class="sxs-lookup"><span data-stu-id="17dd1-108">Members</span></span>

<span data-ttu-id="17dd1-109">Класс **\_ неожиданий в ALPC** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="17dd1-109">The **ALPC\_Unwait** class has these types of members:</span></span>

-   [<span data-ttu-id="17dd1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="17dd1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17dd1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="17dd1-111">Properties</span></span>

<span data-ttu-id="17dd1-112">Класс **с \_ неожиданием «ALPC** » имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="17dd1-112">The **ALPC\_Unwait** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17dd1-113">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="17dd1-113">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17dd1-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17dd1-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17dd1-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17dd1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17dd1-116">Состояние из операции ожидания.</span><span class="sxs-lookup"><span data-stu-id="17dd1-116">Status from wait operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17dd1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="17dd1-117">Requirements</span></span>



| <span data-ttu-id="17dd1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="17dd1-118">Requirement</span></span> | <span data-ttu-id="17dd1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="17dd1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="17dd1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17dd1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17dd1-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17dd1-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="17dd1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17dd1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17dd1-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17dd1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




