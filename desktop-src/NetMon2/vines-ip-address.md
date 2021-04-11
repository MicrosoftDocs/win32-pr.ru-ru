---
description: '\_Структура IP- \_ адресов vines представляет собой IP-адрес в сети Vines.'
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Структура VINES_IP_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346295"
---
# <a name="vines_ip_address-structure"></a><span data-ttu-id="63bf0-103">\_Структура IP-адресов vines \_</span><span class="sxs-lookup"><span data-stu-id="63bf0-103">VINES\_IP\_ADDRESS structure</span></span>

<span data-ttu-id="63bf0-104">Структура **\_ IP- \_ адресов vines** представляет собой IP-адрес в сети Vines.</span><span class="sxs-lookup"><span data-stu-id="63bf0-104">The **VINES\_IP\_ADDRESS** structure is an IP address on a Vines network.</span></span>

## <a name="syntax"></a><span data-ttu-id="63bf0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63bf0-105">Syntax</span></span>


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="63bf0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="63bf0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="63bf0-107">**нетид**</span><span class="sxs-lookup"><span data-stu-id="63bf0-107">**NetID**</span></span>
</dt> <dd>

<span data-ttu-id="63bf0-108">Идентификатор определенного компьютера в определенной подсети.</span><span class="sxs-lookup"><span data-stu-id="63bf0-108">The identifier of a specific machine on a specific subnet.</span></span>

</dd> <dt>

<span data-ttu-id="63bf0-109">**SubnetID**</span><span class="sxs-lookup"><span data-stu-id="63bf0-109">**SubnetID**</span></span>
</dt> <dd>

<span data-ttu-id="63bf0-110">Идентификатор определенной подсети в целой сети.</span><span class="sxs-lookup"><span data-stu-id="63bf0-110">The identifier of a specific subnet on the whole network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63bf0-111">Требования</span><span class="sxs-lookup"><span data-stu-id="63bf0-111">Requirements</span></span>



| <span data-ttu-id="63bf0-112">Требование</span><span class="sxs-lookup"><span data-stu-id="63bf0-112">Requirement</span></span> | <span data-ttu-id="63bf0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="63bf0-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="63bf0-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63bf0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="63bf0-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63bf0-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="63bf0-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63bf0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="63bf0-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63bf0-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="63bf0-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="63bf0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="63bf0-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="63bf0-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




