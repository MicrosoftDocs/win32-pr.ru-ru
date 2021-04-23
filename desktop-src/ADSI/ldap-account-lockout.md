---
title: Блокировка учетной записи (поставщик LDAP)
description: При превышении числа неудачных попыток входа учетная запись пользователя блокируется в течение периода времени, заданного атрибутом Локкаутдуратион.
ms.assetid: bf86f6ac-8209-4306-8736-99ce53c93617
ms.tgt_platform: multiple
keywords:
- Блокировка учетной записи (поставщик LDAP) ADSI
- Блокировка учетной записи ADSI, поставщик LDAP
- ADSI поставщика LDAP, примеры управления пользователями, блокировка учетной записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b7a25943debfd08469ce9a28463c88159ded9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654367"
---
# <a name="account-lockout-ldap-provider"></a><span data-ttu-id="10dc0-106">Блокировка учетной записи (поставщик LDAP)</span><span class="sxs-lookup"><span data-stu-id="10dc0-106">Account Lockout (LDAP Provider)</span></span>

<span data-ttu-id="10dc0-107">При превышении числа неудачных попыток входа учетная запись пользователя блокируется в течение периода времени, заданного атрибутом [**локкаутдуратион**](/windows/desktop/ADSchema/a-lockoutduration) .</span><span class="sxs-lookup"><span data-stu-id="10dc0-107">When the number of failed logon attempts is exceeded, the user account is locked out for a time period specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="10dc0-108">Свойство [**IADsUser. исаккаунтлоккед**](iadsuser-property-methods.md) является свойством, используемым для чтения и изменения состояния блокировки учетной записи пользователя, но поставщик LDAP ADSI не поддерживает точно поддерживаемое свойство **исаккаунтлоккед** .</span><span class="sxs-lookup"><span data-stu-id="10dc0-108">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the LDAP ADSI provider does not accurately support the **IsAccountLocked** property.</span></span> <span data-ttu-id="10dc0-109">Чтобы получить и задать точные данные блокировки учетной записи, используйте поставщик WinNT.</span><span class="sxs-lookup"><span data-stu-id="10dc0-109">To obtain and set accurate account lockout data, use the WinNT provider.</span></span> <span data-ttu-id="10dc0-110">Дополнительные сведения об использовании свойства **исаккаунтлоккед** с поставщиком WinNT см. в разделе [Блокировка учетной записи (поставщик WinNT)](winnt-account-lockout.md).</span><span class="sxs-lookup"><span data-stu-id="10dc0-110">For more information about using the **IsAccountLocked** property with the WinNT provider, see [Account Lockout (WinNT Provider)](winnt-account-lockout.md).</span></span>

 

 