---
title: Константы WINBIO_BIOMETRIC_SENSOR_SUBTYPE (Винбио \_ types. h)
description: Укажите битовую маску для возможностей встроенного датчика.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415253"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a><span data-ttu-id="b1e83-103">\_ \_ Константы подтипа биометрического датчика винбио \_</span><span class="sxs-lookup"><span data-stu-id="b1e83-103">WINBIO\_BIOMETRIC\_SENSOR\_SUBTYPE Constants</span></span>

<span data-ttu-id="b1e83-104">Следующие константы можно использовать в качестве битовой маски для параметра *capabilities* структуры [**\_ \_ схемы единицы винбио**](winbio-unit-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="b1e83-104">The following constants can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="b1e83-105">Они относятся к возможностям встроенного датчика.</span><span class="sxs-lookup"><span data-stu-id="b1e83-105">These refer to the onboard sensor capabilities.</span></span>



| <span data-ttu-id="b1e83-106">Константа</span><span class="sxs-lookup"><span data-stu-id="b1e83-106">Constant</span></span>                                                                                                                                                                                                            | <span data-ttu-id="b1e83-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b1e83-107">Description</span></span>                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <span data-ttu-id="b1e83-108"><dt>**\_неизвестный \_ ПОДТИП датчика \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="b1e83-108"><dt>**WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN**</dt></span></span> </dl>     | <span data-ttu-id="b1e83-109">Неизвестные подтипы датчика.</span><span class="sxs-lookup"><span data-stu-id="b1e83-109">The sensor sub types is not known.</span></span><br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <span data-ttu-id="b1e83-110"><dt>**\_ \_ \_ считывание подтипа датчика винбио FP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b1e83-110"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE**</dt></span></span> </dl> | <span data-ttu-id="b1e83-111">Датчик поддерживает прокрутку отпечатков пальцев.</span><span class="sxs-lookup"><span data-stu-id="b1e83-111">The sensor supports fingerprint swipes.</span></span><br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <span data-ttu-id="b1e83-112"><dt>**\_ \_ \_ касание подтипа датчика FP винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b1e83-112"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH**</dt></span></span> </dl> | <span data-ttu-id="b1e83-113">Датчик поддерживает касание пальцами.</span><span class="sxs-lookup"><span data-stu-id="b1e83-113">The sensor supports finger touches.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="b1e83-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b1e83-114">Requirements</span></span>



| <span data-ttu-id="b1e83-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b1e83-115">Requirement</span></span> | <span data-ttu-id="b1e83-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b1e83-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e83-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1e83-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e83-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b1e83-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="b1e83-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1e83-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e83-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1e83-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b1e83-121">Header</span><span class="sxs-lookup"><span data-stu-id="b1e83-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1e83-122"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1e83-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1e83-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1e83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e83-124">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="b1e83-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="b1e83-125">**\_схема единицы \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="b1e83-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





