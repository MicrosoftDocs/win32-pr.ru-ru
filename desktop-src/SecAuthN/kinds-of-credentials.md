---
description: Описание двух типов учетных данных, с которыми работает API управления учетными данными.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Виды учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998679"
---
# <a name="kinds-of-credentials"></a><span data-ttu-id="5ddb8-103">Виды учетных данных</span><span class="sxs-lookup"><span data-stu-id="5ddb8-103">Kinds of Credentials</span></span>

<span data-ttu-id="5ddb8-104">API управления учетными данными работает с двумя видами учетных данных:</span><span class="sxs-lookup"><span data-stu-id="5ddb8-104">The Credentials Management API works with two kinds of credentials:</span></span>

-   [<span data-ttu-id="5ddb8-105">Учетные данные домена</span><span class="sxs-lookup"><span data-stu-id="5ddb8-105">Domain Credentials</span></span>](#domain-credentials)
-   [<span data-ttu-id="5ddb8-106">Общие учетные данные</span><span class="sxs-lookup"><span data-stu-id="5ddb8-106">Generic Credentials</span></span>](#generic-credentials)

## <a name="domain-credentials"></a><span data-ttu-id="5ddb8-107">Учетные данные домена</span><span class="sxs-lookup"><span data-stu-id="5ddb8-107">Domain Credentials</span></span>

<span data-ttu-id="5ddb8-108">Учетные данные домена используются операционной системой и проходят проверку подлинности локальным администратором безопасности (LSA).</span><span class="sxs-lookup"><span data-stu-id="5ddb8-108">Domain credentials are used by the operating system and authenticated by the Local Security Authority (LSA).</span></span> <span data-ttu-id="5ddb8-109">Как правило, учетные данные домена устанавливаются для пользователя, если зарегистрированный пакет безопасности, например протокол Kerberos, выполняет проверку подлинности данных входа, предоставленных пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-109">Typically, domain credentials are established for a user when a registered security package, such as the Kerberos protocol, authenticates logon data that is provided by the user.</span></span> <span data-ttu-id="5ddb8-110">Учетные данные для входа в систему кэшируются операционной системой, поэтому единый вход предоставляет пользователю доступ к различным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-110">The logon credentials are cached by the operating system so that a single sign-on gives the user access to many different resources.</span></span> <span data-ttu-id="5ddb8-111">Например, сетевые подключения могут выполняться прозрачно, и доступ к защищенным системным объектам может быть предоставлен на основе учетных данных домена пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-111">For example, network connections can occur transparently, and access to protected system objects can be granted based on the user's cached domain credentials.</span></span>

<span data-ttu-id="5ddb8-112">Функции управления учетными данными предоставляют механизм, с помощью которого приложения запрашивают у пользователя учетные данные домена после входа пользователя в систему и для того, чтобы операционная система выполнила проверку подлинности данных, предоставленных пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-112">Credentials Management functions provide a mechanism for applications to prompt a user for domain credentials after the user logs on, and to have the operating system authenticate the information that is provided by the user.</span></span>

<span data-ttu-id="5ddb8-113">Секретная часть учетных данных домена защищена операционной системой.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-113">The secret part of domain credentials, the password, is protected by the operating system.</span></span> <span data-ttu-id="5ddb8-114">Только код, выполняющийся внутри процесса с LSA, может считывать и записывать учетные данные домена.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-114">Only code running in-process with the LSA can read and write domain credentials.</span></span> <span data-ttu-id="5ddb8-115">Приложения ограничены записью учетных данных домена.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-115">Applications are limited to writing domain credentials.</span></span>

<span data-ttu-id="5ddb8-116">Windows поддерживает расширенное использование учетных данных смарт-карты и сертификата.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-116">Windows supports expanded use of smart card and certificate credentials.</span></span> <span data-ttu-id="5ddb8-117">Чтобы обеспечить безопасность, API управления учетными данными никогда не сохраняет на компьютере ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-117">To help ensure security, the Credentials Management API never stores the smart card PIN on the computer.</span></span>

## <a name="generic-credentials"></a><span data-ttu-id="5ddb8-118">Общие учетные данные</span><span class="sxs-lookup"><span data-stu-id="5ddb8-118">Generic Credentials</span></span>

<span data-ttu-id="5ddb8-119">Универсальные учетные данные определяются и проходят проверку подлинности приложениями, которые управляют авторизацией и безопасностью напрямую, а не делегируя эти задачи операционной системе.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-119">Generic credentials are defined and authenticated by applications that manage authorization and security directly instead of delegating these tasks to the operating system.</span></span> <span data-ttu-id="5ddb8-120">Например, приложение может потребовать от пользователей ввести имя пользователя и пароль, предоставленные приложением, или создать [*сертификат*](../secgloss/c-gly.md) для доступа к веб-сайту.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-120">For example, an application can require users to enter a user name and password provided by the application or to produce a [*certificate*](../secgloss/c-gly.md) to access a website.</span></span>

<span data-ttu-id="5ddb8-121">Приложения используют функции управления учетными данными, чтобы запрашивать у пользователей определяемые приложением, универсальные учетные данные, такие как имя пользователя, сертификат, смарт-карта или пароль.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-121">Applications use Credentials Management functions to prompt users for application-defined, generic, credential information, such as user name, certificate, smart card, or password.</span></span> <span data-ttu-id="5ddb8-122">Данные, вводимых пользователем, возвращаются приложению для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-122">The information entered by the user is returned to the application for authentication.</span></span>

<span data-ttu-id="5ddb8-123">Управление учетными данными обеспечивает настраиваемое управление кэшем и долгосрочное хранение общих учетных данных.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-123">Credentials Management provides customizable cache management and long-term storage for generic credentials.</span></span> <span data-ttu-id="5ddb8-124">Универсальные учетные данные могут быть прочитаны и записаны пользовательскими процессами.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-124">Generic credentials can be read and written by user processes.</span></span>

 

 
