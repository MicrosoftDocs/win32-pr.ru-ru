---
title: Отслеживание ссылок
description: Отслеживание ссылок
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488317"
---
# <a name="reference-tracking"></a><span data-ttu-id="109d7-103">Отслеживание ссылок</span><span class="sxs-lookup"><span data-stu-id="109d7-103">Reference Tracking</span></span>

<span data-ttu-id="109d7-104">Отслеживание ссылок может препятствовать непреднамеренной или вредоносной ранней версии объектов.</span><span class="sxs-lookup"><span data-stu-id="109d7-104">Reference tracking can prevent the unintentional or malicious early release of objects.</span></span>

<span data-ttu-id="109d7-105">При включении отслеживания ссылок вы запрашиваете, что распределенные вызовы [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) и [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) проходят проверку подлинности с помощью COM.</span><span class="sxs-lookup"><span data-stu-id="109d7-105">When you enable reference tracking, you are requesting that distributed [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls be authenticated by COM.</span></span> <span data-ttu-id="109d7-106">Когда отслеживание ссылок включено, COM отслеживает счетчики ссылок на пользователей, чтобы пользователь мог вызывать **выпуск** только для тех объектов, для которых пользователь ранее назывался **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="109d7-106">When reference tracking is enabled, COM keeps track of per-user reference counts so that a user can call **Release** only on objects that the user previously called **AddRef** on.</span></span> <span data-ttu-id="109d7-107">Несмотря на то, что отслеживание ссылок может снизить производительность, это гарантирует, что независимо от того, сколько раз заданный пользователь вызывает **выпуск**, объекты и заглушки будут существовать, если у кого-то другого есть ссылка на них.</span><span class="sxs-lookup"><span data-stu-id="109d7-107">Although reference tracking can decrease performance, it ensures that no matter how many times a given user calls **Release**, the objects and stubs will still exist if someone else has a reference to them.</span></span>

<span data-ttu-id="109d7-108">Клиент может настроить отслеживание ссылок для процесса, передав \_ флаг еоак Secure \_ REFS в вызове [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="109d7-108">The client can set reference tracking for a process by passing the EOAC\_SECURE\_REFS capability flag in a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="109d7-109">Можно также включить или отключить отслеживание ссылок для всех приложений на компьютере с помощью Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="109d7-109">You can also enable or disable reference tracking for all applications on a computer by using Dcomcnfg.exe.</span></span>

<span data-ttu-id="109d7-110">Если включено отслеживание ссылок, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) всегда использует параметры безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="109d7-110">If reference tracking is enabled, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) always uses default security settings.</span></span> <span data-ttu-id="109d7-111">В этом случае вызовы метода [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) на **IUnknown** завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="109d7-111">In this case, calls to [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) on **IUnknown** will fail.</span></span>

 

 