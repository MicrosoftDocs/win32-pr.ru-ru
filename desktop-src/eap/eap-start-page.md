---
title: Расширяемый протокол проверки подлинности
description: Протокол расширенной проверки подлинности (EAP) является стандартом, поддерживаемым несколькими компонентами системы. EAP очень важен для обеспечения безопасности беспроводной сети (802.1 X) и проводных локальных сетей, коммутируемого подключения и виртуальных частных сетей (VPN).
ms.assetid: bdbac41e-064c-445f-8f86-a6e2eff2a683
keywords:
- Расширяемый протокол проверки подлинности
- Протокол расширенной проверки подлинности, начальная страница
- EAP
- EAP см. в разделе Протокол расширенной проверки подлинности.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c79b9585363d74eb50190d0fd6355830a7087aa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789853"
---
# <a name="extensible-authentication-protocol"></a><span data-ttu-id="8a2db-108">Расширяемый протокол проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="8a2db-108">Extensible Authentication Protocol</span></span>

## <a name="purpose"></a><span data-ttu-id="8a2db-109">Назначение</span><span class="sxs-lookup"><span data-stu-id="8a2db-109">Purpose</span></span>

<span data-ttu-id="8a2db-110">Протокол расширенной проверки подлинности (EAP) является стандартом, поддерживаемым несколькими компонентами системы.</span><span class="sxs-lookup"><span data-stu-id="8a2db-110">The Extensible Authentication Protocol (EAP) is a standard supported by several system components.</span></span> <span data-ttu-id="8a2db-111">EAP очень важен для обеспечения безопасности беспроводной сети (802.1 X) и проводных локальных сетей, коммутируемого подключения и виртуальных частных сетей (VPN).</span><span class="sxs-lookup"><span data-stu-id="8a2db-111">EAP is crucial for protecting the security of wireless (802.1X) and wired LANs, Dial-up, and Virtual Private Networks (VPNs).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8a2db-112">Где применимо</span><span class="sxs-lookup"><span data-stu-id="8a2db-112">Where applicable</span></span>

<span data-ttu-id="8a2db-113">EAP улучшает предыдущие протоколы проверки подлинности, такие как протокол PAP и протокол проверки пароля (CHAP).</span><span class="sxs-lookup"><span data-stu-id="8a2db-113">EAP improves on previous authentication protocols such as Password Authentication Protocol (PAP) and Challenge Handshake Authentication Protocol (CHAP).</span></span>

<span data-ttu-id="8a2db-114">Сведения о новом методе EAP для разработки см. в статье [узел протокола расширенной проверки подлинности](../eaphost/portal.md).</span><span class="sxs-lookup"><span data-stu-id="8a2db-114">For new EAP method development, see [Extensible Authentication Protocol Host](../eaphost/portal.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8a2db-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="8a2db-115">Developer audience</span></span>

<span data-ttu-id="8a2db-116">API EAP предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="8a2db-116">The EAP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="8a2db-117">Программисты должны быть знакомы с основными понятиями сети.</span><span class="sxs-lookup"><span data-stu-id="8a2db-117">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8a2db-118">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="8a2db-118">Run-time requirements</span></span>

<span data-ttu-id="8a2db-119">Протокол EAP поддерживается на клиентских и серверных компьютерах под управлением Windows 2000 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="8a2db-119">EAP is supported on client and server computers running on  Windows 2000 and later.</span></span> <span data-ttu-id="8a2db-120">Протокол EAP также поддерживается на компьютерах под управлением Windows 2000 Server и более поздних версий, если на них запущена служба проверки подлинности в Интернете (IAS).</span><span class="sxs-lookup"><span data-stu-id="8a2db-120">EAP is also supported on computers running on Windows 2000 Server and later if they are running Internet Authentication Service (IAS).</span></span> <span data-ttu-id="8a2db-121">Дополнительные сведения о поддерживаемых операционных системах см. в разделе "требования" в документации.</span><span class="sxs-lookup"><span data-stu-id="8a2db-121">For more information about supported operating systems, see the Requirements section in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a2db-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8a2db-122">Related topics</span></span>

<dl> <span data-ttu-id="8a2db-123"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="8a2db-123"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="8a2db-124">Служба удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="8a2db-124">Remote Access Service</span></span>](/windows/desktop/RRAS/remote-access-start-page)
<span data-ttu-id="8a2db-125"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="8a2db-125"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="8a2db-126">Служба проверки подлинности в Интернете</span><span class="sxs-lookup"><span data-stu-id="8a2db-126">Internet Authentication Service</span></span>](/windows/desktop/Nps/ias-extensions)
<span data-ttu-id="8a2db-127"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="8a2db-127"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="8a2db-128">Использование расширенного протокола проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="8a2db-128">Using Extensible Authentication Protocol</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
<span data-ttu-id="8a2db-129"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="8a2db-129"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="8a2db-130">Ссылка на протокол расширенной проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="8a2db-130">Extensible Authentication Protocol Reference</span></span>](extensible-authentication-protocol-reference.md)
</dt> </dl>

 

 