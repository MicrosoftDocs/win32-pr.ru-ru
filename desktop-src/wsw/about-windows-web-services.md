---
title: О веб-службах Windows
description: API веб-служб Windows — это многоуровневый API, который может быть изображен следующим образом.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104556388"
---
# <a name="about-windows-web-services"></a><span data-ttu-id="beeb8-103">О веб-службах Windows</span><span class="sxs-lookup"><span data-stu-id="beeb8-103">About Windows Web Services</span></span>

<span data-ttu-id="beeb8-104">API веб-служб Windows — это многоуровневый API, который может быть изображен следующим образом.</span><span class="sxs-lookup"><span data-stu-id="beeb8-104">The Windows Web Services API is a layered API and it may be pictured as follows</span></span>

![Схема, показывающая слои и области перекрестного слоя API веб-служб Windows.](images/apistack.png)

<span data-ttu-id="beeb8-106">ВВСАПИ — это многоуровневый API.</span><span class="sxs-lookup"><span data-stu-id="beeb8-106">The WWSAPI is a layered API.</span></span> <span data-ttu-id="beeb8-107">Мы планируем, чтобы большинство разработчиков нацелены на модель службы, которая является моделью программирования на основе методов.</span><span class="sxs-lookup"><span data-stu-id="beeb8-107">We expect most developers to target the Service Model, which is a method-based programming model.</span></span> <span data-ttu-id="beeb8-108">В модели службы узел службы предоставляет модель программирования на стороне сервера, а прокси-сервер — модель программирования на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="beeb8-108">In the Service Model, the Service Host provides the server side programming model, while Service Proxy provides the client side programming model.</span></span>

<span data-ttu-id="beeb8-109">Каждый уровень предоставляет набор интерфейсов API и типов, которые можно использовать с API этого слоя.</span><span class="sxs-lookup"><span data-stu-id="beeb8-109">Every layer exposes a set of APIs and types that can be used with APIs of that layer.</span></span>

## <a name="service-model"></a><span data-ttu-id="beeb8-110">Модель службы</span><span class="sxs-lookup"><span data-stu-id="beeb8-110">Service Model</span></span>

<span data-ttu-id="beeb8-111">Уровень верхнего уровня, называемый [моделью службы](service-model-layer-overview.md) , предоставляет модель программирования на основе методов, и это самая простая модель для использования.</span><span class="sxs-lookup"><span data-stu-id="beeb8-111">The top level layer called the [Service Model](service-model-layer-overview.md) provides a method-based programming model and it is the easiest model to use.</span></span> <span data-ttu-id="beeb8-112">В модели службы [узел службы](service-host.md) предоставляет модель программирования на стороне сервера, а [прокси службы](service-proxy.md) предоставляет клиентскую модель программирования.</span><span class="sxs-lookup"><span data-stu-id="beeb8-112">In the Service Model, the [Service Host](service-host.md) provides the server side programming model, while the [Service Proxy](service-proxy.md) provides the client side programming model.</span></span> <span data-ttu-id="beeb8-113">[Контекст](context.md) используется в модели службы для передачи соответствующего состояния, доступного операции службы, и (или) обратного вызова при его вызове.</span><span class="sxs-lookup"><span data-stu-id="beeb8-113">[Context](context.md) is used within the Service Model to pass in a relevant state available to the service operation and/or the callback when it is invoked.</span></span> <span data-ttu-id="beeb8-114">И [контракт службы](contract.md) используются для указания контракта службы в конечной точке, предоставляемой службой.</span><span class="sxs-lookup"><span data-stu-id="beeb8-114">And [Service Contract](contract.md) is used to specify a service contract on an endpoint exposed on the service.</span></span> <span data-ttu-id="beeb8-115">Следующие компоненты и операции являются частью уровня служб:</span><span class="sxs-lookup"><span data-stu-id="beeb8-115">The following components and operations are part of the Service Layer:</span></span>

-   [<span data-ttu-id="beeb8-116">Узел службы</span><span class="sxs-lookup"><span data-stu-id="beeb8-116">Service Host</span></span>](service-host.md)
-   [<span data-ttu-id="beeb8-117">Прокси-сервер службы</span><span class="sxs-lookup"><span data-stu-id="beeb8-117">Service Proxy</span></span>](service-proxy.md)
-   [<span data-ttu-id="beeb8-118">Контекст</span><span class="sxs-lookup"><span data-stu-id="beeb8-118">Context</span></span>](context.md)
-   [<span data-ttu-id="beeb8-119">Архивирован</span><span class="sxs-lookup"><span data-stu-id="beeb8-119">Contract</span></span>](contract.md)
-   [<span data-ttu-id="beeb8-120">Метаданные службы</span><span class="sxs-lookup"><span data-stu-id="beeb8-120">Service Metadata</span></span>](service-metadata.md)

## <a name="channel-layer"></a><span data-ttu-id="beeb8-121">Уровень канала</span><span class="sxs-lookup"><span data-stu-id="beeb8-121">Channel Layer</span></span>

<span data-ttu-id="beeb8-122">Модель службы построена на уровне канала, что обеспечивает полную гибкость, но сложнее в использовании.</span><span class="sxs-lookup"><span data-stu-id="beeb8-122">The Service Model is built upon a Channel Layer, which provides full flexibility but is more difficult to use.</span></span> <span data-ttu-id="beeb8-123">Следующие компоненты и операции являются частью уровня канала:</span><span class="sxs-lookup"><span data-stu-id="beeb8-123">The following components and operations are part of the Channel Layer:</span></span>

