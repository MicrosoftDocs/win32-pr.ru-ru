---
title: Узел протокола расширяемой проверки подлинности
description: Сведения о узле протокола расширенной проверки подлинности (EAP). См. требования к времени выполнения и Просмотр дополнительных доступных ресурсов.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104134827"
---
# <a name="extensible-authentication-protocol-host"></a><span data-ttu-id="ed9b4-104">Узел протокола расширяемой проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="ed9b4-104">Extensible Authentication Protocol Host</span></span>

## <a name="purpose"></a><span data-ttu-id="ed9b4-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="ed9b4-105">Purpose</span></span>


<span data-ttu-id="ed9b4-106">EAPHost — это сетевой компонент Microsoft Windows, предоставляющий инфраструктуру расширенной проверки подлинности (EAP) для проверки подлинности реализаций протоколов, таких как [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) и [точка-точка](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span><span class="sxs-lookup"><span data-stu-id="ed9b4-106">EAPHost is a Microsoft Windows Networking component that provides an Extensible Authentication Protocol (EAP) infrastructure for the authentication of "supplicant" protocol implementations such as [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) and [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span></span> <span data-ttu-id="ed9b4-107">Она также позволяет выполнять проверку подлинности с помощью таких технологий, как сервер политики сети (NPS) (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="ed9b4-107">It also allows for authentication with "authenticator" technologies such as the Microsoft network policy server (NPS).</span></span> <span data-ttu-id="ed9b4-108">В отличие от предыдущего сервера IAS ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS поддерживает [защиту доступа к сети](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span><span class="sxs-lookup"><span data-stu-id="ed9b4-108">Unlike the previous IAS Server ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS supports [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span></span>


<span data-ttu-id="ed9b4-109">API-интерфейсы EAPHost позволяют приложениям проходить проверку подлинности с помощью службы EAPHost и предоставлять шаблон для разработки согласованных методов проверки подлинности для использования с EAPHost.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-109">The EAPHost APIs enable applications to authenticate using the EAPHost service, and provide a template for the development of conformant authentication methods for use with EAPHost.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ed9b4-110">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="ed9b4-110">Run-time requirements</span></span>

<span data-ttu-id="ed9b4-111">API-интерфейсы EAPHost поддерживаются только в Windows Vista и более поздних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-111">The EAPHost APIs are supported only in Windows Vista and later operating systems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed9b4-112">См. также</span><span class="sxs-lookup"><span data-stu-id="ed9b4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed9b4-113">Об EAPHost</span><span class="sxs-lookup"><span data-stu-id="ed9b4-113">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="ed9b4-114">Использование EAPHost</span><span class="sxs-lookup"><span data-stu-id="ed9b4-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="ed9b4-115">Справочник по API EAPHost</span><span class="sxs-lookup"><span data-stu-id="ed9b4-115">EAPHost API Reference</span></span>](eaphost-api-reference.md)
</dt> </dl>

 

 