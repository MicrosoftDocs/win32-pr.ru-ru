---
description: Обмен данными между клиентом и сервером
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Обмен данными между клиентом и сервером
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155906"
---
# <a name="clientserver-exchange"></a><span data-ttu-id="d8fc6-103">Обмен данными между клиентом и сервером</span><span class="sxs-lookup"><span data-stu-id="d8fc6-103">Client/Server Exchange</span></span>

<span data-ttu-id="d8fc6-104">После того как пользователь получил билет на сервер, клиент рабочей станции может установить безопасный сеанс связи с этим сервером.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-104">After a user has a ticket to a server, the workstation client can establish a secure communications session with that server.</span></span>

<span data-ttu-id="d8fc6-105">**Установка безопасного сеанса связи с сервером**</span><span class="sxs-lookup"><span data-stu-id="d8fc6-105">**To establish a secure communications session with a server**</span></span>

1.  <span data-ttu-id="d8fc6-106">Клиент отправляет серверу сообщение типа КРБ \_ AP \_ req (запрос приложения Kerberos).</span><span class="sxs-lookup"><span data-stu-id="d8fc6-106">The client sends the server a message of type KRB\_AP\_REQ (Kerberos Application Request).</span></span> <span data-ttu-id="d8fc6-107">Это сообщение содержит сообщение средства проверки подлинности, зашифрованное с помощью ключа, отправленного [*центр распространения ключей*](/windows/desktop/SecGloss/k-gly) (KDC) для сеанса с сервером, билет для сеансов с сервером и флаг, указывающий, запрашивает ли клиент взаимную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-107">This message contains an authenticator message that is encrypted with the key sent by the [*Key Distribution Center*](/windows/desktop/SecGloss/k-gly) (KDC) for the session with the server, the ticket for sessions with the server, and a flag that indicates whether the client requests mutual authentication.</span></span> <span data-ttu-id="d8fc6-108">Установка флага, запрашивающего взаимную проверку подлинности, — один из вариантов настройки [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="d8fc6-108">Setting the flag that requests mutual authentication is one of the options in configuring [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="d8fc6-109">Пользователь никогда не запрашивает, следует ли использовать взаимную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-109">The user is never asked whether mutual authentication should be used.</span></span>
2.  <span data-ttu-id="d8fc6-110">Сервер получает КРБ \_ AP \_ , расшифровывает билет и извлекает данные авторизации пользователя и [*ключ сеанса*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="d8fc6-110">The server receives KRB\_AP\_REQ, decrypts the ticket, and extracts the user's authorization data and the [*session key*](/windows/desktop/SecGloss/s-gly).</span></span>
3.  <span data-ttu-id="d8fc6-111">Сервер использует ключ сеанса из билета для расшифровки сообщения средства проверки подлинности пользователя и вычисляет метку времени в.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-111">The server uses the session key from the ticket to decrypt the user's authenticator message and evaluates the time stamp inside.</span></span>
4.  <span data-ttu-id="d8fc6-112">Если сообщение проверки подлинности является допустимым, сервер проверяет флаг взаимной проверки подлинности в запросе клиента.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-112">If the authenticator message is valid, the server checks the mutual authentication flag in the client's request.</span></span>
5.  <span data-ttu-id="d8fc6-113">Если установлен флаг взаимной проверки подлинности, то сервер использует сеансовый ключ для шифрования времени из сообщения проверки подлинности пользователя и возвращает результат в сообщении типа КРБ \_ AP \_ (ответ приложения Kerberos).</span><span class="sxs-lookup"><span data-stu-id="d8fc6-113">If the mutual authentication flag is set, the server uses the session key to encrypt the time from the user's authenticator message and returns the result in a message of type KRB\_AP\_REP (Kerberos Application Reply).</span></span>
6.  <span data-ttu-id="d8fc6-114">Когда клиент получает КРБ \_ AP \_ , он расшифровывает сообщение проверки подлинности сервера с помощью ключа сеанса, который используется совместно с сервером, и сравнивает время, отправленное службой, со временем исходного сообщения средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-114">When the client receives KRB\_AP\_REP, it decrypts the server's authenticator message with the session key it shares with the server and compares the time sent back by the service with the time in its original authenticator message.</span></span> <span data-ttu-id="d8fc6-115">Если они совпадают, Клиент гарантирует, что служба является подлинной, и подключение будет продолжено.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-115">If they match, the client is assured that the service is genuine, and the connection proceeds.</span></span>

 

 
