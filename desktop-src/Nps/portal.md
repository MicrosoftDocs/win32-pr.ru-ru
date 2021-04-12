---
title: Сервер политики сети
description: Сервер политики сети (NPS) — это реализация корпорацией Майкрософт сервера RADIUS и прокси.
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337884"
---
# <a name="network-policy-server"></a><span data-ttu-id="2e84e-103">Сервер политики сети</span><span class="sxs-lookup"><span data-stu-id="2e84e-103">Network Policy Server</span></span>

## <a name="purpose"></a><span data-ttu-id="2e84e-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="2e84e-104">Purpose</span></span>

<span data-ttu-id="2e84e-105">Сервер политики сети (NPS) — это реализация корпорацией Майкрософт сервера RADIUS и прокси.</span><span class="sxs-lookup"><span data-stu-id="2e84e-105">Network Policy Server (NPS) is the Microsoft implementation of a Remote Authentication Dial-in User Service (RADIUS) server and proxy.</span></span> <span data-ttu-id="2e84e-106">Это является последователем службы проверки подлинности в Интернете (IAS).</span><span class="sxs-lookup"><span data-stu-id="2e84e-106">It is the successor of Internet Authentication Service (IAS).</span></span>

<span data-ttu-id="2e84e-107">В качестве сервера RADIUS сервер политики сети выполняет проверку подлинности, авторизацию и учет для подключений по беспроводной сети, коммутатора с проверкой подлинности и подключениям удаленного доступа и виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="2e84e-107">As a RADIUS server, NPS performs authentication, authorization, and accounting for wireless, authenticating switch, and remote access dial-up and virtual private network (VPN) connections.</span></span>

<span data-ttu-id="2e84e-108">NPS также является сервером оценки работоспособности для защиты доступа к сети (NAP).</span><span class="sxs-lookup"><span data-stu-id="2e84e-108">NPS is also a health evaluator server for Network Access Protection (NAP).</span></span> <span data-ttu-id="2e84e-109">NPS выполняет проверку подлинности и авторизацию попыток подключения к сети и, основываясь на настроенных политиках работоспособности системы, оценивает соответствие работоспособности компьютера и определяет, как ограничить сетевой доступ или обмен данными на несоответствующем компьютере.</span><span class="sxs-lookup"><span data-stu-id="2e84e-109">NPS performs authentication and authorization of network connection attempts and, based on configured system health policies, evaluates computer health compliance and determines how to limit a noncompliant computer's network access or communication.</span></span> <span data-ttu-id="2e84e-110">Это новая функция, относящаяся только к NPS; IAS не поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="2e84e-110">This is a new feature specific to NPS only; IAS does not support it.</span></span> <span data-ttu-id="2e84e-111">Полный список новых возможностей NPS см. в статье [Служба проверки подлинности в Интернете и сервер политики сети](internet-authentication-service-vs-network-policy-server.md) .</span><span class="sxs-lookup"><span data-stu-id="2e84e-111">See [Internet Authentication Service and Network Policy Server](internet-authentication-service-vs-network-policy-server.md) for a complete list of features new to NPS.</span></span>

<span data-ttu-id="2e84e-112">Сервер политики сети включает два набора API: API расширений NPS и API серверных объектов данных (SDO).</span><span class="sxs-lookup"><span data-stu-id="2e84e-112">NPS includes two API sets: NPS Extensions API and Server Data Objects (SDO) API.</span></span> <span data-ttu-id="2e84e-113">И API расширений NPS, и API SDO поддерживаются службой проверки подлинности в Интернете (основы).</span><span class="sxs-lookup"><span data-stu-id="2e84e-113">Both NPS Extensions API and SDO API are also supported by the precursor of NPS, the Internet Authentication Service.</span></span>

<span data-ttu-id="2e84e-114">API расширений NPS можно использовать для расширения методов проверки подлинности, авторизации и учета, предоставляемых NPS и ранее с помощью IAS.</span><span class="sxs-lookup"><span data-stu-id="2e84e-114">NPS Extensions API can be used to extend the authentication, authorization, and accounting methods offered by NPS and previously by IAS.</span></span>

<span data-ttu-id="2e84e-115">API объектов данных сервера можно использовать для управления конфигурацией политики сети на компьютере, на котором выполняется сервер политики сети или IAS.</span><span class="sxs-lookup"><span data-stu-id="2e84e-115">Server Data Objects API can be used to manipulate the network policy configuration on a computer that runs NPS or IAS.</span></span>

