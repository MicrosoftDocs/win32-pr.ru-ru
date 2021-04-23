---
title: Перечисление WINBIO_CREDENTIAL_FORMAT (Винбио \_ types. h)
description: Определяет флаги, которые можно использовать для указания формата учетных данных конечного пользователя.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- API биометрическая платформа Windows перечисления WINBIO_CREDENTIAL_FORMAT
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135910"
---
# <a name="winbio_credential_format-enumeration"></a><span data-ttu-id="96986-104">\_Перечисление форматов учетных данных винбио \_</span><span class="sxs-lookup"><span data-stu-id="96986-104">WINBIO\_CREDENTIAL\_FORMAT enumeration</span></span>

<span data-ttu-id="96986-105">Определяет флаги, которые можно использовать для указания формата учетных данных конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="96986-105">Defines flags that can be used to specify the end-user credential format.</span></span> <span data-ttu-id="96986-106">Это перечисление используется функцией [**винбиосеткредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) .</span><span class="sxs-lookup"><span data-stu-id="96986-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="96986-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96986-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="96986-108">Константы</span><span class="sxs-lookup"><span data-stu-id="96986-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="96986-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**\_универсальный пароль \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="96986-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO\_PASSWORD\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="96986-110">Пароль имеет общий формат.</span><span class="sxs-lookup"><span data-stu-id="96986-110">The password is in a generic format.</span></span>

</dd> <dt>

<span data-ttu-id="96986-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**ВИНБИО \_ пароль \_**</span><span class="sxs-lookup"><span data-stu-id="96986-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO\_PASSWORD\_PACKED**</span></span>
</dt> <dd>

<span data-ttu-id="96986-112">Пароль имеет сжатый формат.</span><span class="sxs-lookup"><span data-stu-id="96986-112">The password is in a compressed format.</span></span>

</dd> <dt>

<span data-ttu-id="96986-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**\_защищен паролем винбио \_**</span><span class="sxs-lookup"><span data-stu-id="96986-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO\_PASSWORD\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="96986-114">Учетные данные пароля были заключены в оболочку с помощью [**кредпротект**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span><span class="sxs-lookup"><span data-stu-id="96986-114">The password credential was wrapped with [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96986-115">Требования</span><span class="sxs-lookup"><span data-stu-id="96986-115">Requirements</span></span>



| <span data-ttu-id="96986-116">Требование</span><span class="sxs-lookup"><span data-stu-id="96986-116">Requirement</span></span> | <span data-ttu-id="96986-117">Значение</span><span class="sxs-lookup"><span data-stu-id="96986-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96986-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96986-118">Minimum supported client</span></span><br/> | <span data-ttu-id="96986-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96986-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="96986-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96986-120">Minimum supported server</span></span><br/> | <span data-ttu-id="96986-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="96986-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="96986-122">Header</span><span class="sxs-lookup"><span data-stu-id="96986-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="96986-123"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96986-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96986-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96986-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96986-125">Перечисления клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="96986-125">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="96986-126">**винбиосеткредентиал**</span><span class="sxs-lookup"><span data-stu-id="96986-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

