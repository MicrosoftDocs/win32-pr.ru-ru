---
title: Типы данных службы удаленного доступа (RAS. h)
description: API службы удаленного доступа использует следующие типы данных.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988621"
---
# <a name="remote-access-service-data-types"></a><span data-ttu-id="3293b-105">Типы данных службы удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="3293b-105">Remote Access Service Data Types</span></span>

<span data-ttu-id="3293b-106">API службы удаленного доступа использует следующие типы данных.</span><span class="sxs-lookup"><span data-stu-id="3293b-106">The following data types are used by the Remote Access Service API.</span></span>


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

<span data-ttu-id="3293b-107">**RASIPV4ADDR**</span><span class="sxs-lookup"><span data-stu-id="3293b-107">**RASIPV4ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="3293b-108">Значение [**в \_ адресе**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) , содержащее IPv4-адрес.</span><span class="sxs-lookup"><span data-stu-id="3293b-108">A [**in\_addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) that contains an IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="3293b-109">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="3293b-109">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> <dt>

<span data-ttu-id="3293b-110">**RASIPV6ADDR**</span><span class="sxs-lookup"><span data-stu-id="3293b-110">**RASIPV6ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="3293b-111">[**In6 адрес \_ ,**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) который содержит IPv6-адреса.</span><span class="sxs-lookup"><span data-stu-id="3293b-111">A [**in6\_addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) that contains an IPv6 address.</span></span>

> [!Note]  
> <span data-ttu-id="3293b-112">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="3293b-112">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3293b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3293b-113">Requirements</span></span>



| <span data-ttu-id="3293b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3293b-114">Requirement</span></span> | <span data-ttu-id="3293b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3293b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3293b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3293b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3293b-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3293b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3293b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3293b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3293b-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3293b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3293b-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3293b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3293b-121"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="3293b-121"><dt>Ras.h</dt></span></span> </dl> |



 

