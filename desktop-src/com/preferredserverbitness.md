---
title: преферредсервербитнесс
description: Задает предпочтительную архитектуру (32-бит или 64-бит) для этого COM-сервера.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- COM-значение реестра Преферредсервербитнесс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339356"
---
# <a name="preferredserverbitness"></a><span data-ttu-id="269d1-104">преферредсервербитнесс</span><span class="sxs-lookup"><span data-stu-id="269d1-104">PreferredServerBitness</span></span>

<span data-ttu-id="269d1-105">Задает предпочтительную архитектуру (32-бит или 64-бит) для этого COM-сервера.</span><span class="sxs-lookup"><span data-stu-id="269d1-105">Sets the preferred architecture, 32-bit or 64-bit, for this COM server.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="269d1-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="269d1-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a><span data-ttu-id="269d1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="269d1-107">Remarks</span></span>

<span data-ttu-id="269d1-108">Это значение **reg \_ DWORD** , которое доступно только в 64-разрядных версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="269d1-108">This is a **REG\_DWORD** value that is available only on 64-bit versions of Windows.</span></span>



| <span data-ttu-id="269d1-109">Значение</span><span class="sxs-lookup"><span data-stu-id="269d1-109">Value</span></span> | <span data-ttu-id="269d1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="269d1-110">Description</span></span>                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="269d1-111">1</span><span class="sxs-lookup"><span data-stu-id="269d1-111">1</span></span>     | <span data-ttu-id="269d1-112">Сопоставьте серверную архитектуру с архитектурой клиента.</span><span class="sxs-lookup"><span data-stu-id="269d1-112">Match the server architecture to the client architecture.</span></span> <span data-ttu-id="269d1-113">Например, если клиент является 32-битным, используйте 32-разрядную версию сервера, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="269d1-113">For example, if the client is 32-bit, use a 32-bit version of the server, if it is available.</span></span> <span data-ttu-id="269d1-114">В противном случае запрос на активацию клиента завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="269d1-114">If not, the client's activation request will fail.</span></span> |
| <span data-ttu-id="269d1-115">2</span><span class="sxs-lookup"><span data-stu-id="269d1-115">2</span></span>     | <span data-ttu-id="269d1-116">Используйте 32-разрядную версию сервера.</span><span class="sxs-lookup"><span data-stu-id="269d1-116">Use a 32-bit version of the server.</span></span> <span data-ttu-id="269d1-117">Если такой объект не существует, запрос на активацию клиента завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="269d1-117">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |
| <span data-ttu-id="269d1-118">3</span><span class="sxs-lookup"><span data-stu-id="269d1-118">3</span></span>     | <span data-ttu-id="269d1-119">Используйте 64-разрядную версию сервера.</span><span class="sxs-lookup"><span data-stu-id="269d1-119">Use a 64-bit version of the server.</span></span> <span data-ttu-id="269d1-120">Если такой объект не существует, запрос на активацию клиента завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="269d1-120">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |



 

<span data-ttu-id="269d1-121">Если это значение отсутствует, то:</span><span class="sxs-lookup"><span data-stu-id="269d1-121">If this value is not present, then:</span></span>

-   <span data-ttu-id="269d1-122">Если компьютер, на котором размещается сервер, работает под управлением Windows XP или Windows Server 2003 без пакета обновления 1 (SP1) или более поздней версии, то COM предпочитает версию сервера, поддерживающую 64 бит, если он доступен. в противном случае будет активирована 32-разрядная версия сервера.</span><span class="sxs-lookup"><span data-stu-id="269d1-122">If the computer that hosts the server is running Windows XP or Windows Server 2003 without SP1 or later installed, then COM will prefer a 64-bit version of the server if available; otherwise it will activate a 32-bit version of the server.</span></span>
-   <span data-ttu-id="269d1-123">Если компьютер, на котором размещен сервер, работает под управлением Windows Server 2003 с пакетом обновления 1 (SP1) или более поздней версии, COM попытается сопоставить серверную архитектуру с архитектурой клиента.</span><span class="sxs-lookup"><span data-stu-id="269d1-123">If the computer that hosts the server is running Windows Server 2003 with SP1 or later installed, then COM will try to match the server architecture to the client architecture.</span></span> <span data-ttu-id="269d1-124">Иными словами, для 32-разрядного клиента COM активирует 32-разрядный сервер, если он доступен. в противном случае будет активирована 64-разрядная версия сервера.</span><span class="sxs-lookup"><span data-stu-id="269d1-124">In other words, for a 32-bit client, COM will activate a 32-bit server if available; otherwise it will activate a 64-bit version of the server.</span></span> <span data-ttu-id="269d1-125">Для 64-разрядного клиента COM активирует 64-разрядный сервер, если он доступен. в противном случае будет активирован 32-разрядный сервер.</span><span class="sxs-lookup"><span data-stu-id="269d1-125">For a 64-bit client, COM will activate a 64-bit server if available; otherwise it will activate a 32-bit server.</span></span>

<span data-ttu-id="269d1-126">Клиент также может задать собственную настройку архитектуры с помощью КЛСКТКС \_ активировать \_ 32 \_ bit \_ server и клскткс \_ активировать \_ 64 \_ bit \_ Server flags, и это переопределит предпочтения сервера.</span><span class="sxs-lookup"><span data-stu-id="269d1-126">The client can also specify its own architecture preference via the CLSCTX\_ACTIVATE\_32\_BIT\_SERVER and CLSCTX\_ACTIVATE\_64\_BIT\_SERVER flags, and these will override the server's preference.</span></span> <span data-ttu-id="269d1-127">Дополнительные сведения и диаграмма возможных взаимодействий между параметрами архитектуры клиента и сервера см. в разделе [**клскткс**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span><span class="sxs-lookup"><span data-stu-id="269d1-127">For more information, and a chart of possible interactions between client and server architecture preferences, see [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="269d1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="269d1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="269d1-129">**клскткс**</span><span class="sxs-lookup"><span data-stu-id="269d1-129">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 