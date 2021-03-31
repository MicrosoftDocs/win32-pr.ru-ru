---
title: Пример значений реестра
description: В следующем примере показаны возможные данные для некоторых значений реестра протокола проверки подлинности.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104069412"
---
# <a name="registry-values-example"></a><span data-ttu-id="a1315-103">Пример значений реестра</span><span class="sxs-lookup"><span data-stu-id="a1315-103">Registry Values Example</span></span>

<span data-ttu-id="a1315-104">В следующем примере показаны возможные данные для некоторых значений реестра протокола проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a1315-104">The following example shows possible data for some of the authentication protocol registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| <span data-ttu-id="a1315-105">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="a1315-105">Key Name</span></span>            | <span data-ttu-id="a1315-106">Datatype</span><span class="sxs-lookup"><span data-stu-id="a1315-106">Datatype</span></span>        | <span data-ttu-id="a1315-107">Значение</span><span class="sxs-lookup"><span data-stu-id="a1315-107">Value</span></span>                                  |
|---------------------|-----------------|----------------------------------------|
| <span data-ttu-id="a1315-108">Путь</span><span class="sxs-lookup"><span data-stu-id="a1315-108">Path</span></span>                | <span data-ttu-id="a1315-109">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a1315-109">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="a1315-110">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="a1315-110">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="a1315-111">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a1315-111">FriendlyName</span></span>        | <span data-ttu-id="a1315-112">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a1315-112">REG\_SZ</span></span>         | <span data-ttu-id="a1315-113">Пример протокола EAP</span><span class="sxs-lookup"><span data-stu-id="a1315-113">Sample EAP Protocol</span></span>                    |
| <span data-ttu-id="a1315-114">конфигуипас</span><span class="sxs-lookup"><span data-stu-id="a1315-114">ConfigUIPath</span></span>        | <span data-ttu-id="a1315-115">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a1315-115">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="a1315-116">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="a1315-116">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="a1315-117">идентитипас</span><span class="sxs-lookup"><span data-stu-id="a1315-117">IdentityPath</span></span>        | <span data-ttu-id="a1315-118">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a1315-118">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="a1315-119">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="a1315-119">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="a1315-120">интерактивеуипас</span><span class="sxs-lookup"><span data-stu-id="a1315-120">InteractiveUIPath</span></span>   | <span data-ttu-id="a1315-121">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a1315-121">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="a1315-122">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="a1315-122">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="a1315-123">рекуиреконфигуи</span><span class="sxs-lookup"><span data-stu-id="a1315-123">RequireConfigUI</span></span>     | <span data-ttu-id="a1315-124">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="a1315-124">REG\_DWORD</span></span>      | <span data-ttu-id="a1315-125">1</span><span class="sxs-lookup"><span data-stu-id="a1315-125">1</span></span>                                      |
| <span data-ttu-id="a1315-126">конфигклсид</span><span class="sxs-lookup"><span data-stu-id="a1315-126">ConfigCLSID</span></span>         | <span data-ttu-id="a1315-127">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a1315-127">REG\_SZ</span></span>         | <span data-ttu-id="a1315-128">{0000031A-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="a1315-128">{0000031A-0000-0000-C000-000000000046}</span></span> |
| <span data-ttu-id="a1315-129">стандалонесуппортед</span><span class="sxs-lookup"><span data-stu-id="a1315-129">StandaloneSupported</span></span> | <span data-ttu-id="a1315-130">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="a1315-130">REG\_DWORD</span></span>      | <span data-ttu-id="a1315-131">1</span><span class="sxs-lookup"><span data-stu-id="a1315-131">1</span></span>                                      |



 

 

 




