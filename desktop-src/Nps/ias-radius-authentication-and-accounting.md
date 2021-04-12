---
title: Проверка подлинности, авторизация и учет RADIUS
description: Сервер политики сети полностью поддерживает протокол протокол RADIUS (RADIUS). Протокол RADIUS является стандартом де-факто для проверки подлинности удаленного пользователя и описан в RFC 2865 и RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413338"
---
# <a name="radius-authentication-authorization-and-accounting"></a><span data-ttu-id="4ed07-104">Проверка подлинности, авторизация и учет RADIUS</span><span class="sxs-lookup"><span data-stu-id="4ed07-104">RADIUS Authentication, Authorization, and Accounting</span></span>

> [!Note]  
> <span data-ttu-id="4ed07-105">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4ed07-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="4ed07-106">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="4ed07-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="4ed07-107">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="4ed07-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="4ed07-108">Сервер политики сети полностью поддерживает протокол протокол RADIUS (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="4ed07-108">NPS fully supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span> <span data-ttu-id="4ed07-109">Протокол RADIUS является стандартом де-факто для проверки подлинности удаленного пользователя и описан в [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) и [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="4ed07-109">The RADIUS protocol is the de facto standard for remote user authentication and it is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-authentication-and-authorization"></a><span data-ttu-id="4ed07-110">Проверка подлинности и авторизация RADIUS</span><span class="sxs-lookup"><span data-stu-id="4ed07-110">RADIUS Authentication and Authorization</span></span>

<span data-ttu-id="4ed07-111">На следующей схеме показан клиент, выполняющий проверку подлинности ("пользователь"), подключающийся к серверу сетевого доступа (NAS) через коммутируемое подключение, используя протокол PPP (PPP).</span><span class="sxs-lookup"><span data-stu-id="4ed07-111">The following diagram shows an authenticating client ("User") connecting to a Network Access Server (NAS) over a dial-up connection, using the Point-to-Point Protocol (PPP).</span></span> <span data-ttu-id="4ed07-112">Для проверки подлинности пользователя NAS обращается к удаленному серверу, на котором выполняется сервер политики сети.</span><span class="sxs-lookup"><span data-stu-id="4ed07-112">In order to authenticate the User, the NAS contacts a remote server running NPS.</span></span> <span data-ttu-id="4ed07-113">NAS и сервер NPS обмениваются данными по протоколу RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4ed07-113">The NAS and the NPS server communicate using the RADIUS protocol.</span></span>

![Проверка подлинности удаленного пользователя](images/ias01.png)

<span data-ttu-id="4ed07-115">NAS работает как клиент сервера или серверов, поддерживающих протокол RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4ed07-115">A NAS operates as a client of a server or servers that support the RADIUS protocol.</span></span> <span data-ttu-id="4ed07-116">Серверы, поддерживающие протокол RADIUS, обычно называются серверами RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4ed07-116">Servers that support the RADIUS protocol are generally referred to as the RADIUS servers.</span></span> <span data-ttu-id="4ed07-117">Клиент RADIUS, то есть NAS, передает сведения о пользователе на назначенные серверы RADIUS, а затем действует на ответ, возвращаемый серверами.</span><span class="sxs-lookup"><span data-stu-id="4ed07-117">The RADIUS client, that is, the NAS, passes information about the User to designated RADIUS servers, and then acts on the response that the servers return.</span></span> <span data-ttu-id="4ed07-118">Запрос, отправленный NAS серверу RADIUS для проверки подлинности пользователя, обычно называется запросом проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4ed07-118">The request sent by the NAS to the RADIUS server in order to authenticate the User is generally called an "authentication request."</span></span>

<span data-ttu-id="4ed07-119">Если сервер RADIUS успешно проходит проверку подлинности пользователя, сервер RADIUS возвращает серверу NAS сведения о конфигурации, чтобы он мог предоставить пользователю сетевую службу.</span><span class="sxs-lookup"><span data-stu-id="4ed07-119">If a RADIUS server authenticates the User successfully, the RADIUS server returns configuration information to the NAS so that it can provide network service to the user.</span></span> <span data-ttu-id="4ed07-120">Эти сведения о конфигурации состоят из "авторизаций" и содержат, помимо прочего, тип NAS службы, который может предоставить пользователю (например, PPP или Telnet).</span><span class="sxs-lookup"><span data-stu-id="4ed07-120">This configuration information is composed of "authorizations" and contains, among others, the type of service NAS may provide to the User (for example, PPP, or telnet).</span></span>

<span data-ttu-id="4ed07-121">Пока сервер RADIUS обрабатывает запрос проверки подлинности, он может выполнять такие функции авторизации, как проверка номера телефона пользователя и проверка наличия у пользователя уже запущенного сеанса.</span><span class="sxs-lookup"><span data-stu-id="4ed07-121">While the RADIUS server is processing the authentication request, it can perform authorization functions such as verifying the user's telephone number and checking whether the user already has a session in progress.</span></span> <span data-ttu-id="4ed07-122">Сервер RADIUS может определить, есть ли у пользователя уже запущенный сеанс, обратившись к серверу состояний.</span><span class="sxs-lookup"><span data-stu-id="4ed07-122">The RADIUS server can determine whether the user already has a session in progress by contacting a state server.</span></span>

<span data-ttu-id="4ed07-123">Дополнительные сведения о проверке подлинности и авторизации RADIUS см. в [документе RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span><span class="sxs-lookup"><span data-stu-id="4ed07-123">For more information on RADIUS authentication and authorization, see [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span></span>

## <a name="radius-accounting"></a><span data-ttu-id="4ed07-124">Учет RADIUS</span><span class="sxs-lookup"><span data-stu-id="4ed07-124">RADIUS Accounting</span></span>

<span data-ttu-id="4ed07-125">Сервер RADIUS также собирает разнообразные сведения, отправляемые NAS, которые можно использовать для учета и создания отчетов о сетевых операциях.</span><span class="sxs-lookup"><span data-stu-id="4ed07-125">The RADIUS server also collects a variety of information sent by the NAS that can be used for accounting and for reporting on network activity.</span></span> <span data-ttu-id="4ed07-126">Клиент RADIUS отправляет сведения на назначенные серверы RADIUS при входе пользователя в систему и выходе из нее.</span><span class="sxs-lookup"><span data-stu-id="4ed07-126">The RADIUS client sends information to designated RADIUS servers when the User logs on and logs off.</span></span> <span data-ttu-id="4ed07-127">Клиент RADIUS может периодически передавать дополнительные сведения об использовании во время выполнения сеанса.</span><span class="sxs-lookup"><span data-stu-id="4ed07-127">The RADIUS client may send additional usage information on a periodic basis while the session is in progress.</span></span> <span data-ttu-id="4ed07-128">Запросы, отправленные клиентом на сервер для записи сведений о входе, выходе и использовании, обычно называются запросами на учет.</span><span class="sxs-lookup"><span data-stu-id="4ed07-128">The requests sent by the client to the server to record logon/logoff and usage information are generally called "accounting requests."</span></span>

<span data-ttu-id="4ed07-129">Дополнительные сведения о учете RADIUS см. в [документе RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="4ed07-129">For more information on RADIUS accounting, see [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-proxy"></a><span data-ttu-id="4ed07-130">RADIUS-прокси</span><span class="sxs-lookup"><span data-stu-id="4ed07-130">RADIUS Proxy</span></span>

<span data-ttu-id="4ed07-131">Сервер RADIUS может работать в качестве прокси-клиента для других серверов RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4ed07-131">A RADIUS server can act as a proxy client to other RADIUS servers.</span></span> <span data-ttu-id="4ed07-132">В таких случаях сервер RADIUS, обращенный к серверу NAS, передает запрос проверки подлинности или учета на другой сервер RADIUS, который фактически выполняет проверку подлинности или задачу учета.</span><span class="sxs-lookup"><span data-stu-id="4ed07-132">In these cases, the RADIUS server contacted by the NAS passes the authentication or accounting request to another RADIUS server that actually performs the authentication or the accounting task.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ed07-133">См. также</span><span class="sxs-lookup"><span data-stu-id="4ed07-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed07-134">Служба проверки подлинности в Интернете и сервер политики сети</span><span class="sxs-lookup"><span data-stu-id="4ed07-134">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="4ed07-135">RADIUS-пакеты учета</span><span class="sxs-lookup"><span data-stu-id="4ed07-135">RADIUS Accounting Packets</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="4ed07-136">Работа с сервером состояний</span><span class="sxs-lookup"><span data-stu-id="4ed07-136">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 