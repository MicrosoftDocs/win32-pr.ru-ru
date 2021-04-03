---
title: Расширения сервера политики сети
description: API расширений NPS позволяет разработчикам программного обеспечения создавать библиотеки DLL расширения, которые можно использовать для проверки подлинности, авторизации и учета. API расширений NPS поддерживает протокол протокол RADIUS (RADIUS).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987737"
---
# <a name="network-policy-server-extensions"></a><span data-ttu-id="8db19-104">Расширения сервера политики сети</span><span class="sxs-lookup"><span data-stu-id="8db19-104">Network Policy Server Extensions</span></span>

> [!Note]  
> <span data-ttu-id="8db19-105">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8db19-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="8db19-106">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="8db19-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="8db19-107">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="8db19-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="8db19-108">API расширений NPS позволяет разработчикам программного обеспечения создавать библиотеки DLL расширения, которые можно использовать для проверки подлинности, авторизации и учета.</span><span class="sxs-lookup"><span data-stu-id="8db19-108">The NPS Extensions API enables software developers to write extension DLLs that can be used for authentication, authorization, and accounting.</span></span> <span data-ttu-id="8db19-109">API расширений NPS поддерживает протокол протокол RADIUS (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="8db19-109">NPS Extensions API supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span>

<span data-ttu-id="8db19-110">Библиотеки DLL расширения, реализованные с помощью API расширений NPS, могут предоставлять расширенные возможности управления сеансами и учета.</span><span class="sxs-lookup"><span data-stu-id="8db19-110">The extension DLLs implemented using the NPS Extensions API can provide enhanced session control and accounting.</span></span> <span data-ttu-id="8db19-111">Эти библиотеки DLL можно использовать для таких сценариев, как Управление числом сетевых сеансов конечных пользователей, использование сервера состояний и подключение к базам данных проверки подлинности домена и службам Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8db19-111">These DLLs can be used for scenarios such as controlling the number of end-user network sessions, using a state server, and connecting to domain authentication databases and Active Directory services.</span></span> <span data-ttu-id="8db19-112">Библиотеки DLL расширения могут расширять авторизации удаленного доступа, предоставляемые NPS, добавляя собственные авторизации при отправке ответа Accept обратно клиенту, выполняющему проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="8db19-112">The extension DLLs can expand the remote access authorizations provided by NPS by adding their own authorizations when sending an Accept response back to an authenticating client.</span></span>

<span data-ttu-id="8db19-113">API расширений NPS применяется в любой вычислительной среде, где повышение эффективности проверки подлинности удаленных пользователей через удаленный сервер.</span><span class="sxs-lookup"><span data-stu-id="8db19-113">NPS Extensions API is applicable in any computing environment where it would improve efficiency to authenticate dial-in users through a remote server.</span></span> <span data-ttu-id="8db19-114">Эта технология особенно полезна для поставщиков услуг Интернета (ISP).</span><span class="sxs-lookup"><span data-stu-id="8db19-114">This technology is especially useful for Internet Service Providers (ISPs).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8db19-115">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="8db19-115">In This Section</span></span>

[<span data-ttu-id="8db19-116">Обзор</span><span class="sxs-lookup"><span data-stu-id="8db19-116">Overview</span></span>](/windows/desktop/Nps/ias-about-internet-authentication-service)

<span data-ttu-id="8db19-117">Общие сведения о протоколе RADIUS и API расширений NPS.</span><span class="sxs-lookup"><span data-stu-id="8db19-117">General information about RADIUS and the NPS Extensions API.</span></span>

[<span data-ttu-id="8db19-118">Использующ</span><span class="sxs-lookup"><span data-stu-id="8db19-118">Using</span></span>](/windows/desktop/Nps/ias-using-internet-authentication-service)

<span data-ttu-id="8db19-119">Пример кода, демонстрирующий использование API расширений NPS.</span><span class="sxs-lookup"><span data-stu-id="8db19-119">Sample code that demonstrates how to use the NPS Extensions API.</span></span>

[<span data-ttu-id="8db19-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="8db19-120">Reference</span></span>](/windows/desktop/Nps/ias-internet-authentication-service-reference)

<span data-ttu-id="8db19-121">Документация по перечисленным типам, функциям и структурам, составляющим API расширений NPS.</span><span class="sxs-lookup"><span data-stu-id="8db19-121">Documentation of enumerated types, functions, and structures that compose the NPS Extensions API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8db19-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8db19-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8db19-123">Сервер политики сети (служба проверки подлинности в Интернете)</span><span class="sxs-lookup"><span data-stu-id="8db19-123">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="8db19-124">Протокол расширенной проверки подлинности (EAP)</span><span class="sxs-lookup"><span data-stu-id="8db19-124">Extensible Authentication Protocol (EAP)</span></span>](../eap/eap-start-page.md)
</dt> </dl>

 

 