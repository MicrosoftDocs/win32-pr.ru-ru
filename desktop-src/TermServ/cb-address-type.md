---
title: Перечисление CB_ADDRESS_TYPE (Кбклиент. h)
description: Указывает тип адреса.
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- Перечисление CB_ADDRESS_TYPE службы удаленных рабочих столов
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ecf17cea6ffc19743868b266236738839f9f917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801589"
---
# <a name="cb_address_type-enumeration"></a><span data-ttu-id="5178e-104">\_ \_ Перечисление типов адресов CB</span><span class="sxs-lookup"><span data-stu-id="5178e-104">CB\_ADDRESS\_TYPE enumeration</span></span>

<span data-ttu-id="5178e-105">Указывает тип адреса.</span><span class="sxs-lookup"><span data-stu-id="5178e-105">Specifies the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5178e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5178e-106">Syntax</span></span>


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="5178e-107">Константы</span><span class="sxs-lookup"><span data-stu-id="5178e-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5178e-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**адрес CB не \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="5178e-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB\_ADDR\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="5178e-109">Тип адреса не определен.</span><span class="sxs-lookup"><span data-stu-id="5178e-109">The address type is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="5178e-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**Адрес версии-получателя CB \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5178e-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB\_ADDR\_IPv4**</span></span>
</dt> <dd>

<span data-ttu-id="5178e-111">Адрес — это IPv4-адрес.</span><span class="sxs-lookup"><span data-stu-id="5178e-111">The address is an IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="5178e-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**\_Адрес \_ версии-получателя CB**</span><span class="sxs-lookup"><span data-stu-id="5178e-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB\_ADDR\_IPv6**</span></span>
</dt> <dd>

<span data-ttu-id="5178e-113">Адрес является адресом IPv6.</span><span class="sxs-lookup"><span data-stu-id="5178e-113">The address is an IPv6 address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5178e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5178e-114">Requirements</span></span>



| <span data-ttu-id="5178e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5178e-115">Requirement</span></span> | <span data-ttu-id="5178e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5178e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5178e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5178e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5178e-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5178e-118">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="5178e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5178e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5178e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5178e-120">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="5178e-121">Header</span><span class="sxs-lookup"><span data-stu-id="5178e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5178e-122"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="5178e-122"><dt>Cbclient.h</dt></span></span> </dl> |



 

 





