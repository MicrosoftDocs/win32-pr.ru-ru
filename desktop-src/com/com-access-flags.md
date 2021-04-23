---
title: Флаги доступа («Accctrl. h)
description: Эти значения указывают, являются ли записи в списке доступа описания разрешенных или запрещенных прав.
ms.assetid: 460d2c72-3315-4b4c-928e-4bb0640acbe5
topic_type:
- apiref
api_name:
- ACTRL_ACCESS_ALLOWED
- ACTRL_ACCESS_DENIED
api_location:
- AccCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5972bf95efc675d6dd9c2e58c0b7d25c8c305371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137659"
---
# <a name="access-flags"></a><span data-ttu-id="0230e-103">Флаги доступа</span><span class="sxs-lookup"><span data-stu-id="0230e-103">Access Flags</span></span>

<span data-ttu-id="0230e-104">Эти значения указывают, являются ли записи в списке доступа описания разрешенных или запрещенных прав.</span><span class="sxs-lookup"><span data-stu-id="0230e-104">These values indicate whether an entry in the access list describes rights that are allowed or denied.</span></span>



| <span data-ttu-id="0230e-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="0230e-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="0230e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0230e-106">Description</span></span>                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="ACTRL_ACCESS_ALLOWED"></span><span id="actrl_access_allowed"></span><dl> <span data-ttu-id="0230e-107"><dt>**Актрл \_ ДОСТУП \_ разрешен**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="0230e-107"><dt>**ACTRL\_ACCESS\_ALLOWED**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="0230e-108">Указывает запись, разрешенную доступом.</span><span class="sxs-lookup"><span data-stu-id="0230e-108">Indicates an access-allowed entry.</span></span><br/> |
| <span id="ACTRL_ACCESS_DENIED"></span><span id="actrl_access_denied"></span><dl> <span data-ttu-id="0230e-109"><dt>**Актрл \_ \_Отказано в доступе**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="0230e-109"><dt>**ACTRL\_ACCESS\_DENIED**</dt> <dt>0x10000000</dt></span></span> </dl>    | <span data-ttu-id="0230e-110">Указывает запись запрета доступа.</span><span class="sxs-lookup"><span data-stu-id="0230e-110">Indicates an access-denied entry.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="0230e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0230e-111">Requirements</span></span>



| <span data-ttu-id="0230e-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0230e-112">Requirement</span></span> | <span data-ttu-id="0230e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0230e-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0230e-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0230e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0230e-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0230e-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0230e-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0230e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0230e-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0230e-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0230e-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0230e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0230e-119"><dt>«Accctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0230e-119"><dt>AccCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0230e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0230e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0230e-121">**\_запись доступа \_ актрл**</span><span class="sxs-lookup"><span data-stu-id="0230e-121">**ACTRL\_ACCESS\_ENTRY**</span></span>](/windows/desktop/api/AccCtrl/ns-accctrl-actrl_access_entrya)
</dt> </dl>

 

 





