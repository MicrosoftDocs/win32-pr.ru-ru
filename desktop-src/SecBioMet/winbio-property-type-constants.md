---
title: Константы WINBIO_PROPERTY_TYPE (Винбио. h)
description: Укажите источник сведений о свойстве в функции Винбиожетпроперти.
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4a1420af18bfa4d2ba5d0457b22cd5f77e7b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493143"
---
# <a name="winbio_property_type-constants"></a><span data-ttu-id="00174-103">\_ \_ Константы типа свойства винбио</span><span class="sxs-lookup"><span data-stu-id="00174-103">WINBIO\_PROPERTY\_TYPE Constants</span></span>

<span data-ttu-id="00174-104">Следующие константы **\_ \_ типа свойства винбио** можно использовать для указания источника сведений о свойстве в функции [**винбиожетпроперти**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) .</span><span class="sxs-lookup"><span data-stu-id="00174-104">The following **WINBIO\_PROPERTY\_TYPE** constants can be used to specify the source of the property information in the [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) function.</span></span>

<dl> <dt>

<span data-ttu-id="00174-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**\_ \_ сеанс типа свойства \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="00174-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**WINBIO\_PROPERTY\_TYPE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00174-106">Свойство применяется к определенному сеансу биометрической метрики.</span><span class="sxs-lookup"><span data-stu-id="00174-106">The property applies to a specific biometric session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00174-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**\_ \_ шаблон типа свойства \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="00174-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**WINBIO\_PROPERTY\_TYPE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00174-108">Свойство применяется к определенному биометрической шаблону.</span><span class="sxs-lookup"><span data-stu-id="00174-108">The property applies to a specific biometric template.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00174-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**\_ \_ единица типа свойства винбио \_**</span><span class="sxs-lookup"><span data-stu-id="00174-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**WINBIO\_PROPERTY\_TYPE\_UNIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00174-110">Свойство применяется к определенной биометрической единице.</span><span class="sxs-lookup"><span data-stu-id="00174-110">The property applies to a specific biometric unit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00174-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**\_ \_ \_ учетная запись типа свойства винбио**</span><span class="sxs-lookup"><span data-stu-id="00174-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**WINBIO\_PROPERTY\_TYPE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00174-112">Свойство применяется к определенной учетной записи пользователя с биометрической регистрацией.</span><span class="sxs-lookup"><span data-stu-id="00174-112">The property applies to a specific user account that has a biometric enrollment.</span></span> <span data-ttu-id="00174-113">Это значение поддерживается начиная с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="00174-113">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00174-114">Требования</span><span class="sxs-lookup"><span data-stu-id="00174-114">Requirements</span></span>



| <span data-ttu-id="00174-115">Требование</span><span class="sxs-lookup"><span data-stu-id="00174-115">Requirement</span></span> | <span data-ttu-id="00174-116">Значение</span><span class="sxs-lookup"><span data-stu-id="00174-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00174-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00174-117">Minimum supported client</span></span><br/> | <span data-ttu-id="00174-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="00174-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="00174-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00174-119">Minimum supported server</span></span><br/> | <span data-ttu-id="00174-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="00174-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="00174-121">Header</span><span class="sxs-lookup"><span data-stu-id="00174-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="00174-122"><dt>Винбио. h (включение Винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00174-122"><dt>Winbio.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00174-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00174-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00174-124">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="00174-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="00174-125">**винбиожетпроперти**</span><span class="sxs-lookup"><span data-stu-id="00174-125">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 





