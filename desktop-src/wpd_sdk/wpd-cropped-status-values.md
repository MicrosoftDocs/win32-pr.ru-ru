---
description: '\_Тип ПЕРЕЧИСЛЕНИЯ WPD "кадрированные \_ значения состояния" \_ описывает состояние кадрирования изображения.'
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: Перечисление WPD_CROPPED_STATUS_VALUES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674839"
---
# <a name="wpd_cropped_status_values-enumeration"></a><span data-ttu-id="58477-103">\_ \_ Перечисление значений состояния КАДРИРОВАНия WPD \_</span><span class="sxs-lookup"><span data-stu-id="58477-103">WPD\_CROPPED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="58477-104">Тип перечисления **WPD " \_ кадрированные \_ \_ значения состояния** " описывает состояние кадрирования изображения.</span><span class="sxs-lookup"><span data-stu-id="58477-104">The **WPD\_CROPPED\_STATUS\_VALUES** enumeration type describes the cropping status of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="58477-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58477-105">Syntax</span></span>


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="58477-106">Константы</span><span class="sxs-lookup"><span data-stu-id="58477-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="58477-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_состояние кадрирования \_ WPD \_ не \_ обрезано**</span><span class="sxs-lookup"><span data-stu-id="58477-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**WPD\_CROPPED\_STATUS\_NOT\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="58477-108">Изображение не обрезано.</span><span class="sxs-lookup"><span data-stu-id="58477-108">The image has not been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="58477-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**обрезанное \_ \_ состояние WPD \_**</span><span class="sxs-lookup"><span data-stu-id="58477-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**WPD\_CROPPED\_STATUS\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="58477-110">Изображение обрезано.</span><span class="sxs-lookup"><span data-stu-id="58477-110">The image has been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="58477-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**\_состояние кадрирования \_ WPD \_ \_ не следует \_ \_ обрезать**</span><span class="sxs-lookup"><span data-stu-id="58477-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**WPD\_CROPPED\_STATUS\_SHOULD\_NOT\_BE\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="58477-112">Изображение не было, и его не следует обрезать.</span><span class="sxs-lookup"><span data-stu-id="58477-112">The image has not been, and should not be, cropped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58477-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58477-113">Remarks</span></span>

<span data-ttu-id="58477-114">Обозначает обрезанное состояние изображения.</span><span class="sxs-lookup"><span data-stu-id="58477-114">Indicates the cropped status of an image.</span></span> <span data-ttu-id="58477-115">Это перечисление используется свойством " [ \_ \_ \_ состояние кадрирования изображения WPD](image-properties.md) ".</span><span class="sxs-lookup"><span data-stu-id="58477-115">This enumeration is used by the [WPD\_IMAGE\_CROPPED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="58477-116">Требования</span><span class="sxs-lookup"><span data-stu-id="58477-116">Requirements</span></span>



| <span data-ttu-id="58477-117">Требование</span><span class="sxs-lookup"><span data-stu-id="58477-117">Requirement</span></span> | <span data-ttu-id="58477-118">Значение</span><span class="sxs-lookup"><span data-stu-id="58477-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="58477-119">Header</span><span class="sxs-lookup"><span data-stu-id="58477-119">Header</span></span><br/> | <dl> <span data-ttu-id="58477-120"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="58477-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58477-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58477-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58477-122">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="58477-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




