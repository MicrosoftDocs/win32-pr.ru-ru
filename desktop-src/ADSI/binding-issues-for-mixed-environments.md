---
title: Проблемы привязки для смешанных сред
description: Проблемы привязки для смешанных сред
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, использование, проблемы привязки для смешанных сред
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654347"
---
# <a name="binding-issues-for-mixed-environments"></a><span data-ttu-id="529aa-104">Проблемы привязки для смешанных сред</span><span class="sxs-lookup"><span data-stu-id="529aa-104">Binding Issues for Mixed Environments</span></span>

<span data-ttu-id="529aa-105">Для сред, в которых домен, содержащий Active Directory, имеет отношение доверия с доменом Windows NT 4,0, может возникнуть проблема с использованием привязки без сервера для привязки к Active Directory объектам.</span><span class="sxs-lookup"><span data-stu-id="529aa-105">For environments in which the domain that contains Active Directory has a trust relationship with a Windows NT 4.0 domain, there may be a problem with using serverless binding to bind to Active Directory objects.</span></span>

<span data-ttu-id="529aa-106">В некоторых сетевых средах между контроллерами домена, содержащими Active Directory и серверами Windows NT 4,0, были настроены доверительные отношения с целью разрешения проверки подлинности между доменами.</span><span class="sxs-lookup"><span data-stu-id="529aa-106">In some networking environments, trust relationships have been set up between domain controllers that contain Active Directory and Windows NT 4.0 servers for the purpose of allowing authentication between domains.</span></span> <span data-ttu-id="529aa-107">В этих смешанных средах, если пользователь, являющийся членом Windows NT 4,0, пытается привязать бессерверную привязку к объекту Active Directory в доверенном домене, произойдет сбой привязки и будет возвращена ошибка.</span><span class="sxs-lookup"><span data-stu-id="529aa-107">In these mixed environments, if a user, who is a member of the Windows NT 4.0, domain attempts to use serverless binding to bind to an Active Directory object on a trusted domain, then the bind will fail and an error is returned.</span></span> <span data-ttu-id="529aa-108">Это обусловлено тем, что в бессерверной привязке используется функция [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) для привязки к объекту в Active Directory, который зависит от правильной службы DNS.</span><span class="sxs-lookup"><span data-stu-id="529aa-108">This is because a serverless bind uses the [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) function to bind to the object in Active Directory, which is dependent upon the proper DNS.</span></span>

<span data-ttu-id="529aa-109">В этом сценарии пользователь Windows NT должен указать имя определенного домена для привязки.</span><span class="sxs-lookup"><span data-stu-id="529aa-109">In this scenario, the Windows NT user must provide the name of a specific domain to bind to.</span></span> <span data-ttu-id="529aa-110">Пример.</span><span class="sxs-lookup"><span data-stu-id="529aa-110">The following is an example.</span></span>

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 