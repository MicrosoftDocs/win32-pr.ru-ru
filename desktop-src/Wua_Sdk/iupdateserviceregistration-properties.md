---
description: Интерфейс Иупдатесервицерегистратион определяет следующие свойства.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Свойства Иупдатесервицерегистратион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692150"
---
# <a name="iupdateserviceregistration-properties"></a><span data-ttu-id="cd343-103">Свойства Иупдатесервицерегистратион</span><span class="sxs-lookup"><span data-stu-id="cd343-103">IUpdateServiceRegistration Properties</span></span>

<span data-ttu-id="cd343-104">Интерфейс **иупдатесервицерегистратион** определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cd343-104">The **IUpdateServiceRegistration** interface defines the following properties.</span></span>



| <span data-ttu-id="cd343-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="cd343-105">Property</span></span>                                                                                      | <span data-ttu-id="cd343-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cd343-106">Description</span></span>                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd343-107">**испендингрегистратионвисау**</span><span class="sxs-lookup"><span data-stu-id="cd343-107">**IsPendingRegistrationWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | <span data-ttu-id="cd343-108">Возвращает логическое значение, указывающее, будет ли служба также зарегистрирована в автоматическое обновление при добавлении.</span><span class="sxs-lookup"><span data-stu-id="cd343-108">Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added.</span></span>                                  |
| [<span data-ttu-id="cd343-109">**RegistrationState**</span><span class="sxs-lookup"><span data-stu-id="cd343-109">**RegistrationState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | <span data-ttu-id="cd343-110">Возвращает значение [**упдатесервицерегистратионстате**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) , указывающее текущее состояние регистрации службы.</span><span class="sxs-lookup"><span data-stu-id="cd343-110">Gets an [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) value that indicates the current state of the service registration.</span></span> |
| [<span data-ttu-id="cd343-111">**Служба**</span><span class="sxs-lookup"><span data-stu-id="cd343-111">**Service**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | <span data-ttu-id="cd343-112">Возвращает указатель на интерфейс [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) .</span><span class="sxs-lookup"><span data-stu-id="cd343-112">Gets a pointer to an [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) interface.</span></span> <span data-ttu-id="cd343-113">Это свойство является свойством по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cd343-113">This property is the default property.</span></span>                                    |



 

 

 



