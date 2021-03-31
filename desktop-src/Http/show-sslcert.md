---
title: show sslcert
description: Список привязок сертификатов сервера SSL и соответствующих политик сертификатов клиента для IP-адреса и порта.
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- показывать sslcert HTTP
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71c2faf370066f5ce8d5ce6a20b173a74d0f645
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104335059"
---
# <a name="show-sslcert"></a><span data-ttu-id="ab18a-104">show sslcert</span><span class="sxs-lookup"><span data-stu-id="ab18a-104">show sslcert</span></span>

<span data-ttu-id="ab18a-105">Список привязок сертификатов сервера SSL и соответствующих политик сертификатов клиента для IP-адреса и порта.</span><span class="sxs-lookup"><span data-stu-id="ab18a-105">Lists SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="ab18a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab18a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab18a-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[иппорт = \] \* \* \* IP-адрес: порт*</span><span class="sxs-lookup"><span data-stu-id="ab18a-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="ab18a-108">Указывает адрес или порт IPv4 или IPv6, для которого будут отображаться привязки SSL-сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ab18a-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be displayed.</span></span> <span data-ttu-id="ab18a-109">Не указывая иппорт, перечисляются все привязки.</span><span class="sxs-lookup"><span data-stu-id="ab18a-109">Not specifying an ipport lists all bindings.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ab18a-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="ab18a-110">Examples</span></span>

<span data-ttu-id="ab18a-111">**показывать sslcert иппорт = \[ FE80:: 1 \] : 443**</span><span class="sxs-lookup"><span data-stu-id="ab18a-111">**show sslcert ipport=\[fe80::1\]:443**</span></span>

<span data-ttu-id="ab18a-112">**show sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="ab18a-112">**show sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="ab18a-113">**show sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="ab18a-113">**show sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="ab18a-114">**показывать sslcert иппорт = \[ ::: \] 443**</span><span class="sxs-lookup"><span data-stu-id="ab18a-114">**show sslcert ipport=\[::\]:443**</span></span>

 

 




