---
title: Структура IP_NETWORK (RTM. h)
description: Структура IP- \_ сети описывает IP-адрес сети.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- RAS структуры IP_NETWORK
- RAS — указатель структуры PIP_NETWORK
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803010"
---
# <a name="ip_network-structure"></a><span data-ttu-id="68a77-105">Структура IP- \_ сети</span><span class="sxs-lookup"><span data-stu-id="68a77-105">IP\_NETWORK structure</span></span>

<span data-ttu-id="68a77-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="68a77-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="68a77-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="68a77-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="68a77-108">Структура **IP- \_ сети** описывает IP-адрес сети.</span><span class="sxs-lookup"><span data-stu-id="68a77-108">The **IP\_NETWORK** structure describes an IP network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a77-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68a77-109">Syntax</span></span>


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a><span data-ttu-id="68a77-110">Члены</span><span class="sxs-lookup"><span data-stu-id="68a77-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="68a77-111">**N \_ нетнумбер**</span><span class="sxs-lookup"><span data-stu-id="68a77-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="68a77-112">Указывает номер IP-сети, выраженный в виде IP-адреса в порядке байтов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="68a77-112">Specifies the IP network number expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="68a77-113">**N \_ Маска сети**</span><span class="sxs-lookup"><span data-stu-id="68a77-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="68a77-114">Указывает маску сети.</span><span class="sxs-lookup"><span data-stu-id="68a77-114">Specifies the network mask.</span></span> <span data-ttu-id="68a77-115">Примените эту маску к IP-адресу, чтобы извлечь сетевой адрес.</span><span class="sxs-lookup"><span data-stu-id="68a77-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="68a77-116">Маска сети находится в порядке байтов на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="68a77-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68a77-117">Требования</span><span class="sxs-lookup"><span data-stu-id="68a77-117">Requirements</span></span>



| <span data-ttu-id="68a77-118">Требование</span><span class="sxs-lookup"><span data-stu-id="68a77-118">Requirement</span></span> | <span data-ttu-id="68a77-119">Значение</span><span class="sxs-lookup"><span data-stu-id="68a77-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="68a77-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68a77-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68a77-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="68a77-121">None supported</span></span><br/>                                                        |
| <span data-ttu-id="68a77-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68a77-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68a77-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68a77-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="68a77-124">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="68a77-124">End of server support</span></span><br/>    | <span data-ttu-id="68a77-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68a77-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="68a77-126">Header</span><span class="sxs-lookup"><span data-stu-id="68a77-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68a77-127"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="68a77-127"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a77-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68a77-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a77-129">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="68a77-129">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="68a77-130">Структуры диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="68a77-130">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="68a77-131">**Окончательная версия \_ IP- \_ маршрута**</span><span class="sxs-lookup"><span data-stu-id="68a77-131">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





