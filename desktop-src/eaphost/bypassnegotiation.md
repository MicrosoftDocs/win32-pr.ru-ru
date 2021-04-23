---
title: бипасснеготиатион
description: Раздел реестра Бипасснеготиатион определяет, происходит ли согласование возможностей между сервером и клиентом или если используются предварительно настроенные параметры.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412295"
---
# <a name="bypassnegotiation"></a><span data-ttu-id="23ee0-103">бипасснеготиатион</span><span class="sxs-lookup"><span data-stu-id="23ee0-103">BypassNegotiation</span></span>

<span data-ttu-id="23ee0-104">Раздел реестра Бипасснеготиатион определяет, происходит ли согласование возможностей между сервером и клиентом или если используются предварительно настроенные параметры.</span><span class="sxs-lookup"><span data-stu-id="23ee0-104">The BypassNegotiation registry key determines if capabilities negotiation between the server and client occurs or if pre-configured settings are used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="23ee0-105">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="23ee0-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a><span data-ttu-id="23ee0-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23ee0-106">Remarks</span></span>

<span data-ttu-id="23ee0-107">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="23ee0-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="23ee0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="23ee0-108">Value</span></span>   | <span data-ttu-id="23ee0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="23ee0-109">Description</span></span>                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23ee0-110">0</span><span class="sxs-lookup"><span data-stu-id="23ee0-110">0</span></span>       | <span data-ttu-id="23ee0-111">Сервер и клиент согласовывают возможности EAP.</span><span class="sxs-lookup"><span data-stu-id="23ee0-111">Server and client negotiate EAP capabilities.</span></span>                                                                                                                                                        |
| <span data-ttu-id="23ee0-112">отличные</span><span class="sxs-lookup"><span data-stu-id="23ee0-112">nonzero</span></span> | <span data-ttu-id="23ee0-113">Сервер и клиент не согласовывают возможности EAP.</span><span class="sxs-lookup"><span data-stu-id="23ee0-113">Server and client do not negotiate EAP capabilities.</span></span> <span data-ttu-id="23ee0-114">Сервер и клиент используют значение раздела реестра [AssumePhase2Fragmentation](assumephase2fragmentation.md) для поиска возможностей других сторон.</span><span class="sxs-lookup"><span data-stu-id="23ee0-114">Server and client use the [AssumePhase2Fragmentation](assumephase2fragmentation.md) registry key value to find the other party's capabilities.</span></span> |



 

<span data-ttu-id="23ee0-115">Если этот параметр реестра отсутствует, сервер и клиент согласовывают возможности EAP.</span><span class="sxs-lookup"><span data-stu-id="23ee0-115">If this registry value is not present, the server and client negotiate EAP capabilities..</span></span>

## <a name="related-topics"></a><span data-ttu-id="23ee0-116">См. также</span><span class="sxs-lookup"><span data-stu-id="23ee0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23ee0-117">Параметры реестра EAPHost</span><span class="sxs-lookup"><span data-stu-id="23ee0-117">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




