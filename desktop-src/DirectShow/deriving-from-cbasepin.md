---
description: Наследование от Кбасепин
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Наследование от Кбасепин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673110"
---
# <a name="deriving-from-cbasepin"></a><span data-ttu-id="4efe9-103">Наследование от Кбасепин</span><span class="sxs-lookup"><span data-stu-id="4efe9-103">Deriving from CBasePin</span></span>

<span data-ttu-id="4efe9-104">Чтобы реализовать ПИН-код с помощью [**кбасепин**](cbasepin.md), необходимо создать производный класс от базового класса и переопределить несколько его методов.</span><span class="sxs-lookup"><span data-stu-id="4efe9-104">To implement a pin using [**CBasePin**](cbasepin.md), you must derive a new class from the base class and override several of its methods.</span></span> <span data-ttu-id="4efe9-105">Необходимо переопределить следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4efe9-105">You must override the following methods:</span></span>

-   [<span data-ttu-id="4efe9-106">**Кбасепин:: Чеккмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="4efe9-106">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="4efe9-107">**Кбасепин:: Жетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="4efe9-107">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="4efe9-108">Возможно, потребуется переопределить следующие дополнительные методы:</span><span class="sxs-lookup"><span data-stu-id="4efe9-108">You will probably need to override these additional methods:</span></span>

-   [<span data-ttu-id="4efe9-109">**Кбасепин:: Active**</span><span class="sxs-lookup"><span data-stu-id="4efe9-109">**CBasePin::Active**</span></span>](cbasepin-active.md)
-   [<span data-ttu-id="4efe9-110">**Кбасепин:: Бреакконнект**</span><span class="sxs-lookup"><span data-stu-id="4efe9-110">**CBasePin::BreakConnect**</span></span>](cbasepin-breakconnect.md)
-   [<span data-ttu-id="4efe9-111">**Кбасепин:: Чеккконнект**</span><span class="sxs-lookup"><span data-stu-id="4efe9-111">**CBasePin::CheckConnect**</span></span>](cbasepin-checkconnect.md)
-   [<span data-ttu-id="4efe9-112">**Кбасепин:: Комплетеконнект**</span><span class="sxs-lookup"><span data-stu-id="4efe9-112">**CBasePin::CompleteConnect**</span></span>](cbasepin-completeconnect.md)
-   [<span data-ttu-id="4efe9-113">**Кбасепин:: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="4efe9-113">**CBasePin::EndOfStream**</span></span>](cbasepin-endofstream.md)
-   [<span data-ttu-id="4efe9-114">**Кбасепин:: Inactive**</span><span class="sxs-lookup"><span data-stu-id="4efe9-114">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md)
-   [<span data-ttu-id="4efe9-115">**Кбасепин:: notify**</span><span class="sxs-lookup"><span data-stu-id="4efe9-115">**CBasePin::Notify**</span></span>](cbasepin-notify.md)
-   [<span data-ttu-id="4efe9-116">**Кбасепин:: Run**</span><span class="sxs-lookup"><span data-stu-id="4efe9-116">**CBasePin::Run**</span></span>](cbasepin-run.md)

<span data-ttu-id="4efe9-117">Наконец, необходимо реализовать методы [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) и [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="4efe9-117">Finally, you must must implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span>

<span data-ttu-id="4efe9-118">Некоторые из этих методов реализуются в базовых классах, производных от **кбасепин**, таких как [**кбасеинпутпин**](cbaseinputpin.md) и [**кбасеаутпутпин**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="4efe9-118">Some of these methods are implemented in base classes that derive from **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md) and [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4efe9-119">См. также</span><span class="sxs-lookup"><span data-stu-id="4efe9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4efe9-120">**кбасепин**</span><span class="sxs-lookup"><span data-stu-id="4efe9-120">**CBasePin**</span></span>](cbasepin.md)
</dt> </dl>

 

 



