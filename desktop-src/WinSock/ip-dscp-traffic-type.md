---
description: В следующей таблице описаны \_ \_ \_ параметры сокета типа трафика IP DSCP.
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651921"
---
# <a name="ip_dscp_traffic_type"></a><span data-ttu-id="65809-103">\_ \_ тип трафика DSCP \_ IP</span><span class="sxs-lookup"><span data-stu-id="65809-103">IP\_DSCP\_TRAFFIC\_TYPE</span></span>

<span data-ttu-id="65809-104">В следующей таблице описаны \_ \_ \_ параметры сокета типа трафика IP DSCP.</span><span class="sxs-lookup"><span data-stu-id="65809-104">The following table describes IP\_DSCP\_TRAFFIC\_TYPE Socket Options.</span></span>

<dl> <span data-ttu-id="65809-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_ \_ тип трафика DSCP \_ IP**</dt> </span><span class="sxs-lookup"><span data-stu-id="65809-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP\_DSCP\_TRAFFIC\_TYPE**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="65809-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="65809-106">Option</span></span>              | <span data-ttu-id="65809-107">Получить</span><span class="sxs-lookup"><span data-stu-id="65809-107">Get</span></span> | <span data-ttu-id="65809-108">Присвойте параметру</span><span class="sxs-lookup"><span data-stu-id="65809-108">Set</span></span> | <span data-ttu-id="65809-109">Тип оптвал</span><span class="sxs-lookup"><span data-stu-id="65809-109">Optval Type</span></span> | <span data-ttu-id="65809-110">Описание</span><span class="sxs-lookup"><span data-stu-id="65809-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65809-111">\_тип трафика \_ DSCP</span><span class="sxs-lookup"><span data-stu-id="65809-111">DSCP\_TRAFFIC\_TYPE</span></span> | <span data-ttu-id="65809-112">Да</span><span class="sxs-lookup"><span data-stu-id="65809-112">Yes</span></span> | <span data-ttu-id="65809-113">Да</span><span class="sxs-lookup"><span data-stu-id="65809-113">Yes</span></span> | <span data-ttu-id="65809-114">DWORD</span><span class="sxs-lookup"><span data-stu-id="65809-114">DWORD</span></span>       | <span data-ttu-id="65809-115">Если задать для этого параметра значения, определенные **в \_ \_ типе трафика DSCP**, приложение сможет потребовать от своих сетевых пакетов обрабатываться в соответствии с типом запрашиваемой службы.</span><span class="sxs-lookup"><span data-stu-id="65809-115">By setting this value to values defined in **DSCP\_TRAFFIC\_TYPE**, an application will be able to ask its network packets to be treated according to the type of service being requested.</span></span> <span data-ttu-id="65809-116">Аналогичные вызовы [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) можно использовать для получения текущего значения для типа трафика, запрошенного на данном сокете.</span><span class="sxs-lookup"><span data-stu-id="65809-116">Similarly calls to [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) can be used to obtain the current setting for the type of traffic requested on the given socket</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65809-117">Требования</span><span class="sxs-lookup"><span data-stu-id="65809-117">Requirements</span></span>



| <span data-ttu-id="65809-118">Требование</span><span class="sxs-lookup"><span data-stu-id="65809-118">Requirement</span></span> | <span data-ttu-id="65809-119">Значение</span><span class="sxs-lookup"><span data-stu-id="65809-119">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="65809-120">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="65809-120">End of client support</span></span><br/> | <span data-ttu-id="65809-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="65809-121">Windows 10</span></span><br/>                                                          |
| <span data-ttu-id="65809-122">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="65809-122">End of server support</span></span><br/> | <span data-ttu-id="65809-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="65809-123">Windows Server 2016</span></span><br/>                                                 |
| <span data-ttu-id="65809-124">Header</span><span class="sxs-lookup"><span data-stu-id="65809-124">Header</span></span><br/>                | <dl> <span data-ttu-id="65809-125"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="65809-125"><dt>N/A</dt></span></span> </dl> |



 

 




