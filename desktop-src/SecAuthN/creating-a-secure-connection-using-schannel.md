---
description: Как создать безопасное подключение с помощью канала Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Создание безопасного подключения с помощью канала Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814745"
---
# <a name="creating-a-secure-connection-using-schannel"></a><span data-ttu-id="0a193-103">Создание безопасного подключения с помощью канала Schannel</span><span class="sxs-lookup"><span data-stu-id="0a193-103">Creating a Secure Connection Using Schannel</span></span>

<span data-ttu-id="0a193-104">[*Пакет безопасности*](/windows/desktop/SecGloss/s-gly) SChannel предоставляет доступ к четырем [*протоколам безопасности*](/windows/desktop/SecGloss/s-gly):</span><span class="sxs-lookup"><span data-stu-id="0a193-104">The Schannel [*security package*](/windows/desktop/SecGloss/s-gly) provides access to four [*security protocols*](/windows/desktop/SecGloss/s-gly):</span></span>

-   [<span data-ttu-id="0a193-105">Безопасность транспортного уровня (TLS 1,2)</span><span class="sxs-lookup"><span data-stu-id="0a193-105">Transport Layer Security (TLS 1.2)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="0a193-106">Безопасность транспортного уровня (TLS 1,1)</span><span class="sxs-lookup"><span data-stu-id="0a193-106">Transport Layer Security (TLS 1.1)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="0a193-107">Безопасность транспортного уровня (TLS 1,0)</span><span class="sxs-lookup"><span data-stu-id="0a193-107">Transport Layer Security (TLS 1.0)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="0a193-108">SSL (SSL 3,0)</span><span class="sxs-lookup"><span data-stu-id="0a193-108">Secure Sockets Layer (SSL 3.0)</span></span>](secure-sockets-layer-protocol.md)
-   [<span data-ttu-id="0a193-109">SSL (SSL 2,0)</span><span class="sxs-lookup"><span data-stu-id="0a193-109">Secure Sockets Layer (SSL 2.0)</span></span>](secure-sockets-layer-protocol.md)

> [!Note]  
> <span data-ttu-id="0a193-110">Протоколы PCT и SSL 2,0 были заменены протоколом TLS и не должны использоваться для новой разработки.</span><span class="sxs-lookup"><span data-stu-id="0a193-110">The PCT and SSL 2.0 protocols have been superseded by the TLS protocol and should not be used for new development.</span></span>

 

<span data-ttu-id="0a193-111">**Настройка безопасного подключения между клиентом и сервером**</span><span class="sxs-lookup"><span data-stu-id="0a193-111">**To set up a secure connection between a client and server**</span></span>

1.  <span data-ttu-id="0a193-112">Получение учетных данных Schannel ([Получение учетных данных SChannel](obtaining-schannel-credentials.md)).</span><span class="sxs-lookup"><span data-stu-id="0a193-112">Obtain Schannel credentials ([Obtaining Schannel Credentials](obtaining-schannel-credentials.md)).</span></span>
2.  <span data-ttu-id="0a193-113">Создание контекста безопасности безопасного канала Schannel ([Создание контекста безопасности SChannel](creating-an-schannel-security-context.md)).</span><span class="sxs-lookup"><span data-stu-id="0a193-113">Create an Schannel security context ([Creating an Schannel Security Context](creating-an-schannel-security-context.md)).</span></span>

<span data-ttu-id="0a193-114">После установления соединения можно получить сведения о его атрибутах.</span><span class="sxs-lookup"><span data-stu-id="0a193-114">After a connection is established, you can retrieve information about its attributes.</span></span> <span data-ttu-id="0a193-115">Дополнительные сведения см. в разделе [Получение сведений о подключениях SChannel](getting-information-about-schannel-connections.md).</span><span class="sxs-lookup"><span data-stu-id="0a193-115">For details, see [Getting Information About Schannel Connections](getting-information-about-schannel-connections.md).</span></span>

<span data-ttu-id="0a193-116">Если после установления подключения происходит потеря требований безопасности приложения или подключение теряется, можно повторно согласовать соединение.</span><span class="sxs-lookup"><span data-stu-id="0a193-116">If, after you have established a connection, the security requirements of your application change or the connection is lost, you can renegotiate the connection.</span></span> <span data-ttu-id="0a193-117">Дополнительные сведения см. в разделе повторное [согласование подключения SChannel](renegotiating-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0a193-117">For details, see [Renegotiating an Schannel Connection](renegotiating-an-schannel-connection.md).</span></span>

<span data-ttu-id="0a193-118">После завершения использования подключения SChannel необходимо выполнить необходимую очистку.</span><span class="sxs-lookup"><span data-stu-id="0a193-118">When you have finished using an Schannel connection, you must perform the necessary cleanup.</span></span> <span data-ttu-id="0a193-119">Дополнительные сведения см. [в разделе Завершение работы подключения SChannel](shutting-down-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0a193-119">For details, see [Shutting Down an Schannel Connection](shutting-down-an-schannel-connection.md).</span></span>

<span data-ttu-id="0a193-120">Сведения о примерах, поставляемых с пакетом средств разработки программного обеспечения для платформы (SDK), демонстрирующих [*пакеты безопасности*](/windows/desktop/SecGloss/s-gly)SChannel, см. в примерах PSDK с использованием канала Schannel.</span><span class="sxs-lookup"><span data-stu-id="0a193-120">For information about samples shipped with the Platform Software Development Kit (SDK) that demonstrate the Schannel [*security package*](/windows/desktop/SecGloss/s-gly), see the PSDK samples using Schannel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a193-121">См. также</span><span class="sxs-lookup"><span data-stu-id="0a193-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a193-122">Указание шифров SChannel и стойкости шифров</span><span class="sxs-lookup"><span data-stu-id="0a193-122">Specifying Schannel Ciphers and Cipher Strengths</span></span>](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