-   [<span data-ttu-id="beeb8-124">Message</span><span class="sxs-lookup"><span data-stu-id="beeb8-124">Message</span></span>](message.md)
-   [<span data-ttu-id="beeb8-125">Канал</span><span class="sxs-lookup"><span data-stu-id="beeb8-125">Channel</span></span>](channel.md)
-   [<span data-ttu-id="beeb8-126">Средство прослушивания</span><span class="sxs-lookup"><span data-stu-id="beeb8-126">Listener</span></span>](listener.md)
-   [<span data-ttu-id="beeb8-127">Ошибки</span><span class="sxs-lookup"><span data-stu-id="beeb8-127">Faults</span></span>](faults.md)
-   [<span data-ttu-id="beeb8-128">Url</span><span class="sxs-lookup"><span data-stu-id="beeb8-128">Url</span></span>](url.md)
-   [<span data-ttu-id="beeb8-129">Безопасность</span><span class="sxs-lookup"><span data-stu-id="beeb8-129">Security</span></span>](security-overview.md)
-   [<span data-ttu-id="beeb8-130">Импорт метаданных</span><span class="sxs-lookup"><span data-stu-id="beeb8-130">Metadata Import</span></span>](metadata-import.md)

## <a name="xml-layer"></a><span data-ttu-id="beeb8-131">Уровень XML</span><span class="sxs-lookup"><span data-stu-id="beeb8-131">XML Layer</span></span>

<span data-ttu-id="beeb8-132">Уровень канала, в свою очередь, построен на основе упрощенной платформы XML, которая включает десериализацию типов данных C.</span><span class="sxs-lookup"><span data-stu-id="beeb8-132">The Channel Layer is in turn built upon a lightweight XML framework, which includes deserialization of C data types.</span></span> <span data-ttu-id="beeb8-133">Следующие компоненты и операции являются частью XML-слоя:</span><span class="sxs-lookup"><span data-stu-id="beeb8-133">The following components and operations are part of the XML Layer:</span></span>

-   [<span data-ttu-id="beeb8-134">Модуль записи XML</span><span class="sxs-lookup"><span data-stu-id="beeb8-134">XML Writer</span></span>](xml-writer.md)
-   [<span data-ttu-id="beeb8-135">Модуль чтения XML</span><span class="sxs-lookup"><span data-stu-id="beeb8-135">XML Reader</span></span>](xml-reader.md)
-   [<span data-ttu-id="beeb8-136">XML-буфер</span><span class="sxs-lookup"><span data-stu-id="beeb8-136">XML Buffer</span></span>](xml-buffer.md)
-   [<span data-ttu-id="beeb8-137">Сериализация</span><span class="sxs-lookup"><span data-stu-id="beeb8-137">Serialization</span></span>](serialization.md)
-   [<span data-ttu-id="beeb8-138">Поддержка языка XML</span><span class="sxs-lookup"><span data-stu-id="beeb8-138">XML Language Support</span></span>](xml-language-support.md)

## <a name="common-to-all-layers"></a><span data-ttu-id="beeb8-139">Общие для всех слоев</span><span class="sxs-lookup"><span data-stu-id="beeb8-139">Common to all layers</span></span>

<span data-ttu-id="beeb8-140">Ниже приведены разделы, которые относятся к любому из трех уровней.</span><span class="sxs-lookup"><span data-stu-id="beeb8-140">The following are topics that apply to any of the three layers:</span></span>

-   [<span data-ttu-id="beeb8-141">ошибки</span><span class="sxs-lookup"><span data-stu-id="beeb8-141">Errors</span></span>](errors.md)
-   [<span data-ttu-id="beeb8-142">Асинхронная модель</span><span class="sxs-lookup"><span data-stu-id="beeb8-142">Asynchronous Model</span></span>](asynchronous-model.md)
-   [<span data-ttu-id="beeb8-143">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="beeb8-143">Thread Safety</span></span>](thread-safety.md)
-   [<span data-ttu-id="beeb8-144">Трассировка</span><span class="sxs-lookup"><span data-stu-id="beeb8-144">Tracing</span></span>](tracing.md)
-   [<span data-ttu-id="beeb8-145">Отмена</span><span class="sxs-lookup"><span data-stu-id="beeb8-145">Cancellation</span></span>](cancellation.md)
-   [<span data-ttu-id="beeb8-146">Служебные программы</span><span class="sxs-lookup"><span data-stu-id="beeb8-146">Utilities</span></span>](utilities.md)
-   [<span data-ttu-id="beeb8-147">Отладка</span><span class="sxs-lookup"><span data-stu-id="beeb8-147">Debugging</span></span>](debugging.md)
-   [<span data-ttu-id="beeb8-148">Средство компилятора всутил</span><span class="sxs-lookup"><span data-stu-id="beeb8-148">Wsutil Compiler tool</span></span>](wsutil-compiler-tool.md)
-   [<span data-ttu-id="beeb8-149">Кучи</span><span class="sxs-lookup"><span data-stu-id="beeb8-149">Heap</span></span>](heap.md)

## <a name="examples"></a><span data-ttu-id="beeb8-150">Примеры</span><span class="sxs-lookup"><span data-stu-id="beeb8-150">Examples</span></span>

<span data-ttu-id="beeb8-151">Дополнительные сведения об элементах API см. в [справочнике по веб-службам Windows](windows-web-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="beeb8-151">For more information about API elements, see [Windows Web Services Reference](windows-web-services-reference.md).</span></span> <span data-ttu-id="beeb8-152">Примеры использования API см. в разделе [Использование веб-служб Windows](using-windows-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="beeb8-152">For examples of using the API, see [Using Windows Web Services](using-windows-web-services.md).</span></span>

 

 




