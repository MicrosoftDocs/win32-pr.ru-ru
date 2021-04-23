---
title: Перечисление WINBIO_CREDENTIAL_STATE (Винбио \_ types. h)
description: Определяет значения, указывающие, связаны ли учетные данные с биометрических данных конечного пользователя.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- API биометрическая платформа Windows перечисления WINBIO_CREDENTIAL_STATE
- API биометрическая платформа Windows указателя перечисления PWINBIO_CREDENTIAL_STATE
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340425"
---
# <a name="winbio_credential_state-enumeration"></a><span data-ttu-id="5a1c8-105">\_Перечисление состояния учетных данных винбио \_</span><span class="sxs-lookup"><span data-stu-id="5a1c8-105">WINBIO\_CREDENTIAL\_STATE enumeration</span></span>

<span data-ttu-id="5a1c8-106">Определяет значения, указывающие, связаны ли учетные данные с биометрических данных конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5a1c8-106">Defines values that specify whether a credential has been associated with the biometric data for an end user.</span></span> <span data-ttu-id="5a1c8-107">Это перечисление используется функцией [**винбиожеткредентиалстате**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .</span><span class="sxs-lookup"><span data-stu-id="5a1c8-107">This enumeration is used by the [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a1c8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a1c8-108">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a><span data-ttu-id="5a1c8-109">Константы</span><span class="sxs-lookup"><span data-stu-id="5a1c8-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5a1c8-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_учетные данные винбио \_ не \_ заданы**</span><span class="sxs-lookup"><span data-stu-id="5a1c8-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**WINBIO\_CREDENTIAL\_NOT\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="5a1c8-111">Учетные данные были связаны с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5a1c8-111">A credential has been associated with the end user.</span></span>

</dd> <dt>

<span data-ttu-id="5a1c8-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**\_набор учетных данных винбио \_**</span><span class="sxs-lookup"><span data-stu-id="5a1c8-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**WINBIO\_CREDENTIAL\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="5a1c8-113">Учетные данные не связаны с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5a1c8-113">A credential has not been associated with the end user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a1c8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5a1c8-114">Requirements</span></span>



| <span data-ttu-id="5a1c8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5a1c8-115">Requirement</span></span> | <span data-ttu-id="5a1c8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5a1c8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1c8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a1c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1c8-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5a1c8-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="5a1c8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a1c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1c8-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a1c8-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5a1c8-121">Header</span><span class="sxs-lookup"><span data-stu-id="5a1c8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a1c8-122"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a1c8-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a1c8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a1c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1c8-124">Перечисления клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="5a1c8-124">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="5a1c8-125">**винбиожеткредентиалстате**</span><span class="sxs-lookup"><span data-stu-id="5a1c8-125">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





