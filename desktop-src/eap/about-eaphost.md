---
title: Сведения о связи EAP и EAPHost
description: Описывает отношение между протоколом EAP и узлом протокола расширяемой проверки подлинности.
ms.assetid: 7f585fc6-71ed-4a64-88a7-6acb1550e825
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c888a6e21992b95ea10f83175c5766246b7aaf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104273991"
---
# <a name="learn-about-the-eap-and-eaphost-relationship"></a><span data-ttu-id="6aeb0-103">Сведения о связи EAP и EAPHost</span><span class="sxs-lookup"><span data-stu-id="6aeb0-103">Learn about the EAP and EAPHost relationship</span></span>

<span data-ttu-id="6aeb0-104">В этом разделе описывается отношение между протоколом EAP и узлом протокола расширяемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="6aeb0-104">This topic describes the relationship between the Extensible Authentication Protocol (EAP) and Extensible Authentication Protocol Host.</span></span> <span data-ttu-id="6aeb0-105">Сведения о новом методе EAP для разработки см. в статье [узел протокола расширенной проверки подлинности](../eaphost/portal.md).</span><span class="sxs-lookup"><span data-stu-id="6aeb0-105">For new EAP method development, see [Extensible Authentication Protocol Host](../eaphost/portal.md).</span></span>

## <a name="eaphost-framework"></a><span data-ttu-id="6aeb0-106">Платформа EAPHost</span><span class="sxs-lookup"><span data-stu-id="6aeb0-106">EAPHost Framework</span></span>

<span data-ttu-id="6aeb0-107">Архитектура EAPHost считается платформой для EAP по двум причинам.</span><span class="sxs-lookup"><span data-stu-id="6aeb0-107">EAPHost is considered to be a framework for EAP for two reasons.</span></span>

-   <span data-ttu-id="6aeb0-108">EAPHost — это компонент инфраструктуры Windows, в котором размещены подключаемые модули EAP.</span><span class="sxs-lookup"><span data-stu-id="6aeb0-108">EAPHost is a Windows infrastructure component that hosts the EAP plug-ins</span></span>
-   <span data-ttu-id="6aeb0-109">EAPHost реализует протокол EAP согласно [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span><span class="sxs-lookup"><span data-stu-id="6aeb0-109">EAPHost implements the EAP protocol as per [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span></span> <span data-ttu-id="6aeb0-110">Проверка подлинности EAP состоит из протокола EAP в соответствии с [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063)и особенностей протокола EAP.</span><span class="sxs-lookup"><span data-stu-id="6aeb0-110">An EAP authentication consists of the EAP protocol as per [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063), and the EAP method-specific aspects of the protocol.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6aeb0-111">См. также</span><span class="sxs-lookup"><span data-stu-id="6aeb0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aeb0-112">О протоколах EAP и EAPHost</span><span class="sxs-lookup"><span data-stu-id="6aeb0-112">About EAP and EAPHost</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 
