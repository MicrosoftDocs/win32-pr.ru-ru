---
description: Этот класс является классом типа событий для событий возврата запроса драйвера. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 04505f8c-a11e-4bf7-91c0-fca1b5846d80
title: Класс Дриверкомплетерекуестретурн
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequestReturn
- DriverCompleteRequestReturn.Irp
- DriverCompleteRequestReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c147573578e067b7fb1b588545a1d9f231e35f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540367"
---
# <a name="drivercompleterequestreturn-class"></a><span data-ttu-id="ef679-104">Класс Дриверкомплетерекуестретурн</span><span class="sxs-lookup"><span data-stu-id="ef679-104">DriverCompleteRequestReturn class</span></span>

<span data-ttu-id="ef679-105">Этот класс является классом типа событий для событий возврата запроса драйвера.</span><span class="sxs-lookup"><span data-stu-id="ef679-105">This class is the event type class for driver complete request return events.</span></span>

<span data-ttu-id="ef679-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="ef679-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef679-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef679-107">Syntax</span></span>

``` syntax
[EventType{53}, EventTypeName{"DrvComplReqRet"}]
class DriverCompleteRequestReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="ef679-108">Участники</span><span class="sxs-lookup"><span data-stu-id="ef679-108">Members</span></span>

<span data-ttu-id="ef679-109">Класс **дриверкомплетерекуестретурн** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ef679-109">The **DriverCompleteRequestReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="ef679-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef679-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef679-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef679-111">Properties</span></span>

<span data-ttu-id="ef679-112">Класс **дриверкомплетерекуестретурн** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ef679-112">The **DriverCompleteRequestReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef679-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="ef679-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef679-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef679-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef679-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef679-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef679-116">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="ef679-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ef679-117">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="ef679-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="ef679-118">**уникматчид**</span><span class="sxs-lookup"><span data-stu-id="ef679-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef679-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef679-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef679-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef679-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef679-121">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="ef679-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="ef679-122">Идентификатор, который однозначно идентифицирует запрос.</span><span class="sxs-lookup"><span data-stu-id="ef679-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="ef679-123">Используйте этот идентификатор для сопоставления с другими событиями драйвера, например с событием [**дриверкомплетерекуест**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="ef679-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef679-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ef679-124">Requirements</span></span>



| <span data-ttu-id="ef679-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ef679-125">Requirement</span></span> | <span data-ttu-id="ef679-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ef679-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef679-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef679-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ef679-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef679-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ef679-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef679-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ef679-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ef679-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef679-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef679-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef679-132">**дискио**</span><span class="sxs-lookup"><span data-stu-id="ef679-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




