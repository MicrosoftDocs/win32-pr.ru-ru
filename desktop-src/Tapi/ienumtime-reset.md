---
description: Метод Reset сбрасывается до начала последовательности перечисления.
ms.assetid: a9131da1-051d-493c-939d-07801fda2d49
title: 'Метод Иенумтиме:: Reset'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9615fbc07edfb93c2377a7455d94b5fcd8ccd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154567"
---
# <a name="ienumtimereset-method"></a><span data-ttu-id="8a7dd-103">Метод Иенумтиме:: Reset</span><span class="sxs-lookup"><span data-stu-id="8a7dd-103">IEnumTime::Reset method</span></span>

<span data-ttu-id="8a7dd-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a7dd-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8a7dd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8a7dd-106">Метод **Reset** сбрасывается до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-106">The **Reset** method resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7dd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a7dd-107">Syntax</span></span>


```C++
HRESULT Reset();
```

## <a name="parameters"></a><span data-ttu-id="8a7dd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a7dd-108">Parameters</span></span>
<span data-ttu-id="8a7dd-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a7dd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a7dd-110">Return value</span></span>
<span data-ttu-id="8a7dd-111">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-111">This method can return one of these values.</span></span>

| <span data-ttu-id="8a7dd-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8a7dd-112">Value</span></span> | <span data-ttu-id="8a7dd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8a7dd-113">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="8a7dd-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7dd-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8a7dd-115">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="8a7dd-115">Method succeeded.</span></span> <br/>         |
