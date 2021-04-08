---
title: delete iplisten
description: Указывает адрес IPv4 или IPv6, удаляемый из списка прослушивания IP-адресов.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- Удаление иплистен HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104069229"
---
# <a name="delete-iplisten"></a><span data-ttu-id="13bbb-104">delete iplisten</span><span class="sxs-lookup"><span data-stu-id="13bbb-104">delete iplisten</span></span>

<span data-ttu-id="13bbb-105">Указывает адрес IPv4 или IPv6, удаляемый из списка прослушивания IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="13bbb-105">Specifies an IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="13bbb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="13bbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13bbb-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ address = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="13bbb-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[address=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="13bbb-108">Указывает IPv4-или IPv6-адрес, который нужно удалить из списка прослушивания IP.</span><span class="sxs-lookup"><span data-stu-id="13bbb-108">Specifies the IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13bbb-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13bbb-109">Remarks</span></span>

<span data-ttu-id="13bbb-110">Удаляет IP-адрес из списка прослушивания IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="13bbb-110">Deletes an IP address to the IP listen list.</span></span> <span data-ttu-id="13bbb-111">Это не распространяется на номер порта.</span><span class="sxs-lookup"><span data-stu-id="13bbb-111">This does not include the port number.</span></span> <span data-ttu-id="13bbb-112">Список прослушивания IP-адресов используется для определения области списка адресов, к которым привязывается служба HTTP.</span><span class="sxs-lookup"><span data-stu-id="13bbb-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="13bbb-113">"0.0.0.0" означает любой IPv4-адрес, а "::" — любой IPv6-адрес.</span><span class="sxs-lookup"><span data-stu-id="13bbb-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="13bbb-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="13bbb-114">Examples</span></span>

<span data-ttu-id="13bbb-115">**Удаление иплистен Address = FE80:: 1**</span><span class="sxs-lookup"><span data-stu-id="13bbb-115">**delete iplisten address=fe80::1**</span></span>

<span data-ttu-id="13bbb-116">**удалить иплистен Address = 1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="13bbb-116">**delete iplisten address=1.1.1.1**</span></span>

<span data-ttu-id="13bbb-117">**удалить адрес иплистен = 0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="13bbb-117">**delete iplisten address=0.0.0.0**</span></span>

<span data-ttu-id="13bbb-118">**удалить иплистен Address =::**</span><span class="sxs-lookup"><span data-stu-id="13bbb-118">**delete iplisten address=::**</span></span>

 

 




