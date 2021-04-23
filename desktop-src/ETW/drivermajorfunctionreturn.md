---
description: Этот класс является классом типа события для событий возврата вызова основной функции драйвера. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: Класс Дривермажорфунктионретурн
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21340224253d1eb3f3ddc733bf2d43e847844282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540359"
---
# <a name="drivermajorfunctionreturn-class"></a><span data-ttu-id="4b28e-104">Класс Дривермажорфунктионретурн</span><span class="sxs-lookup"><span data-stu-id="4b28e-104">DriverMajorFunctionReturn class</span></span>

<span data-ttu-id="4b28e-105">Этот класс является классом типа события для событий возврата вызова основной функции драйвера.</span><span class="sxs-lookup"><span data-stu-id="4b28e-105">This class is the event type class for driver major function call return events.</span></span>

<span data-ttu-id="4b28e-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="4b28e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b28e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b28e-107">Syntax</span></span>

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="4b28e-108">Участники</span><span class="sxs-lookup"><span data-stu-id="4b28e-108">Members</span></span>

<span data-ttu-id="4b28e-109">Класс **дривермажорфунктионретурн** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4b28e-109">The **DriverMajorFunctionReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="4b28e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b28e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b28e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b28e-111">Properties</span></span>

<span data-ttu-id="4b28e-112">Класс **дривермажорфунктионретурн** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4b28e-112">The **DriverMajorFunctionReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b28e-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="4b28e-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b28e-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b28e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b28e-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b28e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b28e-116">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="4b28e-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4b28e-117">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="4b28e-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="4b28e-118">**уникматчид**</span><span class="sxs-lookup"><span data-stu-id="4b28e-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b28e-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b28e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b28e-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b28e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b28e-121">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="4b28e-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4b28e-122">Идентификатор, который однозначно идентифицирует запрос.</span><span class="sxs-lookup"><span data-stu-id="4b28e-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="4b28e-123">Используйте этот идентификатор для сопоставления с другими событиями драйвера, например с событием [**дриверкомплетерекуест**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="4b28e-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b28e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4b28e-124">Requirements</span></span>



| <span data-ttu-id="4b28e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4b28e-125">Requirement</span></span> | <span data-ttu-id="4b28e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4b28e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b28e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b28e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4b28e-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b28e-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b28e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b28e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4b28e-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b28e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b28e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b28e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b28e-132">**дискио**</span><span class="sxs-lookup"><span data-stu-id="4b28e-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




