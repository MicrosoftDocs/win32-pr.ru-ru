---
description: Согласование типов мультимедиа
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Согласование типов мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684788"
---
# <a name="negotiating-media-types"></a><span data-ttu-id="8dc13-103">Согласование типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8dc13-103">Negotiating Media Types</span></span>

<span data-ttu-id="8dc13-104">Когда диспетчер графа фильтров вызывает метод [**Ипин:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , он имеет несколько параметров для указания типа носителя:</span><span class="sxs-lookup"><span data-stu-id="8dc13-104">When the Filter Graph Manager calls the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method, it has several options for specifying a media type:</span></span>

-   <span data-ttu-id="8dc13-105">**Полный тип:** Если тип носителя указан полностью, ПИН-коды пытаются подключиться к этому типу.</span><span class="sxs-lookup"><span data-stu-id="8dc13-105">**Complete type:** If the media type is fully specified, the pins attempt to connect with that type.</span></span> <span data-ttu-id="8dc13-106">В противном случае попытка подключения завершится неудачей.</span><span class="sxs-lookup"><span data-stu-id="8dc13-106">If they cannot, the connection attempt fails.</span></span>
-   <span data-ttu-id="8dc13-107">**Тип частичного носителя:** Тип мультимедиа является *разделяемым* , если основной тип, подтип или тип формата имеют \_ значение GUID null.</span><span class="sxs-lookup"><span data-stu-id="8dc13-107">**Partial media type:** A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span> <span data-ttu-id="8dc13-108">Значение GUID \_ , равное NULL, действует как "подстановочный знак", что означает приемлемое значение.</span><span class="sxs-lookup"><span data-stu-id="8dc13-108">The value GUID\_NULL acts as a "wildcard," indicating that any value is acceptable.</span></span> <span data-ttu-id="8dc13-109">Эти контакты согласовывают тип, который согласуется с частичным типом.</span><span class="sxs-lookup"><span data-stu-id="8dc13-109">The pins negotiate a type that is consistent with the partial type.</span></span>
-   <span data-ttu-id="8dc13-110">**Нет типа носителя:** Если диспетчер графа фильтров передает **пустой** указатель, ПИН-коды могут быть согласованы с любым типом мультимедиа, допустимым для обоих ПИН.</span><span class="sxs-lookup"><span data-stu-id="8dc13-110">**No media type:** If the Filter Graph Manager passes a **NULL** pointer, the pins can agree to any media type that is acceptable to both pins.</span></span>

<span data-ttu-id="8dc13-111">Если ПИН-коды выполняют подключение, подключение всегда имеет полный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="8dc13-111">If the pins do connect, the connection always has a complete media type.</span></span> <span data-ttu-id="8dc13-112">Тип носителя, заданный диспетчером графа фильтров, предназначен для ограничения возможных типов соединения.</span><span class="sxs-lookup"><span data-stu-id="8dc13-112">The purpose of the media type given by the Filter Graph Manager is to limit the possible connection types.</span></span>

<span data-ttu-id="8dc13-113">Во время процесса согласования выходной ПИН-код предлагает тип мультимедиа, вызывая метод [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) входного контакта.</span><span class="sxs-lookup"><span data-stu-id="8dc13-113">During the negotiation process, the output pin proposes a media type by calling the input pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="8dc13-114">Входной ПИН-код может принять или отклонить предложенный тип.</span><span class="sxs-lookup"><span data-stu-id="8dc13-114">The input pin can accept or reject the proposed type.</span></span> <span data-ttu-id="8dc13-115">Этот процесс повторяется до тех пор, пока входной ПИН-код не примет тип или выходной ПИН-код выходит за пределы типов, а соединение завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8dc13-115">This process repeats until either the input pin accepts a type, or the output pin runs out of types and the connection fails.</span></span>

<span data-ttu-id="8dc13-116">Как закрепление вывода выбирает типы носителей для предложения, зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="8dc13-116">How an output pin selects media types to propose depends on the implementation.</span></span> <span data-ttu-id="8dc13-117">В базовых классах DirectShow выходной ПИН-код вызывает [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="8dc13-117">In the DirectShow base classes, the output pin calls [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) on the input pin.</span></span> <span data-ttu-id="8dc13-118">Этот метод возвращает перечислитель, который перечисляет предпочтительные типы мультимедиа для входного контакта.</span><span class="sxs-lookup"><span data-stu-id="8dc13-118">This method returns an enumerator that enumerates the input pin's preferred media types.</span></span> <span data-ttu-id="8dc13-119">В таком случае закрепление вывода перечисляет свои собственные предпочтительные типы.</span><span class="sxs-lookup"><span data-stu-id="8dc13-119">Failing that, the output pin enumerates its own preferred types.</span></span>

<span data-ttu-id="8dc13-120">**Работа с типами мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="8dc13-120">**Working with Media Types**</span></span>

<span data-ttu-id="8dc13-121">В любой функции, которая получает **параметр \_ \_ типа мультимедиа AM** , всегда проверяйте значения **кбформат** и **форматтипе** перед разыменованием элемента **пбформат** .</span><span class="sxs-lookup"><span data-stu-id="8dc13-121">In any function that receives an **AM\_MEDIA\_TYPE** parameter, always validate the values of **cbFormat** and **formattype** before dereferencing the **pbFormat** member.</span></span> <span data-ttu-id="8dc13-122">Следующий код неверный:</span><span class="sxs-lookup"><span data-stu-id="8dc13-122">The following code is incorrect:</span></span>


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



<span data-ttu-id="8dc13-123">Следующий код правильный:</span><span class="sxs-lookup"><span data-stu-id="8dc13-123">The following code is correct:</span></span>


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



