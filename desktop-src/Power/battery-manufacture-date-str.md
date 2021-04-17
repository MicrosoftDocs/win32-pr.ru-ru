---
description: Содержит дату изготовления аккумулятора.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: Структура BATTERY_MANUFACTURE_DATE (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663129"
---
# <a name="battery_manufacture_date-structure"></a><span data-ttu-id="daff2-103">\_ \_ Структура даты изготовления аккумулятора</span><span class="sxs-lookup"><span data-stu-id="daff2-103">BATTERY\_MANUFACTURE\_DATE structure</span></span>

<span data-ttu-id="daff2-104">Содержит дату изготовления аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="daff2-104">Contains the date of manufacture of a battery.</span></span> <span data-ttu-id="daff2-105">Эта структура используется структурой [**\_ \_ сведений о заряде аккумулятора**](battery-query-information-str.md) при запросе уровня информации баттеримануфактуредате.</span><span class="sxs-lookup"><span data-stu-id="daff2-105">This structure is used by the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure when the BatteryManufactureDate information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="daff2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daff2-106">Syntax</span></span>


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a><span data-ttu-id="daff2-107">Члены</span><span class="sxs-lookup"><span data-stu-id="daff2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="daff2-108">**День**</span><span class="sxs-lookup"><span data-stu-id="daff2-108">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="daff2-109">День изготовления месяца в диапазоне от 1 до 31.</span><span class="sxs-lookup"><span data-stu-id="daff2-109">The day of the month of manufacture, in the range 1 to 31.</span></span> <span data-ttu-id="daff2-110">Несмотря на тип данных, это значение не кодируется в кодировке ASCII.</span><span class="sxs-lookup"><span data-stu-id="daff2-110">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="daff2-111">Это байт без знака.</span><span class="sxs-lookup"><span data-stu-id="daff2-111">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="daff2-112">**Месяц**</span><span class="sxs-lookup"><span data-stu-id="daff2-112">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="daff2-113">Месяц изготовления в диапазоне от 1 (январь) до 12 (декабрь).</span><span class="sxs-lookup"><span data-stu-id="daff2-113">The month of manufacture, in the range 1 (January) to 12 (December).</span></span> <span data-ttu-id="daff2-114">Несмотря на тип данных, это значение не кодируется в кодировке ASCII.</span><span class="sxs-lookup"><span data-stu-id="daff2-114">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="daff2-115">Это байт без знака.</span><span class="sxs-lookup"><span data-stu-id="daff2-115">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="daff2-116">**Год**</span><span class="sxs-lookup"><span data-stu-id="daff2-116">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="daff2-117">Год изготовления.</span><span class="sxs-lookup"><span data-stu-id="daff2-117">The year of manufacture.</span></span> <span data-ttu-id="daff2-118">Обычно они находятся в диапазоне 1900-2100.</span><span class="sxs-lookup"><span data-stu-id="daff2-118">This will typically be in the range 1900-2100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="daff2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="daff2-119">Remarks</span></span>

<span data-ttu-id="daff2-120">Дата кодируется в григорианском или Западной календарном формате.</span><span class="sxs-lookup"><span data-stu-id="daff2-120">The date is encoded in the Gregorian or western calendar format.</span></span>

## <a name="requirements"></a><span data-ttu-id="daff2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="daff2-121">Requirements</span></span>



| <span data-ttu-id="daff2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="daff2-122">Requirement</span></span> | <span data-ttu-id="daff2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="daff2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daff2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="daff2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="daff2-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="daff2-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="daff2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="daff2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="daff2-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="daff2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="daff2-128">Header</span><span class="sxs-lookup"><span data-stu-id="daff2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="daff2-129"><dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="daff2-129"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daff2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="daff2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daff2-131">**\_ \_ сведения о запросе аккумулятора**</span><span class="sxs-lookup"><span data-stu-id="daff2-131">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="daff2-132">**\_ \_ сведения о запросе от аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="daff2-132">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




