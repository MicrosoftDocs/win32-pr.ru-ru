---
title: Credential Guard и сторонние приложения
description: Credential Guard не позволяет сторонним поставщикам общих служб запрашивать хэш-коды паролей из LSA.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a036ba5db5b86ab7c186b25e4d858b1badc60bd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487732"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a><span data-ttu-id="5b622-103">Сторонние поставщики поддержки безопасности с Credential Guard</span><span class="sxs-lookup"><span data-stu-id="5b622-103">Third party Security Support Providers with Credential Guard</span></span>

<span data-ttu-id="5b622-104">Credential Guard не позволяет сторонним поставщикам общих служб запрашивать хэш-коды паролей из LSA.</span><span class="sxs-lookup"><span data-stu-id="5b622-104">Credential Guard does not allow 3rd party SSPs to ask for password hashes from LSA.</span></span> <span data-ttu-id="5b622-105">При этом SSP и AP все равно получают уведомление о пароле, когда пользователь входит в систему или меняет пароль.</span><span class="sxs-lookup"><span data-stu-id="5b622-105">However, SSPs and APs still get notified of the password when a user logs on and/or changes their password.</span></span> <span data-ttu-id="5b622-106">Никакое использование недокументированных API с другими поставщиками общих служб и AP не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5b622-106">Any use of undocumented APIs within custom SSPs and APs are not supported.</span></span>

<span data-ttu-id="5b622-107">По мере увеличения масштабов защиты, осуществляемой Credential Guard, последующие выпуски Windows 10 с работающим Credential Guard могут повлиять на сценарии, которые работали в прошлом.</span><span class="sxs-lookup"><span data-stu-id="5b622-107">As the depth and breadth of protections provided by Credential Guard are increased, subsequent releases of Windows 10 with Credential Guard running may impact scenarios that were working in the past.</span></span> <span data-ttu-id="5b622-108">Например, Credential Guard может заблокировать использование определенного типа учетных данных или определенного компонента, чтобы не позволить вредоносному ПО воспользоваться уязвимостями.</span><span class="sxs-lookup"><span data-stu-id="5b622-108">For example, Credential Guard may block the use of a particular type of credential or a particular component to prevent malware from taking advantage of vulnerabilities.</span></span> <span data-ttu-id="5b622-109">Поэтому мы рекомендуем проверять сценарии, необходимые для работы организации, перед обновлением устройств с работающим Credential Guard.</span><span class="sxs-lookup"><span data-stu-id="5b622-109">Therefore, we recommend that scenarios required for operations in an organization are tested before upgrading a device that has Credential Guard running.</span></span>

<span data-ttu-id="5b622-110">Полное описание и рекомендуемые способы устранения этой проблемы см. в [этой статье](/windows/security/identity-protection/credential-guard/credential-guard) .</span><span class="sxs-lookup"><span data-stu-id="5b622-110">Please refer to [this article](/windows/security/identity-protection/credential-guard/credential-guard) for the full description and recommended mitigations.</span></span>

 

 