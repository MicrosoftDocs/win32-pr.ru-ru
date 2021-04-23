---
description: Приложение должно выполнять инвентаризацию доступных для него ресурсов связи, а затем уведомлять TAPI о том, какие ресурсы будут использоваться и как они будут использоваться.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Инвентаризация ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673704"
---
# <a name="resource-inventory"></a><span data-ttu-id="0a44c-103">Инвентаризация ресурсов</span><span class="sxs-lookup"><span data-stu-id="0a44c-103">Resource Inventory</span></span>

<span data-ttu-id="0a44c-104">Приложение должно выполнять инвентаризацию доступных для него ресурсов связи, а затем уведомлять TAPI о том, какие ресурсы будут использоваться и как они будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="0a44c-104">The application must inventory the communications resources available to it, then notify TAPI about which resources it will use and how it will use them.</span></span> <span data-ttu-id="0a44c-105">Дополнительные сведения о типах ресурсов и возможностях, к которым может обращаться приложение, см. в разделе [Управление устройством](device-control.md) .</span><span class="sxs-lookup"><span data-stu-id="0a44c-105">See [Device Control](device-control.md) for additional information on the types of resources and capabilities an application might access.</span></span>

<span data-ttu-id="0a44c-106">**Интерфейс TAPI 2. x:** Приложения получают количество доступных строк при возврате [**линеинитиализикс**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="0a44c-106">**TAPI 2.x:** Applications get the number of available lines when [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) returns.</span></span> <span data-ttu-id="0a44c-107">Затем они могут выполнять [**линежетдевкапс**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) в каждой строке, [**линежетаддресскапс**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) для каждого адреса и [**линеопен**](/windows/win32/api/tapi/nf-tapi-lineopen) для каждой строки, которая будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="0a44c-107">They can then perform [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) on each line, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) for each address, and [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) for each line that will be used.</span></span>

<span data-ttu-id="0a44c-108">**Интерфейс TAPI 3. x:** Приложения используют [**адреса иттапи:: енумератеаддрессес**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) или [**иттапи:: \_ Get**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) для обнаружения доступных адресов.</span><span class="sxs-lookup"><span data-stu-id="0a44c-108">**TAPI 3.x:** Applications use [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) or [**ITTAPI::get\_Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) to discover the addresses available.</span></span> <span data-ttu-id="0a44c-109">[**Итмедиасуппорт**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) и [**итаддресскапабилитиес**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) предоставляют сведения о типах связи для каждого адреса.</span><span class="sxs-lookup"><span data-stu-id="0a44c-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) and [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) supply information on communication types possible for each address.</span></span> <span data-ttu-id="0a44c-110">При реализации поставщиком услуг [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) предоставляет приложению доступ к дополнительным сведениям и элементам управления.</span><span class="sxs-lookup"><span data-stu-id="0a44c-110">If implemented by the service provider, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) gives an application access to additional information and controls.</span></span>

 

 
