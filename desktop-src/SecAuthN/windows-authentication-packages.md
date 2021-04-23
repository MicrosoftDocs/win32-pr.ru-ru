---
description: Пакеты проверки подлинности Windows предоставляют службы проверки подлинности путем реализации функциональных возможностей пакета для функций Лсалогонусер и LsaCallAuthenticationPackage, предоставляемых LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Пакеты проверки подлинности Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541151"
---
# <a name="windows-authentication-packages"></a><span data-ttu-id="4c002-103">Пакеты проверки подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="4c002-103">Windows Authentication Packages</span></span>

<span data-ttu-id="4c002-104">Пакеты проверки подлинности Windows предоставляют службы проверки подлинности путем реализации функциональных возможностей пакета для функций [**лсалогонусер**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) и [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) , предоставляемых LSA.</span><span class="sxs-lookup"><span data-stu-id="4c002-104">Windows authentication packages provide authentication services by implementing package-specific functionality for the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) and [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) functions provided by the LSA.</span></span>

<span data-ttu-id="4c002-105">MSV1 \_ 0 является примером [*пакета проверки подлинности*](../secgloss/a-gly.md)Windows.</span><span class="sxs-lookup"><span data-stu-id="4c002-105">MSV1\_0 is an example of a Windows [*authentication package*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="4c002-106">Пакет MSV1 \_ 0 принимает имя пользователя и [*хэшированный*](../secgloss/h-gly.md) пароль, который выполняется в базе данных [*диспетчера учетных записей безопасности*](../secgloss/s-gly.md) (SAM).</span><span class="sxs-lookup"><span data-stu-id="4c002-106">The MSV1\_0 package accepts a user name and a [*hashed*](../secgloss/h-gly.md) password, which it looks up in the [*Security Accounts Manager*](../secgloss/s-gly.md) (SAM) database.</span></span> <span data-ttu-id="4c002-107">В зависимости от результатов поиска \_ пакет проверки подлинности MSV1 0 принимает или отклоняет попытки проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4c002-107">Depending on the results of the lookup, the MSV1\_0 authentication package accepts or rejects the authentication attempt.</span></span>

<span data-ttu-id="4c002-108">Список функций поддержки, предоставляемых LSA для использования пакетами проверки подлинности Windows, которые нуждаются в системных службах, см. в разделе [функции LSA, вызываемые пакетами проверки подлинности](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4c002-108">For a list of the support functions the LSA provides for use by Windows authentication packages that require system services, see [LSA Functions Called by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="4c002-109">Пакеты проверки подлинности Windows должны реализовывать набор функций, которые вызываются LSA.</span><span class="sxs-lookup"><span data-stu-id="4c002-109">Windows authentication packages must implement a set of functions that are called by the LSA.</span></span> <span data-ttu-id="4c002-110">Полный список функций см. в разделе [функции, реализованные пакетами проверки подлинности](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4c002-110">For the complete list of functions, see [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

 

 
