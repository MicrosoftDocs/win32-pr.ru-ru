---
title: Проверка подлинности пользователей
description: Сам протокол проверки подлинности может выполнять проверку подлинности пользователя с помощью защищенного EAP (PEAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "103785106"
---
# <a name="user-authentication"></a><span data-ttu-id="93ac4-103">Проверка подлинности пользователей</span><span class="sxs-lookup"><span data-stu-id="93ac4-103">User Authentication</span></span>

<span data-ttu-id="93ac4-104">Сам протокол проверки подлинности может выполнять проверку подлинности пользователя с помощью защищенного EAP (PEAP).</span><span class="sxs-lookup"><span data-stu-id="93ac4-104">The authentication protocol itself can authenticate the user via Protected EAP (PEAP).</span></span> <span data-ttu-id="93ac4-105">Кроме того, в операционной системе встроены два поставщика проверки подлинности: проверка подлинности домена Windows (доступ через службы каталогов) и пользовательская служба удаленного доступа (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="93ac4-105">There are also two authentication providers built into the operating system: Windows domain authentication (accessed via Directory Services) and Remote Access Dial-In User Service (RADIUS).</span></span>

<span data-ttu-id="93ac4-106">Если RADIUS является поставщиком проверки подлинности, подключаемый модуль EAP устанавливается на сервере RADIUS, а не на сервере точки доступа к беспроводной сети (AP), например на сервере RAS.</span><span class="sxs-lookup"><span data-stu-id="93ac4-106">In the case where RADIUS is the authentication provider, the EAP Plug-in is installed on the RADIUS server rather than on the wireless Access Point (AP) server, such as a RAS server.</span></span> <span data-ttu-id="93ac4-107">Сервер AP передает пакеты EAP непосредственно от клиента в службу проверки подлинности на сервере RADIUS.</span><span class="sxs-lookup"><span data-stu-id="93ac4-107">The AP server passes EAP packets directly from the client to the authentication service on the RADIUS server.</span></span> <span data-ttu-id="93ac4-108">Сервер AP не обрабатывает какие-либо сведения в пакетах EAP, но для создания безопасного подключения он должен принять ключи шифрования, созданные PEAP на стороне сервера (256 бит).</span><span class="sxs-lookup"><span data-stu-id="93ac4-108">The AP server does not process any of the information in the EAP packets, but it must accept the server-side, full strength (256 bit) PEAP generated encryption keys in order to create the secure connection.</span></span>

 

 