> [!Note]  
> <span data-ttu-id="2e84e-116">Политики сети в NPS эквивалентны политикам удаленного доступа в IAS.</span><span class="sxs-lookup"><span data-stu-id="2e84e-116">Network policies in NPS are equivalent to remote access policies in IAS.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="2e84e-117">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="2e84e-117">Developer audience</span></span>

<span data-ttu-id="2e84e-118">API расширений NPS предназначен для использования программистами, использующими программное обеспечение для разработки на C/C++.</span><span class="sxs-lookup"><span data-stu-id="2e84e-118">The NPS Extensions API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="2e84e-119">Программисты должны быть знакомы с основными понятиями сети и протоколом RADIUS.</span><span class="sxs-lookup"><span data-stu-id="2e84e-119">Programmers should be familiar with networking concepts and the RADIUS protocol.</span></span> <span data-ttu-id="2e84e-120">Протокол RADIUS описан в [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) и [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="2e84e-120">RADIUS is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

<span data-ttu-id="2e84e-121">API объектов данных сервера предназначен для использования программистами, использующими C/C++ или Visual Basic разработки программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="2e84e-121">The Server Data Objects API is designed for use by programmers using C/C++ or Visual Basic development software.</span></span> <span data-ttu-id="2e84e-122">Программисты должны быть знакомы со [службой удаленного доступа](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) и протоколом RADIUS.</span><span class="sxs-lookup"><span data-stu-id="2e84e-122">Programmers should be familiar with [Remote Access Service](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) and the RADIUS protocol.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2e84e-123">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="2e84e-123">Run-time requirements</span></span>

<span data-ttu-id="2e84e-124">API расширений NPS поддерживается в Windows Server 2008 с установкой коммерческой Интернет-службы Майкрософт (МЦИС).</span><span class="sxs-lookup"><span data-stu-id="2e84e-124">NPS Extensions API is supported on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

<span data-ttu-id="2e84e-125">API объектов данных сервера поддерживается в Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2e84e-125">Server Data Objects API is supported on Windows Server 2008.</span></span>

<span data-ttu-id="2e84e-126">Сервер политики сети доступен в Windows Server 2008 с установкой коммерческой Интернет-службы Майкрософт (МЦИС).</span><span class="sxs-lookup"><span data-stu-id="2e84e-126">NPS is available on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2e84e-127">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="2e84e-127">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2e84e-128">Обзор</span><span class="sxs-lookup"><span data-stu-id="2e84e-128">Overview</span></span>](about-network-policy-server.md)
</dt> <dd>

<span data-ttu-id="2e84e-129">Общие сведения о RADIUS, IAS и NPS.</span><span class="sxs-lookup"><span data-stu-id="2e84e-129">General information regarding RADIUS, IAS, and NPS.</span></span>

</dd> <dt>

[<span data-ttu-id="2e84e-130">API расширений сервера политики сети</span><span class="sxs-lookup"><span data-stu-id="2e84e-130">Network Policy Server Extensions API</span></span>](ias-extensions.md)
</dt> <dd>

<span data-ttu-id="2e84e-131">API для реализации библиотек DLL расширения, используемых для проверки подлинности, авторизации и учета.</span><span class="sxs-lookup"><span data-stu-id="2e84e-131">API for implementing extension DLLs used for authentication, authorization, and accounting.</span></span>

</dd> <dt>

[<span data-ttu-id="2e84e-132">API объектов данных сервера</span><span class="sxs-lookup"><span data-stu-id="2e84e-132">Server Data Objects API</span></span>](server-data-objects.md)
</dt> <dd>

<span data-ttu-id="2e84e-133">API для управления конфигурацией политики сети.</span><span class="sxs-lookup"><span data-stu-id="2e84e-133">API for managing the network policy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="2e84e-134">Программирование SQL</span><span class="sxs-lookup"><span data-stu-id="2e84e-134">SQL Programmability</span></span>](sql-programmability.md)
</dt> <dd>

<span data-ttu-id="2e84e-135">Примеры хранимых процедур, используемых для управления ведением журнала NPS (IAS).</span><span class="sxs-lookup"><span data-stu-id="2e84e-135">Samples of stored procedures used for managing NPS (IAS) logging.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2e84e-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2e84e-136">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2e84e-137">[TechNet: сервер политики сети](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="2e84e-137">[TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="2e84e-138">[TechNet: служба проверки подлинности в Интернете](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="2e84e-138">[TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="2e84e-139">Защита доступа к сети</span><span class="sxs-lookup"><span data-stu-id="2e84e-139">Network Access Protection</span></span>](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 