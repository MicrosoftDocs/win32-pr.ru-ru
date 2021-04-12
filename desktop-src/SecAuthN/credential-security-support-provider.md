---
description: Протокол CredSSP — это поставщик поддержки безопасности, реализуемый с помощью интерфейса поставщика поддержки безопасности (SSPI).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Поставщик поддержки безопасности учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263470"
---
# <a name="credential-security-support-provider"></a><span data-ttu-id="c5358-103">Поставщик поддержки безопасности учетных данных</span><span class="sxs-lookup"><span data-stu-id="c5358-103">Credential Security Support Provider</span></span>

<span data-ttu-id="c5358-104">Протокол CredSSP — это поставщик поддержки безопасности, реализуемый с помощью интерфейса поставщика поддержки безопасности ([SSPI](sspi.md)).</span><span class="sxs-lookup"><span data-stu-id="c5358-104">The Credential Security Support Provider protocol (CredSSP) is a Security Support Provider that is implemented by using the Security Support Provider Interface ([SSPI](sspi.md)).</span></span> <span data-ttu-id="c5358-105">CredSSP позволяет приложению делегировать учетные данные пользователя от клиента целевому серверу для удаленной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c5358-105">CredSSP lets an application delegate the user's credentials from the client to the target server for remote authentication.</span></span> <span data-ttu-id="c5358-106">CredSSP предоставляет зашифрованный канал [протокола безопасности транспортного уровня](transport-layer-security-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="c5358-106">CredSSP provides an encrypted [Transport Layer Security Protocol](transport-layer-security-protocol.md) channel.</span></span> <span data-ttu-id="c5358-107">Проверка подлинности клиента осуществляется по зашифрованному каналу с помощью простого и защищенного протокола Negotiate (SPNEGO) с [Microsoft Kerberos](microsoft-kerberos.md) или [Microsoft NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="c5358-107">The client is authenticated over the encrypted channel by using the Simple and Protected Negotiate (SPNEGO) protocol with either [Microsoft Kerberos](microsoft-kerberos.md) or [Microsoft NTLM](microsoft-ntlm.md).</span></span>

> [!Caution]  
> <span data-ttu-id="c5358-108">Это не ограниченное делегирование.</span><span class="sxs-lookup"><span data-stu-id="c5358-108">This is not constrained delegation.</span></span> <span data-ttu-id="c5358-109">CredSSP передает полные учетные данные пользователя на сервер без каких бы то ни было ограничений.</span><span class="sxs-lookup"><span data-stu-id="c5358-109">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="c5358-110">Сведения о программе SPNEGO см. в разделе [Microsoft Negotiate](microsoft-negotiate.md).</span><span class="sxs-lookup"><span data-stu-id="c5358-110">For information about SPNEGO, see [Microsoft Negotiate](microsoft-negotiate.md).</span></span>

<span data-ttu-id="c5358-111">После проверки подлинности клиента и сервера клиент передает учетные данные пользователя на сервер.</span><span class="sxs-lookup"><span data-stu-id="c5358-111">After the client and server are authenticated, the client passes the user's credentials to the server.</span></span> <span data-ttu-id="c5358-112">Учетные данные дважды шифруются в ключах сеанса SPNEGO и TLS.</span><span class="sxs-lookup"><span data-stu-id="c5358-112">The credentials are doubly encrypted under the SPNEGO and TLS session keys.</span></span> <span data-ttu-id="c5358-113">CredSSP поддерживает вход на основе пароля, а также вход с помощью смарт-карты на основе как [*X. 509*](/windows/desktop/SecGloss/x-gly) , так и PKINIT.</span><span class="sxs-lookup"><span data-stu-id="c5358-113">CredSSP supports password-based logon as well as smart card logon based on both [*X.509*](/windows/desktop/SecGloss/x-gly) and PKINIT.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5358-114">CredSSP не поддерживает клиенты WOW64.</span><span class="sxs-lookup"><span data-stu-id="c5358-114">CredSSP does not support Wow64 clients.</span></span>

 

<span data-ttu-id="c5358-115">Дополнительные сведения о CredSSP см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="c5358-115">For more information about CredSSP, see the following topics.</span></span>



| <span data-ttu-id="c5358-116">Раздел</span><span class="sxs-lookup"><span data-stu-id="c5358-116">Topic</span></span>                                                                         | <span data-ttu-id="c5358-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c5358-117">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5358-118">Параметры групповая политика CredSSP</span><span class="sxs-lookup"><span data-stu-id="c5358-118">CredSSP Group Policy Settings</span></span>](credssp-group-policy-settings.md)<br/> | <span data-ttu-id="c5358-119">Делегирование учетных данных CredSSP можно контролировать с помощью параметров групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c5358-119">Delegation of credentials by CredSSP can be controlled by using group policy settings.</span></span><br/> |



 

 

