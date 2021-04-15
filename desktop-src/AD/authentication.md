---
title: Проверка подлинности (AD DS)
description: Каждый объект в домен Active Directory Services имеет уникальный дескриптор безопасности, определяющий разрешения на доступ, необходимые для чтения или обновления объекта или его отдельных свойств.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, привязка, проверка подлинности
- Привязка AD для проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487512"
---
# <a name="authentication-ad-ds"></a><span data-ttu-id="ed65a-105">Проверка подлинности (AD DS)</span><span class="sxs-lookup"><span data-stu-id="ed65a-105">Authentication (AD DS)</span></span>

<span data-ttu-id="ed65a-106">Каждый объект в домен Active Directory Services имеет уникальный дескриптор безопасности, определяющий разрешения на доступ, необходимые для чтения или обновления объекта или его отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="ed65a-106">Every object in Active Directory Domain Services has a unique security descriptor that defines the access permissions that are required to read or update the object or its individual properties.</span></span> <span data-ttu-id="ed65a-107">Права доступа определяются правами, предоставленными учетной записи пользователя или членству в группе.</span><span class="sxs-lookup"><span data-stu-id="ed65a-107">Access privileges are determined by the rights granted to a user's account or group memberships.</span></span>

<span data-ttu-id="ed65a-108">Когда приложение привязывается к объекту в каталоге, права доступа, которые приложение имеет к этому объекту, основаны на пользовательском контексте, указанном во время операции привязки.</span><span class="sxs-lookup"><span data-stu-id="ed65a-108">When an application binds to an object in the directory, the access privileges that the application has to that object are based on the user context specified during the bind operation.</span></span> <span data-ttu-id="ed65a-109">Для функций привязки и методов [**адсжетобжект**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**иадсопендсобжект:: опендсобжект**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject)приложение может неявно использовать учетные данные вызывающей стороны, явно указывать учетные данные учетной записи пользователя или использовать пользовательский контекст без проверки подлинности (Guest).</span><span class="sxs-lookup"><span data-stu-id="ed65a-109">For the binding functions and methods [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), an application can implicitly use the credentials of the caller, explicitly specify the credentials of a user account, or use an unauthenticated user context (Guest).</span></span>

 

 