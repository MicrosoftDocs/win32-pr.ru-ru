---
title: Перечисление DRM_INDIVIDUALIZATION_STATUS (Вмдрмсдк. h)
description: '\_Тип перечисления для индивидуальной защиты DRM \_ определяет допустимые состояния для индивидуальной защиты DRM. | Перечисление DRM_INDIVIDUALIZATION_STATUS (Вмдрмсдк. h)'
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- Формат Windows Media DRM_INDIVIDUALIZATION_STATUS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669163"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="7a2c3-106">Перечисление DRM_INDIVIDUALIZATION_STATUS (Вмдрмсдк. h)</span><span class="sxs-lookup"><span data-stu-id="7a2c3-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="7a2c3-107">Тип перечисления для **\_ индивидуальной защиты DRM \_** определяет допустимые состояния для индивидуальной защиты DRM.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM individualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2c3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a2c3-108">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="7a2c3-109">Константы</span><span class="sxs-lookup"><span data-stu-id="7a2c3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7a2c3-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**столбец indid не \_ определен**</span><span class="sxs-lookup"><span data-stu-id="7a2c3-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="7a2c3-111">Это значение зарезервировано для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-111">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c3-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**\_Начало indid**</span><span class="sxs-lookup"><span data-stu-id="7a2c3-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="7a2c3-113">Указывает начало процесса индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-113">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c3-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**столбец indid \_ выполнен**</span><span class="sxs-lookup"><span data-stu-id="7a2c3-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="7a2c3-115">Указывает, что процесс индивидуализации завершен.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-115">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c3-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**\_Ошибка indid**</span><span class="sxs-lookup"><span data-stu-id="7a2c3-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="7a2c3-117">Указывает, что процесс индивидуализации завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-117">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c3-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**\_Отмена indid**</span><span class="sxs-lookup"><span data-stu-id="7a2c3-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="7a2c3-119">Указывает, что процесс индивидуализации был отменен приложением.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-119">Indicates that the individualization process was canceled by the application.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c3-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**\_скачивание indid**</span><span class="sxs-lookup"><span data-stu-id="7a2c3-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="7a2c3-121">Указывает, что загружается обновление безопасности.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-121">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c3-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**\_Установка indid**</span><span class="sxs-lookup"><span data-stu-id="7a2c3-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="7a2c3-123">Указывает, что устанавливается обновление системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-123">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a2c3-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a2c3-124">Remarks</span></span>

<span data-ttu-id="7a2c3-125">Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](drmwm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="7a2c3-125">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a2c3-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7a2c3-126">Requirements</span></span>



| <span data-ttu-id="7a2c3-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7a2c3-127">Requirement</span></span> | <span data-ttu-id="7a2c3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7a2c3-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2c3-129">Header</span><span class="sxs-lookup"><span data-stu-id="7a2c3-129">Header</span></span><br/> | <dl> <span data-ttu-id="7a2c3-130"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a2c3-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a2c3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a2c3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2c3-132">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="7a2c3-132">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





