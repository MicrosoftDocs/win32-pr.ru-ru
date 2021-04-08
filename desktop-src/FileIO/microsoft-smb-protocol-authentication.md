---
description: Модель безопасности, используемая в протоколе SMB Microsoft, идентична той, которая используется другими вариантами SMB, и состоит из двух уровней безопасности&\# 8212; пользователя и общего ресурса.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Проверка подлинности протокола SMB (Майкрософт)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897238"
---
# <a name="microsoft-smb-protocol-authentication"></a><span data-ttu-id="eee90-103">Проверка подлинности протокола SMB (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="eee90-103">Microsoft SMB Protocol Authentication</span></span>

<span data-ttu-id="eee90-104">Модель безопасности, используемая в протоколе SMB Microsoft, идентична той, которая используется другими вариантами SMB, и состоит из двух уровней безопасности — пользователя и общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="eee90-104">The security model used in Microsoft SMB Protocol is identical to the one used by other variants of SMB, and consists of two levels of security—user and share.</span></span> <span data-ttu-id="eee90-105">Общий ресурс — это файл, каталог или принтер, доступ к которому могут получить клиенты протокола Microsoft SMB.</span><span class="sxs-lookup"><span data-stu-id="eee90-105">A share is a file, directory, or printer that can be accessed by Microsoft SMB Protocol clients.</span></span>

<span data-ttu-id="eee90-106">Проверка подлинности на уровне пользователя означает, что клиент, пытающийся получить доступ к общей папке на сервере, должен предоставить имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="eee90-106">User-level authentication indicates that the client attempting to access a share on a server must provide a user name and password.</span></span> <span data-ttu-id="eee90-107">При проверке подлинности пользователь может получить доступ ко всем общим папкам на сервере, не защищенным с помощью безопасности на уровне общего доступа.</span><span class="sxs-lookup"><span data-stu-id="eee90-107">When authenticated, the user can then access all shares on a server not also protected by share-level security.</span></span> <span data-ttu-id="eee90-108">Этот уровень безопасности позволяет системным администраторам определять, какие пользователи и группы имеют доступ к общей папке.</span><span class="sxs-lookup"><span data-stu-id="eee90-108">This security level allows system administrators to specifically determine which users and groups can access a share.</span></span>

<span data-ttu-id="eee90-109">Проверка подлинности на уровне общего ресурса означает, что доступ к общей папке управляется только паролем, назначенным этому общему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="eee90-109">Share-level authentication indicates that access to a share is controlled by a password assigned to that share only.</span></span> <span data-ttu-id="eee90-110">В отличие от безопасности на уровне пользователя, для этого уровня безопасности не требуется имя пользователя для проверки подлинности и удостоверение пользователя не устанавливается.</span><span class="sxs-lookup"><span data-stu-id="eee90-110">Unlike user-level security, this security level does not require a user name for authentication and no user identity is established.</span></span>

<span data-ttu-id="eee90-111">В обоих уровнях безопасности пароль шифруется перед отправкой на сервер.</span><span class="sxs-lookup"><span data-stu-id="eee90-111">Under both of these security levels, the password is encrypted before it is sent to the server.</span></span> <span data-ttu-id="eee90-112">Протоколы [NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) и более ранних версий диспетчера LAN (LM) поддерживаются с помощью протокола Microsoft SMB.</span><span class="sxs-lookup"><span data-stu-id="eee90-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) and the older LAN Manager (LM) encryption are supported by Microsoft SMB Protocol.</span></span> <span data-ttu-id="eee90-113">Оба метода шифрования используют проверку подлинности типа "запрос-ответ", где сервер отправляет клиенту случайную строку, а клиент Возвращает вычисленную строку ответа, которая подтверждает, что у клиента достаточно учетных данных для доступа.</span><span class="sxs-lookup"><span data-stu-id="eee90-113">Both encryption methods use challenge-response authentication, where the server sends the client a random string and the client returns a computed response string that proves the client has sufficient credentials for access.</span></span>

 

 
