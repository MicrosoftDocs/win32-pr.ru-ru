---
title: Структуры служб развертывания Windows
description: В службах развертывания Windows используются следующие структуры.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20f5b369a2bbb5d68bd77dce1751e09fed2e6b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068472"
---
# <a name="windows-deployment-services-structures"></a><span data-ttu-id="2daa4-103">Структуры служб развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="2daa4-103">Windows Deployment Services Structures</span></span>

<span data-ttu-id="2daa4-104">В службах развертывания Windows используются следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="2daa4-104">The following structures are used with Windows Deployment Services.</span></span>



| <span data-ttu-id="2daa4-105">Структура</span><span class="sxs-lookup"><span data-stu-id="2daa4-105">Structure</span></span>                                                                         | <span data-ttu-id="2daa4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="2daa4-106">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2daa4-107">**PXE- \_ адрес**</span><span class="sxs-lookup"><span data-stu-id="2daa4-107">**PXE\_ADDRESS**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | <span data-ttu-id="2daa4-108">Указывает сетевой адрес пакета.</span><span class="sxs-lookup"><span data-stu-id="2daa4-108">Specifies the network address for a packet.</span></span>                                                                        |
| [<span data-ttu-id="2daa4-109">**\_сообщение DHCP \_ PXE**</span><span class="sxs-lookup"><span data-stu-id="2daa4-109">**PXE\_DHCP\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | <span data-ttu-id="2daa4-110">Эта структура используется с API-сервером PXE служб развертывания Windows.</span><span class="sxs-lookup"><span data-stu-id="2daa4-110">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="2daa4-111">**\_параметр PXE DHCP \_**</span><span class="sxs-lookup"><span data-stu-id="2daa4-111">**PXE\_DHCP\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | <span data-ttu-id="2daa4-112">Эта структура используется с API-сервером PXE служб развертывания Windows.</span><span class="sxs-lookup"><span data-stu-id="2daa4-112">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="2daa4-113">**\_поставщик PXE**</span><span class="sxs-lookup"><span data-stu-id="2daa4-113">**PXE\_PROVIDER**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | <span data-ttu-id="2daa4-114">Описывает поставщик.</span><span class="sxs-lookup"><span data-stu-id="2daa4-114">Describes a provider.</span></span>                                                                                              |
| [<span data-ttu-id="2daa4-115">**\_cred CLI \_ WDS**</span><span class="sxs-lookup"><span data-stu-id="2daa4-115">**WDS\_CLI\_CRED**</span></span>](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | <span data-ttu-id="2daa4-116">Содержит учетные данные, используемые для авторизации сеанса клиента.</span><span class="sxs-lookup"><span data-stu-id="2daa4-116">Contains credentials used to authorize a client session.</span></span>                                                           |
| [<span data-ttu-id="2daa4-117">**\_запрос WDS транспортклиент \_**</span><span class="sxs-lookup"><span data-stu-id="2daa4-117">**WDS\_TRANSPORTCLIENT\_REQUEST**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | <span data-ttu-id="2daa4-118">Используется функцией [**вдстранспортклиентстартсессион**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .</span><span class="sxs-lookup"><span data-stu-id="2daa4-118">Used by the [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) function.</span></span>                     |
| [<span data-ttu-id="2daa4-119">**\_сведения о сеансе транспортклиент \_**</span><span class="sxs-lookup"><span data-stu-id="2daa4-119">**TRANSPORTCLIENT\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | <span data-ttu-id="2daa4-120">Используется функцией обратного вызова [*PFN \_ вдстранспортклиентсессионстартекс*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) .</span><span class="sxs-lookup"><span data-stu-id="2daa4-120">Used by the [*PFN\_WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) callback function.</span></span> |
| [<span data-ttu-id="2daa4-121">**\_ \_ параметры инициализации WDS \_ транспортпровидер**</span><span class="sxs-lookup"><span data-stu-id="2daa4-121">**WDS\_TRANSPORTPROVIDER\_INIT\_PARAMS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | <span data-ttu-id="2daa4-122">Используется функцией обратного вызова [**вдстранспортпровидеринитиализе**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="2daa4-122">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |
| [<span data-ttu-id="2daa4-123">**\_Параметры ТРАНСПОРТПРОВИДЕР \_ WDS**</span><span class="sxs-lookup"><span data-stu-id="2daa4-123">**WDS\_TRANSPORTPROVIDER\_SETTINGS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | <span data-ttu-id="2daa4-124">Используется функцией обратного вызова [**вдстранспортпровидеринитиализе**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="2daa4-124">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |



 

<span data-ttu-id="2daa4-125">Доступны следующие возможности, начиная с Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2daa4-125">The following is available beginning with Windows 8 and Windows Server 2012.</span></span>

| <span data-ttu-id="2daa4-126">Структура</span><span class="sxs-lookup"><span data-stu-id="2daa4-126">Structure</span></span>                                          | <span data-ttu-id="2daa4-127">Описание</span><span class="sxs-lookup"><span data-stu-id="2daa4-127">Description</span></span>                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="2daa4-128">**PXE \_ , \_ параметр DHCPv6**</span><span class="sxs-lookup"><span data-stu-id="2daa4-128">**PXE\_DHCPV6\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | <span data-ttu-id="2daa4-129">Используется с API PXE-сервера служб развертывания Windows.</span><span class="sxs-lookup"><span data-stu-id="2daa4-129">Used with the Windows Deployment Services PXE Server API.</span></span> |
| [<span data-ttu-id="2daa4-130">**\_Сообщение DHCPv6 \_ PXE**</span><span class="sxs-lookup"><span data-stu-id="2daa4-130">**PXE\_DHCPV6\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | <span data-ttu-id="2daa4-131">Сообщение DHCPV6.</span><span class="sxs-lookup"><span data-stu-id="2daa4-131">A DHCPV6 message.</span></span>                                         |



 

 

 




