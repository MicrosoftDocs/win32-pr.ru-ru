---
title: Интерфейсы поставщика протокол удаленного рабочего стола
description: Интерфейсы, поддерживаемые API поставщика протокол удаленного рабочего стола.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986064"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a><span data-ttu-id="ea12f-103">Интерфейсы поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="ea12f-103">Remote Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="ea12f-104">API поставщика протокол удаленного рабочего стола поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ea12f-104">The following interfaces are supported by the Remote Desktop Protocol Provider API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ea12f-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="ea12f-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ea12f-106">**иврдспротоколконнектион**</span><span class="sxs-lookup"><span data-stu-id="ea12f-106">**IWRdsProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

<span data-ttu-id="ea12f-107">Предоставляет методы, вызываемые службой службы удаленных рабочих столов для настройки клиентского соединения.</span><span class="sxs-lookup"><span data-stu-id="ea12f-107">Exposes methods called by the Remote Desktop Services service to configure a client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-108">**иврдспротоколконнектионкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="ea12f-108">**IWRdsProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="ea12f-109">Предоставляет методы, предоставляющие сведения о состоянии клиентского соединения и выполняющие действия для клиента.</span><span class="sxs-lookup"><span data-stu-id="ea12f-109">Exposes methods that provide information about the status of a client connection and that perform actions for the client.</span></span> <span data-ttu-id="ea12f-110">Этот интерфейс реализуется службой службы удаленных рабочих столов и вызывается протоколом.</span><span class="sxs-lookup"><span data-stu-id="ea12f-110">This interface is implemented by the Remote Desktop Services service and called by the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-111">**иврдспротоколлиценсеконнектион**</span><span class="sxs-lookup"><span data-stu-id="ea12f-111">**IWRdsProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="ea12f-112">Предоставляет методы, используемые службой службы удаленных рабочих столов для выполнения подтверждения лицензирования во время последовательности подключения.</span><span class="sxs-lookup"><span data-stu-id="ea12f-112">Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-113">**иврдспротоколлистенер**</span><span class="sxs-lookup"><span data-stu-id="ea12f-113">**IWRdsProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

<span data-ttu-id="ea12f-114">Предоставляет методы, запрашивающие запуск и прекращение прослушивания протоколом запросов на подключение клиента.</span><span class="sxs-lookup"><span data-stu-id="ea12f-114">Exposes methods that request that the protocol start and stop listening for client connection requests.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-115">**иврдспротоколлистенеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="ea12f-115">**IWRdsProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="ea12f-116">Предоставляет методы, уведомляющие службу службы удаленных рабочих столов, к которой подключен клиент.</span><span class="sxs-lookup"><span data-stu-id="ea12f-116">Exposes methods that notify the Remote Desktop Services service that a client has connected.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-117">**иврдспротоколлогонеррорредиректор**</span><span class="sxs-lookup"><span data-stu-id="ea12f-117">**IWRdsProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="ea12f-118">Предоставляет методы, вызываемые службой службы удаленных рабочих столов для обновления состояния входа в систему и определения способа направления сообщений об ошибках входа в систему.</span><span class="sxs-lookup"><span data-stu-id="ea12f-118">Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-119">**иврдспротоколманажер**</span><span class="sxs-lookup"><span data-stu-id="ea12f-119">**IWRdsProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

<span data-ttu-id="ea12f-120">Предоставляет методы, которые служба службы удаленных рабочих столов использует для взаимодействия с поставщиком протокола.</span><span class="sxs-lookup"><span data-stu-id="ea12f-120">Exposes methods that the Remote Desktop Services service uses to communicate with the protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-121">**иврдспротоколсеттингс**</span><span class="sxs-lookup"><span data-stu-id="ea12f-121">**IWRdsProtocolSettings**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

<span data-ttu-id="ea12f-122">Предоставляет методы для извлечения и добавления параметров, связанных с политикой.</span><span class="sxs-lookup"><span data-stu-id="ea12f-122">Exposes methods for retrieving and adding policy-related settings.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-123">**иврдспротоколшадовкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="ea12f-123">**IWRdsProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="ea12f-124">Предоставляет методы, вызываемые протоколом, для уведомления службы службы удаленных рабочих столов о запуске или прекращении целевой стороны тени.</span><span class="sxs-lookup"><span data-stu-id="ea12f-124">Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-125">**иврдспротоколшадовконнектион**</span><span class="sxs-lookup"><span data-stu-id="ea12f-125">**IWRdsProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="ea12f-126">Предоставляет методы, уведомляющие поставщика протокола о состоянии теневого сеанса.</span><span class="sxs-lookup"><span data-stu-id="ea12f-126">Exposes methods that notify the protocol provider about the status of session shadowing.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-127">**иврдсремотефксграфиксконнектион**</span><span class="sxs-lookup"><span data-stu-id="ea12f-127">**IWRdsRemoteFXGraphicsConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

<span data-ttu-id="ea12f-128">Предоставляет методы, относящиеся к манипуляции и пониманию графики в клиентском подключении.</span><span class="sxs-lookup"><span data-stu-id="ea12f-128">Exposes methods relating to the manipulation and understanding of graphics on the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ea12f-129">Нерекомендуемые интерфейсы поставщика протокола рабочего стола</span><span class="sxs-lookup"><span data-stu-id="ea12f-129">Deprecated Desktop Protocol Provider Interfaces</span></span>](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

<span data-ttu-id="ea12f-130">Следующие интерфейсы являются устаревшими и больше не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="ea12f-130">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="ea12f-131">Для новых проектов вместо этого используйте интерфейсы интерфейсов поставщика протокол удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ea12f-131">For new projects, use the Remote Desktop Protocol Provider Interfaces interfaces instead.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ea12f-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ea12f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea12f-133">Справочник по поставщику протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="ea12f-133">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="ea12f-134">Перечисления поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="ea12f-134">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="ea12f-135">Структуры поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="ea12f-135">Remote Desktop Protocol Provider Structures</span></span>](custom-remote-protocol-structures.md)
</dt> <dt>

[<span data-ttu-id="ea12f-136">Объединения поставщиков протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="ea12f-136">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




