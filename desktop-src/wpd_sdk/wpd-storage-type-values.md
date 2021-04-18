---
description: Тип перечисления "WPD- \_ тип хранилища" \_ \_ описывает различные типы хранилищ переносных устройств Windows.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Перечисление WPD_STORAGE_TYPE_VALUES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648781"
---
# <a name="wpd_storage_type_values-enumeration"></a><span data-ttu-id="69d51-103">\_ \_ Перечисление значений типа хранилища WPD \_</span><span class="sxs-lookup"><span data-stu-id="69d51-103">WPD\_STORAGE\_TYPE\_VALUES enumeration</span></span>

<span data-ttu-id="69d51-104">Тип перечисления " **WPD- \_ \_ тип \_ хранилища** " описывает различные типы хранилищ переносных устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="69d51-104">The **WPD\_STORAGE\_TYPE\_VALUES** enumeration type describes the different Windows Portable Device storage types.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d51-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69d51-105">Syntax</span></span>


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a><span data-ttu-id="69d51-106">Константы</span><span class="sxs-lookup"><span data-stu-id="69d51-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="69d51-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**\_тип хранилища WPD не \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="69d51-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD\_STORAGE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="69d51-108">Хранилище имеет неопределенный тип.</span><span class="sxs-lookup"><span data-stu-id="69d51-108">The storage is of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="69d51-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**\_тип хранилища WPD — \_ \_ фиксированное \_ ПЗУ**</span><span class="sxs-lookup"><span data-stu-id="69d51-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD\_STORAGE\_TYPE\_FIXED\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="69d51-110">Хранилище не является съемным и доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="69d51-110">The storage is non-removable and read-only.</span></span>

</dd> <dt>

<span data-ttu-id="69d51-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_тип хранилища WPD — \_ \_ съемные \_ диски**</span><span class="sxs-lookup"><span data-stu-id="69d51-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="69d51-112">Хранилище является съемным и доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="69d51-112">The storage is removable and is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="69d51-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_тип хранилища \_ WPD \_ фиксированный \_ объем ОЗУ**</span><span class="sxs-lookup"><span data-stu-id="69d51-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**WPD\_STORAGE\_TYPE\_FIXED\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="69d51-114">Хранилище не является съемным и доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="69d51-114">The storage is non-removable and is read/write capable.</span></span>

</dd> <dt>

<span data-ttu-id="69d51-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_тип хранилища WPD — \_ \_ съемная \_ оперативная память**</span><span class="sxs-lookup"><span data-stu-id="69d51-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="69d51-116">Хранилище является съемным и доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="69d51-116">The storage is removable and is read/write capable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69d51-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69d51-117">Remarks</span></span>

<span data-ttu-id="69d51-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="69d51-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d51-119">Требования</span><span class="sxs-lookup"><span data-stu-id="69d51-119">Requirements</span></span>



| <span data-ttu-id="69d51-120">Требование</span><span class="sxs-lookup"><span data-stu-id="69d51-120">Requirement</span></span> | <span data-ttu-id="69d51-121">Значение</span><span class="sxs-lookup"><span data-stu-id="69d51-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="69d51-122">Header</span><span class="sxs-lookup"><span data-stu-id="69d51-122">Header</span></span><br/> | <dl> <span data-ttu-id="69d51-123"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d51-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69d51-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69d51-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d51-125">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="69d51-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




