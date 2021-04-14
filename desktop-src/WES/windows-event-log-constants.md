---
title: Константы журнала событий Windows (Виневт. h)
description: В журнале событий Windows определены следующие константы
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415488"
---
# <a name="windows-event-log-constants"></a><span data-ttu-id="52f77-103">Константы журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="52f77-103">Windows Event Log Constants</span></span>

<span data-ttu-id="52f77-104">В журнале событий Windows определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="52f77-104">Windows Event Log defines the following constants:</span></span>

<dl> <dt>

<span data-ttu-id="52f77-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**\_ \_ маска типа варианта \_ evt**</span><span class="sxs-lookup"><span data-stu-id="52f77-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f77-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="52f77-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="52f77-107">Битовая маска, используемая для маскирования бита массива типа Variant, чтобы можно было определить тип данных значения типа Variant, содержащегося в структуре [**evt \_ Variant**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) .</span><span class="sxs-lookup"><span data-stu-id="52f77-107">A bitmask that you use to mask out the array bit of the variant type, so you can determine the data type of the variant value that the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure contains.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52f77-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**\_массив вариативных \_ типов \_ Variant**</span><span class="sxs-lookup"><span data-stu-id="52f77-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f77-109">128</span><span class="sxs-lookup"><span data-stu-id="52f77-109">128</span></span>
</dt> <dt>



<span data-ttu-id="52f77-110">Этот бит устанавливается для элемента **типа** в структуре параметра [**evt \_**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) , если вариант содержит указатель на массив значений, а не само значение.</span><span class="sxs-lookup"><span data-stu-id="52f77-110">The **Type** member of the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure has this bit set if the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52f77-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**проevt \_ доступ на чтение \_**</span><span class="sxs-lookup"><span data-stu-id="52f77-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f77-112">0x1</span><span class="sxs-lookup"><span data-stu-id="52f77-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="52f77-113">Разрешение на управление доступом на чтение, позволяющее считывать данные из журнала событий.</span><span class="sxs-lookup"><span data-stu-id="52f77-113">Read access control permission that allows information to be read from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52f77-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**\_доступ на запись для ПРОevt \_**</span><span class="sxs-lookup"><span data-stu-id="52f77-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**EVT\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f77-115">0x2</span><span class="sxs-lookup"><span data-stu-id="52f77-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="52f77-116">Разрешение на запись контроля доступа, позволяющее записывать данные в журнал событий.</span><span class="sxs-lookup"><span data-stu-id="52f77-116">Write access control permission that allows information to be written to an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52f77-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**\_четкий \_ доступ к evt**</span><span class="sxs-lookup"><span data-stu-id="52f77-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT\_CLEAR\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f77-118">0x4</span><span class="sxs-lookup"><span data-stu-id="52f77-118">0x4</span></span>
</dt> <dt>



<span data-ttu-id="52f77-119">Очистите разрешение на контроль доступа, позволяющее очищать всю информацию из журнала событий.</span><span class="sxs-lookup"><span data-stu-id="52f77-119">Clear access control permission that allows all information to be cleared from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52f77-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**проevt \_ весь \_ доступ**</span><span class="sxs-lookup"><span data-stu-id="52f77-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f77-121">0x7</span><span class="sxs-lookup"><span data-stu-id="52f77-121">0x7</span></span>
</dt> <dt>



<span data-ttu-id="52f77-122">Все разрешения на управление доступом (чтение, запись, очистка и удаление).</span><span class="sxs-lookup"><span data-stu-id="52f77-122">All (read, write, clear, and delete) access control permission.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52f77-123">Требования</span><span class="sxs-lookup"><span data-stu-id="52f77-123">Requirements</span></span>



| <span data-ttu-id="52f77-124">Требование</span><span class="sxs-lookup"><span data-stu-id="52f77-124">Requirement</span></span> | <span data-ttu-id="52f77-125">Значение</span><span class="sxs-lookup"><span data-stu-id="52f77-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52f77-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52f77-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52f77-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52f77-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="52f77-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52f77-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52f77-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52f77-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52f77-130">Header</span><span class="sxs-lookup"><span data-stu-id="52f77-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="52f77-131"><dt>Виневт. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f77-131"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





