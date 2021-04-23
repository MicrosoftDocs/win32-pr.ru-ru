---
description: Поле типа в записи управления доступом (ACE), которое определяет, является ли ACE записью ACE, которая разрешает доступ или запрещает доступ.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Константы типа ACE пространства имен (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648999"
---
# <a name="namespace-ace-type-constants"></a><span data-ttu-id="f7958-103">Константы типа ACE пространства имен</span><span class="sxs-lookup"><span data-stu-id="f7958-103">Namespace ACE Type Constants</span></span>

<span data-ttu-id="f7958-104">Поле **типа** в записи управления доступом (ACE), которое определяет, является ли ACE записью ACE, которая разрешает доступ или запрещает доступ.</span><span class="sxs-lookup"><span data-stu-id="f7958-104">The **Type** field in an access control entry (ACE) that determines whether the ACE is an ACE that allows access or denies access.</span></span>

<dl> <dt>

<span data-ttu-id="f7958-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Возможность**</span><span class="sxs-lookup"><span data-stu-id="f7958-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7958-106">0</span><span class="sxs-lookup"><span data-stu-id="f7958-106">0</span></span>
</dt> <dt>



<span data-ttu-id="f7958-107">ACE разрешает доступ к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="f7958-107">The ACE allows access to the namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7958-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Deny**</span><span class="sxs-lookup"><span data-stu-id="f7958-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Deny**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7958-109">1</span><span class="sxs-lookup"><span data-stu-id="f7958-109">1</span></span>
</dt> <dt>



<span data-ttu-id="f7958-110">ACE запрещает доступ к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="f7958-110">The ACE denies access to the namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7958-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f7958-111">Requirements</span></span>



| <span data-ttu-id="f7958-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f7958-112">Requirement</span></span> | <span data-ttu-id="f7958-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f7958-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7958-114">Header</span><span class="sxs-lookup"><span data-stu-id="f7958-114">Header</span></span><br/> | <dl> <span data-ttu-id="f7958-115"><dt>Файл Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7958-115"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7958-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7958-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7958-117">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="f7958-117">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="f7958-118">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="f7958-118">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="f7958-119">Установка наследования безопасности пространства имен</span><span class="sxs-lookup"><span data-stu-id="f7958-119">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="f7958-120">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="f7958-120">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




