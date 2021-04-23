---
description: Задает элементы структуры НМКОЛУМНВАРИАНТ.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: Перечисление НМКОЛУМНТИПЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3c88d001ce3ccf1ebfe1e28855ae9df9fca5d327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818521"
---
# <a name="nmcolumntype-enumeration"></a><span data-ttu-id="a598b-103">Перечисление НМКОЛУМНТИПЕ</span><span class="sxs-lookup"><span data-stu-id="a598b-103">NMCOLUMNTYPE enumeration</span></span>

<span data-ttu-id="a598b-104">Перечисление **нмколумнтипе** указывает элементы структуры [**нмколумнвариант**](nmcolumnvariant.md) .</span><span class="sxs-lookup"><span data-stu-id="a598b-104">The **NMCOLUMNTYPE** enumeration specifies the members of the [**NMCOLUMNVARIANT**](nmcolumnvariant.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a598b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a598b-105">Syntax</span></span>


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a><span data-ttu-id="a598b-106">Константы</span><span class="sxs-lookup"><span data-stu-id="a598b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a598b-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**НМКОЛУМНТИПЕ \_ UINT8**</span><span class="sxs-lookup"><span data-stu-id="a598b-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE\_UINT8**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-108">8-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a598b-108">8-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**НМКОЛУМНТИПЕ \_ SINT8**</span><span class="sxs-lookup"><span data-stu-id="a598b-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE\_SINT8**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-110">8-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="a598b-110">8-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**НМКОЛУМНТИПЕ \_ UINT16**</span><span class="sxs-lookup"><span data-stu-id="a598b-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE\_UINT16**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-112">16-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a598b-112">16-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**НМКОЛУМНТИПЕ \_ SINT16**</span><span class="sxs-lookup"><span data-stu-id="a598b-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE\_SINT16**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-114">16-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="a598b-114">16-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**НМКОЛУМНТИПЕ \_ UINT32**</span><span class="sxs-lookup"><span data-stu-id="a598b-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE\_UINT32**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-116">32-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="a598b-116">32-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**НМКОЛУМНТИПЕ \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="a598b-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE\_SINT32**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-118">32-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="a598b-118">32-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**НМКОЛУМНТИПЕ \_ FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="a598b-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE\_FLOAT64**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-120">64-разрядное число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="a598b-120">64-bit float.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**НМКОЛУМНТИПЕ \_ рамка**</span><span class="sxs-lookup"><span data-stu-id="a598b-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**NMCOLUMNTYPE\_FRAME**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-122">Номер кадра.</span><span class="sxs-lookup"><span data-stu-id="a598b-122">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**НМКОЛУМНТИПЕ \_ Данет**</span><span class="sxs-lookup"><span data-stu-id="a598b-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE\_YESNO**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-124">"Yes" или "No".</span><span class="sxs-lookup"><span data-stu-id="a598b-124">"Yes" or "No".</span></span>

</dd> <dt>

<span data-ttu-id="a598b-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**НМКОЛУМНТИПЕ \_ онофф**</span><span class="sxs-lookup"><span data-stu-id="a598b-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE\_ONOFF**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-126">"On" или "OFF"</span><span class="sxs-lookup"><span data-stu-id="a598b-126">"On" or "Off"</span></span>

</dd> <dt>

<span data-ttu-id="a598b-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**НМКОЛУМНТИПЕ \_ труефалсе**</span><span class="sxs-lookup"><span data-stu-id="a598b-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE\_TRUEFALSE**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-128">"True" или "false".</span><span class="sxs-lookup"><span data-stu-id="a598b-128">"True" or "False".</span></span>

</dd> <dt>

<span data-ttu-id="a598b-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**НМКОЛУМНТИПЕ \_ макаддр**</span><span class="sxs-lookup"><span data-stu-id="a598b-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE\_MACADDR**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-130">MAC-адрес.</span><span class="sxs-lookup"><span data-stu-id="a598b-130">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**НМКОЛУМНТИПЕ \_ ипксаддр**</span><span class="sxs-lookup"><span data-stu-id="a598b-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE\_IPXADDR**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-132">IPX-адрес.</span><span class="sxs-lookup"><span data-stu-id="a598b-132">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**НМКОЛУМНТИПЕ \_ reduce**</span><span class="sxs-lookup"><span data-stu-id="a598b-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE\_IPADDR**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-134">IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a598b-134">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**НМКОЛУМНТИПЕ \_ вартиме**</span><span class="sxs-lookup"><span data-stu-id="a598b-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE\_VARTIME**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-136">Вариант времени.</span><span class="sxs-lookup"><span data-stu-id="a598b-136">Variant time.</span></span>

</dd> <dt>

<span data-ttu-id="a598b-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**\_строка нмколумнтипе**</span><span class="sxs-lookup"><span data-stu-id="a598b-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**NMCOLUMNTYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="a598b-138">Указатель на строку.</span><span class="sxs-lookup"><span data-stu-id="a598b-138">Pointer to a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a598b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="a598b-139">Requirements</span></span>



| <span data-ttu-id="a598b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="a598b-140">Requirement</span></span> | <span data-ttu-id="a598b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="a598b-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a598b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a598b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a598b-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a598b-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a598b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a598b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a598b-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a598b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a598b-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a598b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a598b-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a598b-147"><dt>Netmon.h</dt></span></span> </dl> |



 

 




