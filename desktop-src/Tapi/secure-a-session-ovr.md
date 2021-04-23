---
description: Если приложение не хочет никаких помех извне за пределами событий для сеанса от TAPI или поставщика услуг, он должен обеспечить защиту вызова.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Обеспечение безопасности сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684662"
---
# <a name="secure-a-session"></a><span data-ttu-id="0c735-103">Обеспечение безопасности сеанса</span><span class="sxs-lookup"><span data-stu-id="0c735-103">Secure a Session</span></span>

<span data-ttu-id="0c735-104">Если приложение не хочет никаких помех извне за пределами событий для сеанса от TAPI или поставщика услуг, он должен обеспечить защиту вызова.</span><span class="sxs-lookup"><span data-stu-id="0c735-104">If an application does not want any interference by outside events for a session from TAPI or the service provider, it should secure the call.</span></span> <span data-ttu-id="0c735-105">Например, в аналоговой среде в режиме ожидания вызовов может уничтожиться сеанс факса или модема при первоначальном вызове.</span><span class="sxs-lookup"><span data-stu-id="0c735-105">For example, in an analog environment call-waiting tones can destroy a fax or modem session on the original call.</span></span>

<span data-ttu-id="0c735-106">Приложение может защитить вызов во время вызова или после того, как вызов уже существует.</span><span class="sxs-lookup"><span data-stu-id="0c735-106">An application can secure a call at the time the call is made or after the call already exists.</span></span>

<span data-ttu-id="0c735-107">Не все поставщики служб поддерживают использование этой операции.</span><span class="sxs-lookup"><span data-stu-id="0c735-107">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="0c735-108">**Интерфейс TAPI 2. x:** См. [**линесекурекалл**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span><span class="sxs-lookup"><span data-stu-id="0c735-108">**TAPI 2.x:** See [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span></span>

<span data-ttu-id="0c735-109">**Интерфейс TAPI 3. x:** См. раздел [**итаддресс:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span><span class="sxs-lookup"><span data-stu-id="0c735-109">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span></span>

 

 
