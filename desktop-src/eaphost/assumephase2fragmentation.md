---
title: AssumePhase2Fragmentation
description: Раздел реестра AssumePhase2Fragmentation определяет, предполагает ли сервер и клиент фрагментацию этапа 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412277"
---
# <a name="assumephase2fragmentation"></a><span data-ttu-id="a9400-103">AssumePhase2Fragmentation</span><span class="sxs-lookup"><span data-stu-id="a9400-103">AssumePhase2Fragmentation</span></span>

<span data-ttu-id="a9400-104">Раздел реестра AssumePhase2Fragmentation определяет, предполагает ли сервер и клиент фрагментацию этапа 2.</span><span class="sxs-lookup"><span data-stu-id="a9400-104">The AssumePhase2Fragmentation registry key determines if the server and client assume phase 2 fragmentation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a9400-105">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="a9400-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a><span data-ttu-id="a9400-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9400-106">Remarks</span></span>

<span data-ttu-id="a9400-107">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a9400-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="a9400-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a9400-108">Value</span></span>   | <span data-ttu-id="a9400-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a9400-109">Description</span></span>                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9400-110">0</span><span class="sxs-lookup"><span data-stu-id="a9400-110">0</span></span>       | <span data-ttu-id="a9400-111">Сервер и клиент предполагают, что другая сторона не поддерживает 2 этапа фрагментации во время аутентификации PEAP.</span><span class="sxs-lookup"><span data-stu-id="a9400-111">Server and client assume the other party is not capable of phase 2 fragmentation during PEAP authentication.</span></span> |
| <span data-ttu-id="a9400-112">отличные</span><span class="sxs-lookup"><span data-stu-id="a9400-112">nonzero</span></span> | <span data-ttu-id="a9400-113">Сервер и клиент предполагают, что другая сторона поддерживает этап 2 во время проверки подлинности PEAP.</span><span class="sxs-lookup"><span data-stu-id="a9400-113">Server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>     |



 

<span data-ttu-id="a9400-114">Если это значение реестра отсутствует, сервер и клиент предполагают, что другая сторона поддерживает фрагментацию второго этапа во время аутентификации PEAP.</span><span class="sxs-lookup"><span data-stu-id="a9400-114">If this registry value is not present, the server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9400-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a9400-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9400-116">Параметры реестра EAPHost</span><span class="sxs-lookup"><span data-stu-id="a9400-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




