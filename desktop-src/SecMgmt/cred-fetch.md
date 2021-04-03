---
description: Определяет значения, определяющие способ получения учетных данных групповой управляемой учетной записи службы (gMSA).
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: Перечисление CRED_FETCH (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999018"
---
# <a name="cred_fetch-enumeration"></a><span data-ttu-id="5577a-103">\_Перечисление выборки для CRED</span><span class="sxs-lookup"><span data-stu-id="5577a-103">CRED\_FETCH enumeration</span></span>

<span data-ttu-id="5577a-104">Определяет значения, определяющие способ получения учетных данных групповой управляемой учетной записи службы (gMSA).</span><span class="sxs-lookup"><span data-stu-id="5577a-104">Defines values that determine how to fetch the credential of a Group Managed Service Account (gMSA).</span></span>

## <a name="syntax"></a><span data-ttu-id="5577a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5577a-105">Syntax</span></span>


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a><span data-ttu-id="5577a-106">Константы</span><span class="sxs-lookup"><span data-stu-id="5577a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5577a-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**кредфетчдефаулт**</span><span class="sxs-lookup"><span data-stu-id="5577a-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span></span>
</dt> <dd>

<span data-ttu-id="5577a-108">Означает, что операционная система должна сначала попытаться получить пароль из локального кэша.</span><span class="sxs-lookup"><span data-stu-id="5577a-108">Signifies that the operating system should first attempt to retrieve the password from the local cache.</span></span> <span data-ttu-id="5577a-109">Если время получения пароля истекло, операционная система должна связаться с контроллером домена для ввода пароля.</span><span class="sxs-lookup"><span data-stu-id="5577a-109">If it is time to fetch the password, then the operating system should contact a domain controller for the password.</span></span> <span data-ttu-id="5577a-110">Если это не удается, возвращайте все кэшированные пароли со значением status Success.</span><span class="sxs-lookup"><span data-stu-id="5577a-110">If that fails, then return any cached passwords with the status value of success.</span></span>

</dd> <dt>

<span data-ttu-id="5577a-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**кредфетчдпапи**</span><span class="sxs-lookup"><span data-stu-id="5577a-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span></span>
</dt> <dd>

<span data-ttu-id="5577a-112">Возвращает учетные данные локальной DPAPI для вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="5577a-112">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="5577a-113">[*Поставщики поддержки безопасности*](/windows/desktop/SecGloss/s-gly) (SSP) обычно не требуют использования этого перечисления.</span><span class="sxs-lookup"><span data-stu-id="5577a-113">[*Security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs) generally would not require the use of this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="5577a-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**кредфетчфорцед**</span><span class="sxs-lookup"><span data-stu-id="5577a-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span></span>
</dt> <dd>

<span data-ttu-id="5577a-115">Заставляет операционную систему попытаться прочитать пароль из контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="5577a-115">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="5577a-116">В течение времени смены пароля пароль, возможно, изменился на контроллере домена и на других узлах-членах, но узел участника gMSA распознает пароль так, как если бы он был действителен.</span><span class="sxs-lookup"><span data-stu-id="5577a-116">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="5577a-117">Это может произойти из-за проблем с отклонением часов между разными контроллерами домена.</span><span class="sxs-lookup"><span data-stu-id="5577a-117">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="5577a-118">Если указано это значение, операционная система определяет, возможно ли изменение пароля из-за неравномерного смещения часов, и, если да, получает пароль.</span><span class="sxs-lookup"><span data-stu-id="5577a-118">When this value is specified, the operating system determines if there could be a possible password change due to clock skew, and if so, retrieves the password.</span></span> <span data-ttu-id="5577a-119">В противном случае возвращаются кэшированные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="5577a-119">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="5577a-120">Если кэшированные учетные данные отсутствуют, операционная система пытается получить его из контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="5577a-120">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5577a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5577a-121">Requirements</span></span>



| <span data-ttu-id="5577a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5577a-122">Requirement</span></span> | <span data-ttu-id="5577a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5577a-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5577a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5577a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5577a-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5577a-125">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5577a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5577a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5577a-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5577a-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5577a-128">Header</span><span class="sxs-lookup"><span data-stu-id="5577a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5577a-129"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5577a-129"><dt>Secpkg.h</dt></span></span> </dl> |



 

