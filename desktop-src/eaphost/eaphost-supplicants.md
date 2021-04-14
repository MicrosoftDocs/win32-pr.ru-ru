---
title: EAPHost отправителей запросов
description: Сведения о поведении EAPHost отправителей запросов. Дополнительные сведения см. в разделах "как настроить вызывающий объект, указав конфигурацию метода EAP в EAPHost".
ms.assetid: 843f3ada-9694-4d96-b835-41d0ccf24b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc64213f0ac0e64f1512d098dd2f5d1aabc49e65
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104414284"
---
# <a name="eaphost-supplicants"></a><span data-ttu-id="e7546-104">EAPHost отправителей запросов</span><span class="sxs-lookup"><span data-stu-id="e7546-104">EAPHost Supplicants</span></span>

<span data-ttu-id="e7546-105">В этом разделе описывается поведение EAPHost отправителей запросов.</span><span class="sxs-lookup"><span data-stu-id="e7546-105">This section describes the behavior of EAPHost supplicants.</span></span>



| <span data-ttu-id="e7546-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="e7546-106">Topic</span></span>                                                                                                                    | <span data-ttu-id="e7546-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e7546-107">Description</span></span>                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7546-108">Настройка пользовательского интерфейса метода EAP</span><span class="sxs-lookup"><span data-stu-id="e7546-108">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)                               | <span data-ttu-id="e7546-109">Описание настройки запрашивающей стороны путем предоставления конфигурации метода EAP для EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e7546-109">Explains how to configure the supplicant by supplying an EAP method configuration to EAPHost.</span></span>                                                                                                                                            |
| [<span data-ttu-id="e7546-110">Включение групповая политика</span><span class="sxs-lookup"><span data-stu-id="e7546-110">Enabling Group Policy</span></span>](enabling-group-policy.md)                                                                       | <span data-ttu-id="e7546-111">В этой статье объясняется, как настроить этот метод, включив групповую политику.</span><span class="sxs-lookup"><span data-stu-id="e7546-111">Explains how to configure the supplicant by enabling group policy.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="e7546-112">Реализация поддержки NAP In-Band для методов EAP</span><span class="sxs-lookup"><span data-stu-id="e7546-112">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)                                     | <span data-ttu-id="e7546-113">Объясняет, как реализовать внутреннюю поддержку NAP для методов EAP, которые поддерживают передачу объектов типа length-value (ТЛВС).</span><span class="sxs-lookup"><span data-stu-id="e7546-113">Explains how to implement in-band NAP support for EAP methods that support the transmission of type-length-value objects (TLVs).</span></span> <span data-ttu-id="e7546-114">Если включена поддержка NAP в аппаратном контроллере, пакеты NAP передаются внутри пакетов методов EAP.</span><span class="sxs-lookup"><span data-stu-id="e7546-114">When in-band NAP support is enabled, NAP packets are transported inside EAP method packets.</span></span>             |
| [<span data-ttu-id="e7546-115">Реализация поддержки NAP для методов EAP</span><span class="sxs-lookup"><span data-stu-id="e7546-115">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)                                         | <span data-ttu-id="e7546-116">Объясняет, как реализовать NAP для запрашивающего устройства EAPHost.</span><span class="sxs-lookup"><span data-stu-id="e7546-116">Explains how to implement NAP for an EAPHost supplicant.</span></span> <span data-ttu-id="e7546-117">В Windows Vista и Windows Server 2008 клиент принудительной защиты доступа к сети (NAP EC) доступен для подключений с проверкой подлинности [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="e7546-117">In Windows Vista and Windows Server 2008 a NAP Enforcement Client (NAP EC) is available for [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authenticated connections.</span></span> |
| [<span data-ttu-id="e7546-118">Передача данных между запрашивающим и методами EAP</span><span class="sxs-lookup"><span data-stu-id="e7546-118">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md) | <span data-ttu-id="e7546-119">Описывает, как можно обмениваться данными между отправителей запросов и методами EAP с помощью атрибутов EAP.</span><span class="sxs-lookup"><span data-stu-id="e7546-119">Describes how data can be exchanged between supplicants and EAP methods using EAP attributes.</span></span>                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="e7546-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e7546-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7546-121">Об EAPHost</span><span class="sxs-lookup"><span data-stu-id="e7546-121">About EAPHost</span></span>](about-eap-host.md)
</dt> </dl>

 

 