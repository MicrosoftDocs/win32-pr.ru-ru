---
title: Поддержка узла безопасности RAS
description: Windows NT 4,0 предоставляет сторонний DLL-библиотеку безопасности RAS, которая позволяет усовершенствовать встроенные функции безопасности RAS. Windows 95 не обеспечивает такую поддержку.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Поддержка узла, RAS
- Поддержка узла безопасности, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777276"
---
# <a name="ras-security-host-support"></a><span data-ttu-id="30a20-106">Поддержка узла безопасности RAS</span><span class="sxs-lookup"><span data-stu-id="30a20-106">RAS Security Host Support</span></span>

<span data-ttu-id="30a20-107">Windows NT 4,0 предоставляет сторонний DLL-библиотеку безопасности RAS, которая позволяет усовершенствовать встроенные функции безопасности RAS.</span><span class="sxs-lookup"><span data-stu-id="30a20-107">Windows NT 4.0 provides a way for a third-party RAS security DLL to enhance the built-in RAS security features.</span></span> <span data-ttu-id="30a20-108">Windows 95 не обеспечивает такую поддержку.</span><span class="sxs-lookup"><span data-stu-id="30a20-108">Windows 95 does not provide this support.</span></span>

<span data-ttu-id="30a20-109">Сервер удаленного доступа Windows NT/Windows 2000 предоставляет механизмы безопасности для проверки сетевого доступа удаленных пользователей.</span><span class="sxs-lookup"><span data-stu-id="30a20-109">A Windows NT/Windows 2000 RAS server provides security mechanisms for validating the network access of remote users.</span></span> <span data-ttu-id="30a20-110">Когда сервер удаленного доступа получает вызов, он проверяет учетные данные пользователя на соответствие локальной базе данных или доменной учетной записи домена.</span><span class="sxs-lookup"><span data-stu-id="30a20-110">When a RAS server receives a call, it validates the user's credentials against the local or domain account database.</span></span> <span data-ttu-id="30a20-111">Служба RAS также поддерживает безопасность обратных вызовов, при которой сервер RAS зависает, а затем обращается к удаленному пользователю для установления соединения.</span><span class="sxs-lookup"><span data-stu-id="30a20-111">RAS also supports call-back security, in which the RAS server hangs up and then calls back to the remote user to establish the connection.</span></span> <span data-ttu-id="30a20-112">Для сетей, в которых уровень безопасности недостаточно, можно установить сторонние DLL-библиотеки безопасности RAS.</span><span class="sxs-lookup"><span data-stu-id="30a20-112">For networks in which this level of security is not enough, you can install a third-party RAS security DLL.</span></span> <span data-ttu-id="30a20-113">После этого библиотека DLL безопасности может проверить подлинность удаленного пользователя, считывая сведения о безопасности из базы данных, отличной от стандартной базы данных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="30a20-113">The security DLL can then authenticate a remote user by reading security information from a database other than the standard user account database.</span></span>

<span data-ttu-id="30a20-114">Когда сервер удаленного доступа получает вызов, он вызывает библиотеку DLL безопасности для проверки подлинности удаленного пользователя.</span><span class="sxs-lookup"><span data-stu-id="30a20-114">When the RAS server receives a call, it invokes the security DLL to authenticate the remote user.</span></span> <span data-ttu-id="30a20-115">Поддержка узла безопасности RAS предоставляет библиотеке DLL безопасности механизм взаимодействия с удаленным пользователем через окно терминала на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="30a20-115">The RAS security host support provides a mechanism for the security DLL to communicate with the remote user through a terminal window on the remote computer.</span></span> <span data-ttu-id="30a20-116">В типичном сценарии DLL-библиотека безопасности запрашивает имя входа удаленного пользователя.</span><span class="sxs-lookup"><span data-stu-id="30a20-116">In a typical scenario, the security DLL asks for the logon name of the remote user.</span></span> <span data-ttu-id="30a20-117">Затем библиотека DLL использует свою закрытую базу данных безопасности для формирования запроса на отправку в удаленный терминал.</span><span class="sxs-lookup"><span data-stu-id="30a20-117">The DLL then uses its private security database to formulate a challenge to send to the remote terminal.</span></span> <span data-ttu-id="30a20-118">Например, задача может быть кодом, который пользователь должен предоставить в качестве входных данных для читателя кардкэй.</span><span class="sxs-lookup"><span data-stu-id="30a20-118">For example, the challenge could be a code that the user must provide as input to a cardkey reader.</span></span> <span data-ttu-id="30a20-119">Затем средство чтения кардкэй отображает ответ, который удаленный пользователь вводит в окне терминала.</span><span class="sxs-lookup"><span data-stu-id="30a20-119">The cardkey reader then displays a response that the remote user types in the terminal window.</span></span> <span data-ttu-id="30a20-120">Затем библиотека безопасности проверяет ответ на данные пользователя в частной базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="30a20-120">The security DLL then validates the response against the user's information in the private security database.</span></span>

<span data-ttu-id="30a20-121">Если DLL-библиотека безопасности проверяет подлинность удаленного пользователя, сервер RAS выполняет собственную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="30a20-121">If the security DLL authenticates the remote user, the RAS server performs its own authentication.</span></span> <span data-ttu-id="30a20-122">Это гарантирует, что безопасность RAS всегда будет проверять подлинность удаленного пользователя, даже если установлена библиотека DLL безопасности, предоставляющая доступ всем пользователям.</span><span class="sxs-lookup"><span data-stu-id="30a20-122">This ensures that RAS security always authenticates a remote user, even if a security DLL is installed that grants access to all users.</span></span>

> [!Note]  
> <span data-ttu-id="30a20-123">В настоящее время Windows NT или Windows 2000 предоставляет поддержку узла безопасности RAS только для асинхронных подключений через модем. другие типы подключений, такие как Ethernet (не являющиеся модемными), VPN (которая также не является модемным подключением) или ISDN (которая является синхронной), не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="30a20-123">Windows NT/Windows 2000 currently provides RAS security host support only for asynchronous modem connections; other types of connections such as Ethernet (which is not a modem connection), VPN (which is also not a modem connection), or ISDN (which is synchronous), are not supported.</span></span>

 

 

 




