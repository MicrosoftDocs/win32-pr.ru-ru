---
description: Тип перечисления "WPD SMS Encoding Types" \_ \_ \_ описывает тип кодировки сообщения SMS.
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Перечисление WPD_SMS_ENCODING_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648986"
---
# <a name="wpd_sms_encoding_types-enumeration"></a><span data-ttu-id="a2ba1-103">\_ \_ \_ Перечисление типов кодирования SMS типа WPD</span><span class="sxs-lookup"><span data-stu-id="a2ba1-103">WPD\_SMS\_ENCODING\_TYPES enumeration</span></span>

<span data-ttu-id="a2ba1-104">Тип перечисления " **WPD \_ SMS \_ Encoding \_** Types" описывает тип кодировки сообщения SMS.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-104">The **WPD\_SMS\_ENCODING\_TYPES** enumeration type describes the encoding type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ba1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2ba1-105">Syntax</span></span>


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="a2ba1-106">Константы</span><span class="sxs-lookup"><span data-stu-id="a2ba1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a2ba1-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**\_Кодировка SMS \_ 7 \_ bit**</span><span class="sxs-lookup"><span data-stu-id="a2ba1-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS\_ENCODING\_7\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="a2ba1-108">7-разрядная кодировка.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-108">Seven-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="a2ba1-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**\_ \_ 8 бит кодирования \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="a2ba1-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS\_ENCODING\_8\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="a2ba1-110">8-разрядная кодировка.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-110">Eight-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="a2ba1-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**\_Кодирование SMS \_ UTF \_ 16**</span><span class="sxs-lookup"><span data-stu-id="a2ba1-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS\_ENCODING\_UTF\_16**</span></span>
</dt> <dd>

<span data-ttu-id="a2ba1-112">16-битная кодировка (UTF).</span><span class="sxs-lookup"><span data-stu-id="a2ba1-112">Sixteen-bit encoding (UTF).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2ba1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2ba1-113">Remarks</span></span>

<span data-ttu-id="a2ba1-114">Это перечисление используется свойством [ \_ \_ кодирования WPD в SMS](sms-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ba1-114">This enumeration is used by the [WPD\_SMS\_ENCODING](sms-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ba1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a2ba1-115">Requirements</span></span>



| <span data-ttu-id="a2ba1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a2ba1-116">Requirement</span></span> | <span data-ttu-id="a2ba1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a2ba1-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ba1-118">Header</span><span class="sxs-lookup"><span data-stu-id="a2ba1-118">Header</span></span><br/> | <dl> <span data-ttu-id="a2ba1-119"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ba1-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2ba1-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2ba1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ba1-121">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="a2ba1-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




