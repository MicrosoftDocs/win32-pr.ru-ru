---
title: Определение потребностей в безопасности
description: Настройка безопасности COM для приложения зависит от того, какой тип безопасности требуется приложению. Существует несколько распространенных ситуаций, которые определяют, что следует делать.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779970"
---
# <a name="determining-your-security-needs"></a><span data-ttu-id="315d0-104">Определение потребностей в безопасности</span><span class="sxs-lookup"><span data-stu-id="315d0-104">Determining Your Security Needs</span></span>

<span data-ttu-id="315d0-105">Настройка безопасности COM для приложения зависит от того, какой тип безопасности требуется приложению.</span><span class="sxs-lookup"><span data-stu-id="315d0-105">How you set up COM security for your application depends on what kind of security your application needs.</span></span> <span data-ttu-id="315d0-106">Существует несколько распространенных ситуаций, которые определяют, что следует делать.</span><span class="sxs-lookup"><span data-stu-id="315d0-106">There are several common situations that determine what you should do.</span></span>

<span data-ttu-id="315d0-107">Если вы решили использовать параметры безопасности COM по умолчанию, вам не нужно делать анисингâ "COM" обрабатывать все.</span><span class="sxs-lookup"><span data-stu-id="315d0-107">If you decide to use the COM security defaults, you do not have to do anythingâ€”COM handles it all.</span></span> <span data-ttu-id="315d0-108">Сведения о параметрах по умолчанию см. в разделе Параметры [безопасности COM по умолчанию](com-security-defaults.md).</span><span class="sxs-lookup"><span data-stu-id="315d0-108">For information on what these default settings are, see [COM Security Defaults](com-security-defaults.md).</span></span>

<span data-ttu-id="315d0-109">Кроме того, можно предотвратить удаленные вызовы к компьютеру, отключив DCOM полностью (COM между удаленными компьютерами).</span><span class="sxs-lookup"><span data-stu-id="315d0-109">You can also prevent any remote calls into your machine by disabling DCOM altogether (COM between remote computers).</span></span> <span data-ttu-id="315d0-110">Дополнительные сведения см. в разделе [Настройка безопасности System-Wide с помощью DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="315d0-110">For more information, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="315d0-111">Для устаревших или новых приложений в реестре можно задать параметры безопасности на уровне процесса.</span><span class="sxs-lookup"><span data-stu-id="315d0-111">For legacy or new applications, you can set process-wide security in the registry.</span></span> <span data-ttu-id="315d0-112">Дополнительные сведения см. [в разделе Настройка безопасности процессвиде в реестре](setting-processwide-security-through-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="315d0-112">For more information, see [Setting Processwide Security Through the Registry](setting-processwide-security-through-the-registry.md).</span></span>

<span data-ttu-id="315d0-113">Можно также переопределить параметры безопасности по умолчанию для вызовов определенных интерфейсов в процессе, установив безопасность по умолчанию для оставшейся части процесса (чтобы разрешить COM обработку общих вариантов).</span><span class="sxs-lookup"><span data-stu-id="315d0-113">You can also override default security settings for calls to certain interfaces in the process while setting default security for the remainder of the process (to allow COM to handle the general cases).</span></span> <span data-ttu-id="315d0-114">Дополнительные сведения см. в разделе [Настройка безопасности на уровне прокси интерфейса](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="315d0-114">For more information, see [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="315d0-115">В случае сложных требований безопасности вы можете управлять всей безопасностью программным способом, не разрешая COM выполнять их самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="315d0-115">For complex security requirements, you can handle all security programmatically rather than allowing COM to handle it for you.</span></span> <span data-ttu-id="315d0-116">Для этого вызовите [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы отключить автоматическую проверку подлинности, а затем Контролируйте все параметры безопасности, установив параметры безопасности для каждого интерфейса прокси.</span><span class="sxs-lookup"><span data-stu-id="315d0-116">To do this, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to disable automatic authentication, and then control all the security settings by setting security on a per-interface proxy basis.</span></span> <span data-ttu-id="315d0-117">Дополнительные сведения см. в разделе [Настройка безопасности процессвиде с помощью CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) и [Настройка безопасности на уровне прокси интерфейса](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="315d0-117">For more information, see [Setting Processwide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) and [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="315d0-118">В некоторых сценариях может потребоваться отключить безопасность полностью.</span><span class="sxs-lookup"><span data-stu-id="315d0-118">In some scenarios, you might want to turn off security completely.</span></span> <span data-ttu-id="315d0-119">Вы можете решить, что приложение не нуждается в безопасности, или вы можете отключить безопасность во время разработки, чтобы включить функции безопасности по отдельности.</span><span class="sxs-lookup"><span data-stu-id="315d0-119">You might decide that your application does not need any security, or you might want to disable security during development time so that you can enable security features individually.</span></span> <span data-ttu-id="315d0-120">Сведения об отключении безопасности COM см. в разделе Отключение [безопасности](turning-off-security.md).</span><span class="sxs-lookup"><span data-stu-id="315d0-120">To learn how to disable COM security, see [Turning Off Security](turning-off-security.md).</span></span>

<span data-ttu-id="315d0-121">Безопасность в COM зависит от служб проверки подлинности, администрируемых пакетами безопасности.</span><span class="sxs-lookup"><span data-stu-id="315d0-121">Security in COM relies on authentication services administered by security packages.</span></span> <span data-ttu-id="315d0-122">Поставщик NTLMSSP прекрасно работает для многих приложений, но не обеспечивает более надежную защиту, предоставляемую другими пакетами.</span><span class="sxs-lookup"><span data-stu-id="315d0-122">NTLMSSP works well for many applications but does not provide the more robust security offered by other packages.</span></span> <span data-ttu-id="315d0-123">Поэтому COM поддерживает пакет безопасности SChannel и протокол безопасности Kerberos V5.</span><span class="sxs-lookup"><span data-stu-id="315d0-123">Therefore, COM supports the Schannel security package and the Kerberos v5 security protocol.</span></span> <span data-ttu-id="315d0-124">Дополнительные сведения об использовании этих пакетов безопасности см. в разделе [com и пакеты безопасности](com-and-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="315d0-124">For more details on using these security packages, see [COM and Security Packages](com-and-security-packages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="315d0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="315d0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="315d0-126">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="315d0-126">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




