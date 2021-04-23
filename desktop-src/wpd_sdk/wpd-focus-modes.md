---
description: '\_Тип ПЕРЕЧИСЛЕНИЯ WPD Focus modes \_ описывает режим фокусировки, используемый устройством захвата образа.'
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Перечисление WPD_FOCUS_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668681"
---
# <a name="wpd_focus_modes-enumeration"></a><span data-ttu-id="5f4c5-103">\_ \_ Перечисление режимов фокусировки WPD</span><span class="sxs-lookup"><span data-stu-id="5f4c5-103">WPD\_FOCUS\_MODES enumeration</span></span>

<span data-ttu-id="5f4c5-104">Тип **перечисления \_ WPD \_ Focus** Modes описывает режим фокусировки, используемый устройством захвата образа.</span><span class="sxs-lookup"><span data-stu-id="5f4c5-104">The **WPD\_FOCUS\_MODES** enumeration type describes the focus mode used by a still image capture device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f4c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f4c5-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="5f4c5-106">Константы</span><span class="sxs-lookup"><span data-stu-id="5f4c5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5f4c5-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**фокус WPD не \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="5f4c5-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD\_FOCUS\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="5f4c5-108">Режим фокусировки не указан.</span><span class="sxs-lookup"><span data-stu-id="5f4c5-108">The focus mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="5f4c5-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**\_руководство по возфокусу WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f4c5-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD\_FOCUS\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="5f4c5-110">Указывает ручной фокус.</span><span class="sxs-lookup"><span data-stu-id="5f4c5-110">Specifies manual focus.</span></span>

</dd> <dt>

<span data-ttu-id="5f4c5-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**\_Автоматический фокус в WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f4c5-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD\_FOCUS\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="5f4c5-112">Задает автоматический фокус, управляемый устройством.</span><span class="sxs-lookup"><span data-stu-id="5f4c5-112">Specifies automatic focus, controlled by the device.</span></span>

</dd> <dt>

<span data-ttu-id="5f4c5-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_ \_ автоматический макрос ФОКУСа WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f4c5-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD\_FOCUS\_AUTOMATIC\_MACRO**</span></span>
</dt> <dd>

<span data-ttu-id="5f4c5-114">Указывает, что устройство должно автоматически переключаться между макросом и нормальным фокусом при необходимости.</span><span class="sxs-lookup"><span data-stu-id="5f4c5-114">Specifies that the device should automatically switch between macro and normal focus, as required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f4c5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f4c5-115">Remarks</span></span>

<span data-ttu-id="5f4c5-116">Это перечисление используется в свойстве [ \_ \_ \_ \_ режима фокусировки WPD-изображений](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="5f4c5-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_FOCUS\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f4c5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5f4c5-117">Requirements</span></span>



| <span data-ttu-id="5f4c5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5f4c5-118">Requirement</span></span> | <span data-ttu-id="5f4c5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5f4c5-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f4c5-120">Header</span><span class="sxs-lookup"><span data-stu-id="5f4c5-120">Header</span></span><br/> | <dl> <span data-ttu-id="5f4c5-121"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f4c5-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f4c5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f4c5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f4c5-123">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="5f4c5-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




