---
title: Перечисление WINBIO_CREDENTIAL_TYPE (Винбио \_ types. h)
description: Определяет флаги, которые можно использовать для фильтрации по типу учетных данных.
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- API биометрическая платформа Windows перечисления WINBIO_CREDENTIAL_TYPE
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_TYPE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae41693db264308d33bc30191bdb73007b6b2dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892673"
---
# <a name="winbio_credential_type-enumeration"></a><span data-ttu-id="59f20-104">\_Перечисление типов учетных данных винбио \_</span><span class="sxs-lookup"><span data-stu-id="59f20-104">WINBIO\_CREDENTIAL\_TYPE enumeration</span></span>

<span data-ttu-id="59f20-105">Определяет флаги, которые можно использовать для фильтрации по типу учетных данных.</span><span class="sxs-lookup"><span data-stu-id="59f20-105">Defines flags that can be used to filter on the credential type.</span></span> <span data-ttu-id="59f20-106">Это перечисление используется функциями [**винбиосеткредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**винбиоремовекредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)и [**винбиожеткредентиалстате**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .</span><span class="sxs-lookup"><span data-stu-id="59f20-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential), and [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f20-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59f20-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a><span data-ttu-id="59f20-108">Константы</span><span class="sxs-lookup"><span data-stu-id="59f20-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="59f20-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**\_пароль учетных данных винбио \_**</span><span class="sxs-lookup"><span data-stu-id="59f20-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**WINBIO\_CREDENTIAL\_PASSWORD**</span></span>
</dt> <dd>

<span data-ttu-id="59f20-110">Фильтрует учетные данные пароля.</span><span class="sxs-lookup"><span data-stu-id="59f20-110">Filters password credentials.</span></span>

</dd> <dt>

<span data-ttu-id="59f20-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**ВИНБИО \_ учетные данные \_**</span><span class="sxs-lookup"><span data-stu-id="59f20-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO\_CREDENTIAL\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="59f20-112">Фильтрует все учетные данные.</span><span class="sxs-lookup"><span data-stu-id="59f20-112">Filters all credentials.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59f20-113">Требования</span><span class="sxs-lookup"><span data-stu-id="59f20-113">Requirements</span></span>



| <span data-ttu-id="59f20-114">Требование</span><span class="sxs-lookup"><span data-stu-id="59f20-114">Requirement</span></span> | <span data-ttu-id="59f20-115">Значение</span><span class="sxs-lookup"><span data-stu-id="59f20-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f20-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59f20-116">Minimum supported client</span></span><br/> | <span data-ttu-id="59f20-117">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="59f20-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="59f20-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59f20-118">Minimum supported server</span></span><br/> | <span data-ttu-id="59f20-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="59f20-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="59f20-120">Header</span><span class="sxs-lookup"><span data-stu-id="59f20-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="59f20-121"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59f20-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59f20-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59f20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f20-123">Перечисления клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="59f20-123">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="59f20-124">**винбиожеткредентиалстате**</span><span class="sxs-lookup"><span data-stu-id="59f20-124">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> <dt>

[<span data-ttu-id="59f20-125">**винбиоремовекредентиал**</span><span class="sxs-lookup"><span data-stu-id="59f20-125">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[<span data-ttu-id="59f20-126">**винбиосеткредентиал**</span><span class="sxs-lookup"><span data-stu-id="59f20-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 





