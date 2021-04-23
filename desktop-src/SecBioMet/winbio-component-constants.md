---
title: Константы WINBIO_COMPONENT (Винбио \_ types. h)
description: Укажите тип используемого адаптера.
ms.assetid: f920788b-2175-4c01-81b5-e7b49111a7ac
topic_type:
- apiref
api_name:
- WINBIO_COMPONENT_SENSOR
- WINBIO_COMPONENT_ENGINE
- WINBIO_COMPONENT_STORAGE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07afe4fac08632133d4fa755717d83475b78c675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415121"
---
# <a name="winbio_component-constants"></a><span data-ttu-id="30b9c-103">\_Константы компонента винбио</span><span class="sxs-lookup"><span data-stu-id="30b9c-103">WINBIO\_COMPONENT Constants</span></span>

<span data-ttu-id="30b9c-104">При вызове [**винбиоконтролунит**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit) или [**винбиоконтролунитпривилежед**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged) можно использовать следующие константы для указания типа используемого адаптера.</span><span class="sxs-lookup"><span data-stu-id="30b9c-104">The following constants can be used when calling [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit) or [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged) to specify the type of adapter being used.</span></span>



| <span data-ttu-id="30b9c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="30b9c-105">Constant</span></span>                                                                                                                                                                                        | <span data-ttu-id="30b9c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="30b9c-106">Description</span></span>                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="WINBIO_COMPONENT_SENSOR"></span><span id="winbio_component_sensor"></span><dl> <span data-ttu-id="30b9c-107"><dt>**\_датчик компонента \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="30b9c-107"><dt>**WINBIO\_COMPONENT\_SENSOR**</dt></span></span> </dl>    | <span data-ttu-id="30b9c-108">Указывает адаптер датчика.</span><span class="sxs-lookup"><span data-stu-id="30b9c-108">Specifies a sensor adapter.</span></span><br/>  |
| <span id="WINBIO_COMPONENT_ENGINE"></span><span id="winbio_component_engine"></span><dl> <span data-ttu-id="30b9c-109"><dt>**\_подсистема компонентов винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="30b9c-109"><dt>**WINBIO\_COMPONENT\_ENGINE**</dt></span></span> </dl>    | <span data-ttu-id="30b9c-110">Указывает адаптер подсистемы.</span><span class="sxs-lookup"><span data-stu-id="30b9c-110">Specifies an engine adapter.</span></span><br/> |
| <span id="WINBIO_COMPONENT_STORAGE"></span><span id="winbio_component_storage"></span><dl> <span data-ttu-id="30b9c-111"><dt>**\_хранилище компонентов \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="30b9c-111"><dt>**WINBIO\_COMPONENT\_STORAGE**</dt></span></span> </dl> | <span data-ttu-id="30b9c-112">Указывает адаптер хранилища.</span><span class="sxs-lookup"><span data-stu-id="30b9c-112">Specifies a storage adapter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="30b9c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="30b9c-113">Requirements</span></span>



| <span data-ttu-id="30b9c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="30b9c-114">Requirement</span></span> | <span data-ttu-id="30b9c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="30b9c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b9c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30b9c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="30b9c-117">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="30b9c-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="30b9c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30b9c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="30b9c-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="30b9c-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="30b9c-120">Header</span><span class="sxs-lookup"><span data-stu-id="30b9c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b9c-121"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30b9c-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b9c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30b9c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b9c-123">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="30b9c-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





