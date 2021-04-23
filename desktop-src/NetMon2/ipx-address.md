---
description: Структура IPX- \_ адреса предоставляет адрес на уровне протокола IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: Структура IPX_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541183"
---
# <a name="ipx_address-structure"></a><span data-ttu-id="3c6a8-103">\_Структура адреса IPX</span><span class="sxs-lookup"><span data-stu-id="3c6a8-103">IPX\_ADDRESS structure</span></span>

<span data-ttu-id="3c6a8-104">Структура **IPX- \_ адреса** предоставляет адрес на уровне протокола IPX.</span><span class="sxs-lookup"><span data-stu-id="3c6a8-104">The **IPX\_ADDRESS** structure provides an address at the IPX protocol level.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c6a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c6a8-105">Syntax</span></span>


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="3c6a8-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3c6a8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3c6a8-107">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="3c6a8-107">**Subnet**</span></span>
</dt> <dd>

<span data-ttu-id="3c6a8-108">Идентификатор подсети сети.</span><span class="sxs-lookup"><span data-stu-id="3c6a8-108">Network subnet identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3c6a8-109">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="3c6a8-109">**Address**</span></span>
</dt> <dd>

<span data-ttu-id="3c6a8-110">Идентификатор подсети NIC.</span><span class="sxs-lookup"><span data-stu-id="3c6a8-110">Subnet NIC identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c6a8-111">Требования</span><span class="sxs-lookup"><span data-stu-id="3c6a8-111">Requirements</span></span>



| <span data-ttu-id="3c6a8-112">Требование</span><span class="sxs-lookup"><span data-stu-id="3c6a8-112">Requirement</span></span> | <span data-ttu-id="3c6a8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3c6a8-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c6a8-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c6a8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3c6a8-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c6a8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3c6a8-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c6a8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3c6a8-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c6a8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3c6a8-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3c6a8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c6a8-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c6a8-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




