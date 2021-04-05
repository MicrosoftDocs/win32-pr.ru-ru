---
title: add iplisten
description: Указывает адрес IPv4 или IPv6, добавляемый в список прослушивания IP-адресов.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- Добавить иплистен HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "103987247"
---
# <a name="add-iplisten"></a><span data-ttu-id="c9cdd-104">add iplisten</span><span class="sxs-lookup"><span data-stu-id="c9cdd-104">add iplisten</span></span>

<span data-ttu-id="c9cdd-105">Указывает адрес IPv4 или IPv6, добавляемый в список прослушивания IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c9cdd-105">Specifies an IPv4 or IPv6 address to be added to the IP listen list.</span></span>

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="c9cdd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9cdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9cdd-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="c9cdd-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="c9cdd-108">Указывает адрес IPv4 или IPv6, добавляемый в список прослушивания IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c9cdd-108">Specifies the IPv4 or IPv6 address to be added to the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9cdd-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9cdd-109">Remarks</span></span>

<span data-ttu-id="c9cdd-110">Добавляет новый IP-адрес в список прослушивания IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c9cdd-110">Adds a new IP address to the IP listen list.</span></span> <span data-ttu-id="c9cdd-111">Это не распространяется на номер порта.</span><span class="sxs-lookup"><span data-stu-id="c9cdd-111">This does not include the port number.</span></span> <span data-ttu-id="c9cdd-112">Список прослушивания IP-адресов используется для определения области списка адресов, к которым привязывается служба HTTP.</span><span class="sxs-lookup"><span data-stu-id="c9cdd-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="c9cdd-113">"0.0.0.0" означает любой IPv4-адрес, а "::" — любой IPv6-адрес.</span><span class="sxs-lookup"><span data-stu-id="c9cdd-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="c9cdd-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="c9cdd-114">Examples</span></span>

<span data-ttu-id="c9cdd-115">**add iplisten ipaddress=fe80::1**</span><span class="sxs-lookup"><span data-stu-id="c9cdd-115">**add iplisten ipaddress=fe80::1**</span></span>

<span data-ttu-id="c9cdd-116">**add iplisten ipaddress=1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="c9cdd-116">**add iplisten ipaddress=1.1.1.1**</span></span>

<span data-ttu-id="c9cdd-117">**add iplisten ipaddress=0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="c9cdd-117">**add iplisten ipaddress=0.0.0.0**</span></span>

<span data-ttu-id="c9cdd-118">**add iplisten ipaddress=::**</span><span class="sxs-lookup"><span data-stu-id="c9cdd-118">**add iplisten ipaddress=::**</span></span>

 

 




