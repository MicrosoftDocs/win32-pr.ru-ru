---
title: Сведения о расширениях NPS
description: В этом разделе описывается, как реализовать библиотеки DLL для расширения функциональных возможностей NPS. В нем описывается взаимодействие между сервером политики сети и библиотеками DLL и представлены некоторые рекомендации по проектированию библиотек DLL.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661764"
---
# <a name="about-nps-extensions"></a><span data-ttu-id="3239a-104">Сведения о расширениях NPS</span><span class="sxs-lookup"><span data-stu-id="3239a-104">About NPS Extensions</span></span>

> [!Note]  
> <span data-ttu-id="3239a-105">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3239a-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="3239a-106">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="3239a-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="3239a-107">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="3239a-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="3239a-108">В этом разделе описывается, как реализовать библиотеки DLL для расширения функциональных возможностей NPS.</span><span class="sxs-lookup"><span data-stu-id="3239a-108">This section describes how to implement DLLs to extend the functionality of NPS.</span></span> <span data-ttu-id="3239a-109">В нем описывается взаимодействие между сервером политики сети и библиотеками DLL и представлены некоторые рекомендации по проектированию библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="3239a-109">It describes the interaction between NPS and the DLLs, and presents some design considerations regarding the DLLs.</span></span>

<span data-ttu-id="3239a-110">Сервер политики сети предоставляет две точки расширения: одну для проверки подлинности, а другую для авторизации.</span><span class="sxs-lookup"><span data-stu-id="3239a-110">NPS provides two extension points, one for authentication and the other for authorization.</span></span> <span data-ttu-id="3239a-111">Проверка подлинности означает проверку удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3239a-111">Authentication refers to verifying the identity of the user.</span></span> <span data-ttu-id="3239a-112">Авторизация означает определение служб, которые сеть должна предоставить пользователю.</span><span class="sxs-lookup"><span data-stu-id="3239a-112">Authorization refers to determining what services the network should provide to the user.</span></span> <span data-ttu-id="3239a-113">Две точки расширения соответствуют библиотекам DLL расширения проверки подлинности и библиотекам расширения авторизации.</span><span class="sxs-lookup"><span data-stu-id="3239a-113">The two extension points correspond to Authentication Extension DLLs and Authorization Extension DLLs.</span></span> <span data-ttu-id="3239a-114">Каждая точка расширения может поддерживать несколько библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="3239a-114">Each extension point can support multiple DLLs.</span></span>

<span data-ttu-id="3239a-115">Сервер политики сети предоставляет службы проверки подлинности и авторизации.</span><span class="sxs-lookup"><span data-stu-id="3239a-115">NPS provides both authentication and authorization services.</span></span> <span data-ttu-id="3239a-116">Библиотеки DLL расширения проверки подлинности вызываются NPS до встроенной проверки подлинности и авторизации NPS.</span><span class="sxs-lookup"><span data-stu-id="3239a-116">Authentication Extension DLLs are called by NPS prior to the built-in NPS authentication and authorization.</span></span> <span data-ttu-id="3239a-117">Библиотеки DLL расширения авторизации вызываются после проверки подлинности и авторизации NPS.</span><span class="sxs-lookup"><span data-stu-id="3239a-117">Authorization Extension DLLs are called after NPS authentication and authorization.</span></span>

<span data-ttu-id="3239a-118">На следующей схеме показан поток пакетов через сервер политики сети RADIUS, развернутый с помощью библиотек расширения.</span><span class="sxs-lookup"><span data-stu-id="3239a-118">The following diagram illustrates the flow of packets through an NPS RADIUS server that is expanded using Extension DLLs.</span></span>

![процесс проверки подлинности и авторизации NPS](images/ias03.png)

<span data-ttu-id="3239a-120">Если библиотека DLL расширения проверки подлинности возвращает ACCEPT, пакет пропускает проверку подлинности NPS и переходит непосредственно к авторизации NPS.</span><span class="sxs-lookup"><span data-stu-id="3239a-120">If an Authentication Extension DLL returns ACCEPT, the packet skips the NPS authentication and goes directly to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="3239a-121">При наличии нескольких библиотек DLL расширения проверки подлинности также могут быть пропущены остальные библиотеки DLL расширения.</span><span class="sxs-lookup"><span data-stu-id="3239a-121">When multiple Authentication Extension DLLs are present, the rest of the Extension DLLs might be skipped as well.</span></span> <span data-ttu-id="3239a-122">Дополнительные сведения см. [в разделе Настройка библиотек DLL расширения](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) .</span><span class="sxs-lookup"><span data-stu-id="3239a-122">See [Setting Up the Extension DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) for more information.</span></span>

 

<span data-ttu-id="3239a-123">Если библиотека DLL расширения проверки подлинности возвращает значение CONTINUE, пакет переходит на проверку подлинности NPS, а затем на авторизацию NPS.</span><span class="sxs-lookup"><span data-stu-id="3239a-123">If an Authentication Extension DLL returns CONTINUE, the packet goes to NPS authentication, and then to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="3239a-124">При наличии нескольких библиотек DLL расширения проверки подлинности все остальные библиотеки DLL модулей проверки подлинности вызываются до проверки подлинности NPS.</span><span class="sxs-lookup"><span data-stu-id="3239a-124">When multiple Authentication Extension DLLs are present, the rest of the Authentication Extension DLLs are invoked before NPS authentication.</span></span>

 

<span data-ttu-id="3239a-125">В следующих разделах библиотеки DLL расширения описаны более подробно:</span><span class="sxs-lookup"><span data-stu-id="3239a-125">The following topics describe the Extension DLLs in more detail:</span></span>

-   [<span data-ttu-id="3239a-126">Настройка библиотек DLL расширения</span><span class="sxs-lookup"><span data-stu-id="3239a-126">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [<span data-ttu-id="3239a-127">Вызов библиотек DLL расширения</span><span class="sxs-lookup"><span data-stu-id="3239a-127">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [<span data-ttu-id="3239a-128">Атрибуты идентификации пользователя</span><span class="sxs-lookup"><span data-stu-id="3239a-128">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)

 

 