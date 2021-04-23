---
description: Тип перечисления "типы скорости WPD" \_ \_ описывает тип сжатия звуковых файлов.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Перечисление WPD_BITRATE_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718089"
---
# <a name="wpd_bitrate_types-enumeration"></a><span data-ttu-id="61f01-103">\_ \_ Перечисление типов скорости WPD</span><span class="sxs-lookup"><span data-stu-id="61f01-103">WPD\_BITRATE\_TYPES enumeration</span></span>

<span data-ttu-id="61f01-104">Тип перечисления " **\_ \_ типы скорости WPD** " описывает тип сжатия звукового файла.</span><span class="sxs-lookup"><span data-stu-id="61f01-104">The **WPD\_BITRATE\_TYPES** enumeration type describes an audio file's compression type.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f01-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61f01-105">Syntax</span></span>


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="61f01-106">Константы</span><span class="sxs-lookup"><span data-stu-id="61f01-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="61f01-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**тип скорости WPD не \_ \_ \_ используется**</span><span class="sxs-lookup"><span data-stu-id="61f01-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**WPD\_BITRATE\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="61f01-108">Это значение не было указано.</span><span class="sxs-lookup"><span data-stu-id="61f01-108">This value has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="61f01-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_ \_ дискретная скорость типа WPD \_**</span><span class="sxs-lookup"><span data-stu-id="61f01-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD\_BITRATE\_TYPE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="61f01-110">Сжатие постоянной скорости потока.</span><span class="sxs-lookup"><span data-stu-id="61f01-110">Constant bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="61f01-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**\_переменная скорости \_ типа \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="61f01-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD\_BITRATE\_TYPE\_VARIABLE**</span></span>
</dt> <dd>

<span data-ttu-id="61f01-112">Сжатие переменной скорости.</span><span class="sxs-lookup"><span data-stu-id="61f01-112">Variable bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="61f01-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**тип скорости WPD — \_ \_ \_ бесплатный**</span><span class="sxs-lookup"><span data-stu-id="61f01-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD\_BITRATE\_TYPE\_FREE**</span></span>
</dt> <dd>

<span data-ttu-id="61f01-114">Скорость для свободной версии формата.</span><span class="sxs-lookup"><span data-stu-id="61f01-114">Free format bit rate.</span></span> <span data-ttu-id="61f01-115">Это постоянная скорость, которая ниже максимально допустимой скорости.</span><span class="sxs-lookup"><span data-stu-id="61f01-115">This is a constant bit rate that is lower than the maximum allowed bit rate.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61f01-116">Требования</span><span class="sxs-lookup"><span data-stu-id="61f01-116">Requirements</span></span>



| <span data-ttu-id="61f01-117">Требование</span><span class="sxs-lookup"><span data-stu-id="61f01-117">Requirement</span></span> | <span data-ttu-id="61f01-118">Значение</span><span class="sxs-lookup"><span data-stu-id="61f01-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="61f01-119">Header</span><span class="sxs-lookup"><span data-stu-id="61f01-119">Header</span></span><br/> | <dl> <span data-ttu-id="61f01-120"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="61f01-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61f01-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61f01-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f01-122">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="61f01-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




