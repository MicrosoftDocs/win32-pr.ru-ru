---
description: Написание безопасного поставщика требует учета того, как размещается поставщик, как поставщик обрабатывает олицетворение и гарантирует, что пользователи проверяют права доступа к данным.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Защита поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701988"
---
# <a name="securing-your-provider"></a><span data-ttu-id="571ea-103">Защита поставщика</span><span class="sxs-lookup"><span data-stu-id="571ea-103">Securing Your Provider</span></span>

<span data-ttu-id="571ea-104">Написание безопасного поставщика требует учета того, как размещается поставщик, как поставщик обрабатывает олицетворение и гарантирует, что пользователи проверяют права доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="571ea-104">Writing a secure provider requires considering how the provider is hosted, how the provider handles impersonation, and ensuring that users are checked for access rights to data.</span></span> <span data-ttu-id="571ea-105">Чтобы защитить данные в пространстве имен поставщика, необходимо, чтобы данные были зашифрованы перед отправкой по сети.</span><span class="sxs-lookup"><span data-stu-id="571ea-105">You can secure the data in your provider namespace by requiring that data be encrypted authentication before sending it over a network.</span></span> <span data-ttu-id="571ea-106">Дополнительные сведения см. в разделе [требуется зашифрованное соединение с пространством имен](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="571ea-106">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="571ea-107">Если у пользователя есть **полный \_** доступ на запись в любом пространстве имен, то он может создавать подписки между пространствами имен для данных в пространстве имен, в котором пользователь ограничен.</span><span class="sxs-lookup"><span data-stu-id="571ea-107">If a user has **FULL\_WRITE** access in any namespace, then the user can create cross-namespace subscriptions for data in a namespace in which the user is restricted.</span></span> <span data-ttu-id="571ea-108">Поскольку поставщик может быть загружен в любое пространство имен и выполняться в любом контексте безопасности, поставщик должен выполнить собственные проверки доступа, чтобы убедиться, что доступ к данным или выполнение методов разрешен только полномочным пользователям.</span><span class="sxs-lookup"><span data-stu-id="571ea-108">Because a provider can be loaded into any namespace and be executing in any security context, the provider should perform its own access checks to ensure that only authorized users are allowed access to data or to execute methods.</span></span> <span data-ttu-id="571ea-109">Дополнительные сведения см. в разделе [выполнение проверок доступа](performing-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="571ea-109">For more information, see [Performing Access Checks](performing-access-checks.md).</span></span>

<span data-ttu-id="571ea-110">В следующих разделах рассматривается безопасность поставщика:</span><span class="sxs-lookup"><span data-stu-id="571ea-110">The following topics discuss provider security:</span></span>

-   [<span data-ttu-id="571ea-111">Размещение и безопасность поставщика</span><span class="sxs-lookup"><span data-stu-id="571ea-111">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
-   [<span data-ttu-id="571ea-112">Выполнение проверок доступа</span><span class="sxs-lookup"><span data-stu-id="571ea-112">Performing Access Checks</span></span>](performing-access-checks.md)
-   [<span data-ttu-id="571ea-113">Разделы реестра для управления безопасностью поставщика</span><span class="sxs-lookup"><span data-stu-id="571ea-113">Registry Keys for Controlling Provider Security</span></span>](registry-keys-for-controlling-provider-security-.md)
-   [<span data-ttu-id="571ea-114">Доступ к пространствам имен WMI</span><span class="sxs-lookup"><span data-stu-id="571ea-114">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
-   [<span data-ttu-id="571ea-115">Олицетворение клиента</span><span class="sxs-lookup"><span data-stu-id="571ea-115">Impersonating a Client</span></span>](impersonating-a-client.md)

<span data-ttu-id="571ea-116">В следующих разделах рассматривается взаимодействие клиентов и сценариев с безопасностью поставщика.</span><span class="sxs-lookup"><span data-stu-id="571ea-116">The following topics discuss how clients and scripts interact with provider security:</span></span>

-   [<span data-ttu-id="571ea-117">Настройка проверки подлинности в WMI</span><span class="sxs-lookup"><span data-stu-id="571ea-117">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
-   [<span data-ttu-id="571ea-118">Подключение между различными операционными системами</span><span class="sxs-lookup"><span data-stu-id="571ea-118">Connecting Between Different Operating Systems</span></span>](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [<span data-ttu-id="571ea-119">Настройка уровня безопасности процесса по умолчанию с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="571ea-119">Setting the Default Process Security Level Using VBScript</span></span>](setting-the-default-process-security-level-using-vbscript.md)
-   [<span data-ttu-id="571ea-120">Настройка безопасности процесса клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="571ea-120">Setting Client Application Process Security</span></span>](setting-client-application-process-security.md)

## <a name="related-topics"></a><span data-ttu-id="571ea-121">См. также</span><span class="sxs-lookup"><span data-stu-id="571ea-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="571ea-122">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="571ea-122">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="571ea-123">Использование инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="571ea-123">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
