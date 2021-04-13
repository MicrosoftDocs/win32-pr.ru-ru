---
title: Константы WINBIO_POOL (Винбио \_ types. h)
description: Укажите тип пула биометрических единиц, который будет использоваться в сеансе.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535411"
---
# <a name="winbio_pool-constants"></a><span data-ttu-id="eff6f-103">\_Константы пула винбио</span><span class="sxs-lookup"><span data-stu-id="eff6f-103">WINBIO\_POOL Constants</span></span>

<span data-ttu-id="eff6f-104">Следующие константы можно использовать в функции [**винбиупенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) для указания типа пула биометрических единиц, который будет использоваться в сеансе.</span><span class="sxs-lookup"><span data-stu-id="eff6f-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify the type of biometric unit pool to be used in the session.</span></span>



| <span data-ttu-id="eff6f-105">Константа</span><span class="sxs-lookup"><span data-stu-id="eff6f-105">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="eff6f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="eff6f-106">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="eff6f-107"><dt>**\_неизвестный пул винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eff6f-107"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="eff6f-108">Неизвестный тип пула.</span><span class="sxs-lookup"><span data-stu-id="eff6f-108">The pool type is unknown.</span></span><br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="eff6f-109"><dt>**\_система пула \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="eff6f-109"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>             | <span data-ttu-id="eff6f-110">Указывает общую коллекцию биометрических модулей, управляемых поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="eff6f-110">Specifies a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="eff6f-111"><dt>**\_частный пул \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="eff6f-111"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl>          | <span data-ttu-id="eff6f-112">Указывает коллекцию биометрических единиц, управляемых вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="eff6f-112">Specifies a collection of biometric units that are managed by the caller.</span></span><br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <span data-ttu-id="eff6f-113"><dt>**пул ВИНБИО не \_ \_ назначен**</dt></span><span class="sxs-lookup"><span data-stu-id="eff6f-113"><dt>**WINBIO\_POOL\_UNASSIGNED**</dt></span></span> </dl> | <span data-ttu-id="eff6f-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="eff6f-114">Reserved.</span></span><br/>                                                                         |



## <a name="requirements"></a><span data-ttu-id="eff6f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="eff6f-115">Requirements</span></span>



| <span data-ttu-id="eff6f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="eff6f-116">Requirement</span></span> | <span data-ttu-id="eff6f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eff6f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eff6f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eff6f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eff6f-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eff6f-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="eff6f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eff6f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eff6f-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eff6f-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="eff6f-122">Header</span><span class="sxs-lookup"><span data-stu-id="eff6f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eff6f-123"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eff6f-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eff6f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eff6f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eff6f-125">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="eff6f-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





