---
description: Метод Reset сбрасывается до начала последовательности перечисления.
ms.assetid: 338e0614-8f18-4ee2-8697-66ff3898f813
title: 'Метод Иенуммедиа:: Reset'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14624d5a048df2f5bc80205f34f262068c53da74
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684762"
---
# <a name="ienummediareset-method"></a><span data-ttu-id="0af0b-103">Метод Иенуммедиа:: Reset</span><span class="sxs-lookup"><span data-stu-id="0af0b-103">IEnumMedia::Reset method</span></span>

<span data-ttu-id="0af0b-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="0af0b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0af0b-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="0af0b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0af0b-106">Метод **Reset** сбрасывается до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="0af0b-106">The **Reset** method resets to the beginning of enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af0b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0af0b-107">Syntax</span></span>


```C++
HRESULT Reset();
```

## <a name="parameters"></a><span data-ttu-id="0af0b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0af0b-108">Parameters</span></span>
<span data-ttu-id="0af0b-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0af0b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0af0b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0af0b-110">Return value</span></span>
<span data-ttu-id="0af0b-111">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="0af0b-111">This method can return one of these values.</span></span>

| <span data-ttu-id="0af0b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0af0b-112">Value</span></span> | <span data-ttu-id="0af0b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0af0b-113">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="0af0b-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0af0b-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="0af0b-115">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="0af0b-115">Method succeeded.</span></span> <br/>         |
