---
title: ошибки
description: В этом разделе описываются ошибки, которые могут быть вызваны функциями веб-служб Windows в результате сбоя выполнения команды.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Ошибки веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887935"
---
# <a name="errors"></a><span data-ttu-id="d55b6-106">ошибки</span><span class="sxs-lookup"><span data-stu-id="d55b6-106">Errors</span></span>

<span data-ttu-id="d55b6-107">В этом разделе описываются ошибки, которые могут быть вызваны функциями веб-служб Windows в результате сбоя выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="d55b6-107">This section outlines error that may be issues by Windows Web Services functions in result of a failure to execute the command.</span></span>

-   [<span data-ttu-id="d55b6-108">Выходные параметры</span><span class="sxs-lookup"><span data-stu-id="d55b6-108">Out Parameters</span></span>](#out-parameters)
-   [<span data-ttu-id="d55b6-109">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="d55b6-109">Error Codes</span></span>](#error-codes)
-   [<span data-ttu-id="d55b6-110">Подробные ошибки</span><span class="sxs-lookup"><span data-stu-id="d55b6-110">Rich Errors</span></span>](#rich-errors)
-   [<span data-ttu-id="d55b6-111">Сбои и ошибки</span><span class="sxs-lookup"><span data-stu-id="d55b6-111">Faults and Errors</span></span>](#faults-and-errors)
-   [<span data-ttu-id="d55b6-112">Сведения об ошибке, зависящие от языка</span><span class="sxs-lookup"><span data-stu-id="d55b6-112">Language Sensitive Error Information</span></span>](#language-sensitive-error-information)
-   [<span data-ttu-id="d55b6-113">Канонические коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d55b6-113">Canonical Error Codes</span></span>](#canonical-error-codes)
-   [<span data-ttu-id="d55b6-114">Недопустимое использование API</span><span class="sxs-lookup"><span data-stu-id="d55b6-114">Invalid API Usage</span></span>](#invalid-api-usage)
-   [<span data-ttu-id="d55b6-115">Безопасность</span><span class="sxs-lookup"><span data-stu-id="d55b6-115">Security</span></span>](#security)

## <a name="out-parameters"></a><span data-ttu-id="d55b6-116">Выходные параметры</span><span class="sxs-lookup"><span data-stu-id="d55b6-116">Out Parameters</span></span>

<span data-ttu-id="d55b6-117">Как правило, значения параметров out не изменяются при сбое функции.</span><span class="sxs-lookup"><span data-stu-id="d55b6-117">As a general rule, the value of out parameters are not modified if a function fails.</span></span>

<span data-ttu-id="d55b6-118">Существует несколько экземпляров, в которых параметры out изменяются в случае сбоя функции.</span><span class="sxs-lookup"><span data-stu-id="d55b6-118">There are a few instances where out parameters are modified if the function fails.</span></span> <span data-ttu-id="d55b6-119">Эти случаи явно вызываются в документации по каждому параметру.</span><span class="sxs-lookup"><span data-stu-id="d55b6-119">These cases are explicitly called out in the documentation for each parameter.</span></span> <span data-ttu-id="d55b6-120">Если в документации не упоминается ничего об изменении параметров out в случае сбоя, можно спокойно предположить, что функция не будет изменять их.</span><span class="sxs-lookup"><span data-stu-id="d55b6-120">If the documentation does not mention anything about modifying out parameters in the case of failure, then you can safely assume that the function will not modify them.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d55b6-121">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d55b6-121">Error Codes</span></span>

<span data-ttu-id="d55b6-122">Все коды возврата ошибок — HRESULTs.</span><span class="sxs-lookup"><span data-stu-id="d55b6-122">All error return codes are HRESULTs.</span></span> <span data-ttu-id="d55b6-123">Этот API определяет набор значений HRESULT в \_ диапазоне служебных служб, но также возвращает ошибки, определенные в других окнах Windows API.</span><span class="sxs-lookup"><span data-stu-id="d55b6-123">This API defines a set of HRESULTs in the FACILITY\_WEBSERVICES range, but also returns errors defined elsewhere in the Windows API.</span></span>

<span data-ttu-id="d55b6-124">Сведения о том, какие коды ошибок возвращаются, см. в документации по конкретным API.</span><span class="sxs-lookup"><span data-stu-id="d55b6-124">Refer to the documentation for specific API's to learn about which error codes are returned.</span></span> <span data-ttu-id="d55b6-125">Список не должен быть исчерпывающим для каждого API, а представляет собой список кодов ошибок, для которых существуют распространенные сценарии для явной обработки.</span><span class="sxs-lookup"><span data-stu-id="d55b6-125">The list is not intended to be exhaustive for each API, but rather a list of error codes for which there are common scenarios for explicit handling.</span></span> <span data-ttu-id="d55b6-126">Вызывающий объект всегда должен предположить, что другие коды ошибок возможны из любого API.</span><span class="sxs-lookup"><span data-stu-id="d55b6-126">A caller should always assume other error codes are possible from any API.</span></span>

<span data-ttu-id="d55b6-127">Этот API определяет относительно небольшое количество кодов ошибок, соответствующих сценариям, в которых программа будет предпринимать действия в зависимости от ошибки.</span><span class="sxs-lookup"><span data-stu-id="d55b6-127">This API defines a relatively small number of error codes, which correspond to scenarios where a program will want to take action based on the error.</span></span> <span data-ttu-id="d55b6-128">Только коды ошибок могут быть недостаточными для определения того, что пошло не так, или для предоставления хорошего описания проблемы пользователю.</span><span class="sxs-lookup"><span data-stu-id="d55b6-128">Error codes alone may not be sufficient in order to determine what went wrong, or in order to provide a good description of the problem to the user.</span></span> <span data-ttu-id="d55b6-129">Лучшее понимание проблемы состоит в использовании обширных ошибок, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="d55b6-129">The best understanding of the problem comes from using Rich Errors, as described below.</span></span>

## <a name="rich-errors"></a><span data-ttu-id="d55b6-130">Подробные ошибки</span><span class="sxs-lookup"><span data-stu-id="d55b6-130">Rich Errors</span></span>

<span data-ttu-id="d55b6-131">Кроме того, чтобы возвратить код ошибки, вызывающий объект может дополнительно запросить подробные сведения об ошибке для любого вызова API, передав объект [ \_ ошибки WS](ws-error.md) , отличный от **null**.</span><span class="sxs-lookup"><span data-stu-id="d55b6-131">In additional to returning an error code, a caller may optionally request rich error information for any API call by passing a non-**NULL**[WS\_ERROR](ws-error.md) object.</span></span> <span data-ttu-id="d55b6-132">Чтобы создать объект Error, используйте [**вскреатиррор**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror).</span><span class="sxs-lookup"><span data-stu-id="d55b6-132">To create an error object, use [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror).</span></span> <span data-ttu-id="d55b6-133">При возникновении ошибки API-интерфейс, вызвавший ошибку, будет заполнять объект ошибки дополнительным контекстом об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d55b6-133">If there is an error, then the API that caused the error will fill the error object with additional context about the error situation.</span></span> <span data-ttu-id="d55b6-134">Если ошибка отсутствует, объект Error не изменяется.</span><span class="sxs-lookup"><span data-stu-id="d55b6-134">If there is no error, then the error object is unmodified.</span></span> <span data-ttu-id="d55b6-135">Передача объекта ошибки **null** означает, что вызывающему объекту не нужны подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d55b6-135">Passing a **NULL** error object indicates that the caller is not interested in rich error information.</span></span> <span data-ttu-id="d55b6-136">Вызываемые (включая обратные вызовы) должен быть готов к обработке объектов ошибок **null** .</span><span class="sxs-lookup"><span data-stu-id="d55b6-136">Callees (including callbacks) must be prepared to handle **NULL** error objects.</span></span>

<span data-ttu-id="d55b6-137">Обратите внимание, что один и тот же объект Error может использоваться для нескольких вызовов API, но может использоваться только для одного вызова API за раз (как это происходит в одном потоке).</span><span class="sxs-lookup"><span data-stu-id="d55b6-137">Note that the same error object can be used for multiple API calls, but may only be used for one API call at a time (as it is single threaded).</span></span> <span data-ttu-id="d55b6-138">При каждом возникновении ошибки сведения об ошибке добавляются к объекту Error.</span><span class="sxs-lookup"><span data-stu-id="d55b6-138">Each time an error occurs, error information is appended to the error object.</span></span> <span data-ttu-id="d55b6-139">При очистке цепочки вызовов несколько функций могут добавлять сведения в объект Error, чтобы предоставить дополнительный контекст об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d55b6-139">As a call chain unwinds, multiple functions may add information to the error object to provide additional context about the error.</span></span> <span data-ttu-id="d55b6-140">Чтобы очистить содержимое объекта Error перед его повторным использованием (после возникновения ошибки), используйте [**всресетеррор**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror).</span><span class="sxs-lookup"><span data-stu-id="d55b6-140">To clear the contents of the error object before reusing it (after an error occurs), use [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror).</span></span> <span data-ttu-id="d55b6-141">Если ошибка не возникает, не нужно сбрасывать объект Error перед его повторным использованием.</span><span class="sxs-lookup"><span data-stu-id="d55b6-141">If no error occurs, it is not necessary to reset the error object before reusing it.</span></span>

<span data-ttu-id="d55b6-142">Подробные сведения об ошибке состоят из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="d55b6-142">Rich error information consists of the following:</span></span>

-   <span data-ttu-id="d55b6-143">Набор значений свойств, которые предоставляют дополнительные сведения об ошибке, если она есть.</span><span class="sxs-lookup"><span data-stu-id="d55b6-143">A set of property values, which provide additional information about the error if present.</span></span> <span data-ttu-id="d55b6-144">См. раздел [**\_ \_ свойства ошибки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).</span><span class="sxs-lookup"><span data-stu-id="d55b6-144">See [**WS\_ERROR\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).</span></span>
-   <span data-ttu-id="d55b6-145">Ноль или более строк ошибок.</span><span class="sxs-lookup"><span data-stu-id="d55b6-145">Zero or more error strings.</span></span> <span data-ttu-id="d55b6-146">Строки добавляются с помощью [**всаддеррорстринг**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring), и их можно запрашивать с помощью [**всжетеррорстринг**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring).</span><span class="sxs-lookup"><span data-stu-id="d55b6-146">The strings are added using [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring), and can be queried using using [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring).</span></span> <span data-ttu-id="d55b6-147">Количество строк можно запросить с помощью [**\_ строки свойства WS Error \_ \_ \_ Count**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span><span class="sxs-lookup"><span data-stu-id="d55b6-147">The number of strings can be queried using [**WS\_ERROR\_PROPERTY\_STRING\_COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span></span>

## <a name="faults-and-errors"></a><span data-ttu-id="d55b6-148">Сбои и ошибки</span><span class="sxs-lookup"><span data-stu-id="d55b6-148">Faults and Errors</span></span>

<span data-ttu-id="d55b6-149">Сведения о том, как связаны ошибки и сбои, см. в разделе [ошибки](faults.md) .</span><span class="sxs-lookup"><span data-stu-id="d55b6-149">See [Faults](faults.md) for information about how errors and faults relate.</span></span>

## <a name="language-sensitive-error-information"></a><span data-ttu-id="d55b6-150">Сведения об ошибке, зависящие от языка</span><span class="sxs-lookup"><span data-stu-id="d55b6-150">Language Sensitive Error Information</span></span>

<span data-ttu-id="d55b6-151">При создании объекта Error задается LANGID требуемого перевода языка для сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d55b6-151">When creating an error object, the LANGID of the desired language translation for error information is specified.</span></span> <span data-ttu-id="d55b6-152">Используется при добавлении сведений об ошибке в объект Error.</span><span class="sxs-lookup"><span data-stu-id="d55b6-152">This is used when adding error information to the error object.</span></span>

<span data-ttu-id="d55b6-153">Это значение языка можно получить или задать с помощью [**\_ Свойства WS \_ Error \_ LangID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span><span class="sxs-lookup"><span data-stu-id="d55b6-153">This language value can be retrieved or set using [**WS\_ERROR\_PROPERTY\_LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span></span>

## <a name="canonical-error-codes"></a><span data-ttu-id="d55b6-154">Канонические коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d55b6-154">Canonical Error Codes</span></span>

<span data-ttu-id="d55b6-155">Этот API предоставляет канонический набор кодов ошибок (WS \_ E \_ \* ), которые позволяют использовать различные коммуникационные технологии без необходимости зависеть от конкретных кодов ошибок конкретной базовой реализации.</span><span class="sxs-lookup"><span data-stu-id="d55b6-155">This API provides a canonical set of error codes (WS\_E\_\*) that allow for different communication technologies to be used without having to depend on the specific error codes of the specific underlying implementation.</span></span> <span data-ttu-id="d55b6-156">Полный список этих кодов ошибок см. в разделе [возвращаемые значения веб-служб Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d55b6-156">For a complete list of these error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="d55b6-157">Это позволяет, например, программе проверять наличие кода ошибки **WS \_ E, \_ \_ не \_ найден** ли он при использовании TCP, UDP или HTTP, и предпринимать какие-либо действия (например, пытаться использовать другую конечную точку).</span><span class="sxs-lookup"><span data-stu-id="d55b6-157">This allows, for example, a program to check for the error code **WS\_E\_ENDPOINT\_NOT\_FOUND** whether using TCP, UDP, or HTTP, and take some action (like attempting to use a different endpoint).</span></span>

<span data-ttu-id="d55b6-158">Если код ошибки конкретной реализации сопоставлен с канонической ошибкой, исходный код ошибки сохраняется в объекте Error и по-прежнему может быть доступен в целях диагностики.</span><span class="sxs-lookup"><span data-stu-id="d55b6-158">When an implementation specific error code is mapped to a canonical error, the original error code is saved in the error object, and may still be accessed for diagnostic purposes.</span></span> <span data-ttu-id="d55b6-159">Дополнительные сведения см. в разделе [**\_ свойство ошибки WS Error \_ \_ \_ \_ Code Error**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) .</span><span class="sxs-lookup"><span data-stu-id="d55b6-159">See [**WS\_ERROR\_PROPERTY\_ORIGINAL\_ERROR\_CODE**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) for more information.</span></span>

## <a name="invalid-api-usage"></a><span data-ttu-id="d55b6-160">Недопустимое использование API</span><span class="sxs-lookup"><span data-stu-id="d55b6-160">Invalid API Usage</span></span>

<span data-ttu-id="d55b6-161">Следующие коды ошибок зарезервированы для недопустимого использования API и не будут возвращаться в других обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="d55b6-161">The following error codes are reserved for invalid API usage, and will not be returned in other circumstances.</span></span> <span data-ttu-id="d55b6-162">Если любая из этих ошибок возвращена, это может указывать на ошибку приложения.</span><span class="sxs-lookup"><span data-stu-id="d55b6-162">If any of these errors are returned it may be an indication of an application bug.</span></span>

-   <span data-ttu-id="d55b6-163">**\_ \_ Недопустимая операция WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-163">**WS\_E\_INVALID\_OPERATION**</span></span>
-   <span data-ttu-id="d55b6-164">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="d55b6-164">**E\_INVALIDARG**</span></span>

<span data-ttu-id="d55b6-165">Следующие перечисления являются частью трассировки:</span><span class="sxs-lookup"><span data-stu-id="d55b6-165">The following enumerations are part of tracing:</span></span>

-   [<span data-ttu-id="d55b6-166">**\_ \_ идентификатор свойства ошибки \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d55b6-166">**WS\_ERROR\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [<span data-ttu-id="d55b6-167">**\_код исключения \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d55b6-167">**WS\_EXCEPTION\_CODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

<span data-ttu-id="d55b6-168">Следующие коды ошибок являются частью трассировки:</span><span class="sxs-lookup"><span data-stu-id="d55b6-168">The following error codes are part of tracing:</span></span>

-   <span data-ttu-id="d55b6-169">**СЕРТИФИКАТ \_ E \_ CN \_ без \_ совпадения**</span><span class="sxs-lookup"><span data-stu-id="d55b6-169">**CERT\_E\_CN\_NO\_MATCH**</span></span>
-   <span data-ttu-id="d55b6-170">**\_ \_ истек срок действия сертификата E**</span><span class="sxs-lookup"><span data-stu-id="d55b6-170">**CERT\_E\_EXPIRED**</span></span>
-   <span data-ttu-id="d55b6-171">**CERT \_ E \_ унтрустедрут**</span><span class="sxs-lookup"><span data-stu-id="d55b6-171">**CERT\_E\_UNTRUSTEDROOT**</span></span>
-   <span data-ttu-id="d55b6-172">**\_ \_ неправильное \_ Использование CERT E**</span><span class="sxs-lookup"><span data-stu-id="d55b6-172">**CERT\_E\_WRONG\_USAGE**</span></span>
-   <span data-ttu-id="d55b6-173">**дешифрование \_ \_ отзыва в \_ автономном режиме**</span><span class="sxs-lookup"><span data-stu-id="d55b6-173">**CRYPT\_E\_REVOCATION\_OFFLINE**</span></span>
-   <span data-ttu-id="d55b6-174">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="d55b6-174">**E\_INVALIDARG**</span></span>
-   <span data-ttu-id="d55b6-175">**E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="d55b6-175">**E\_OUTOFMEMORY**</span></span>
-   <span data-ttu-id="d55b6-176">**\_ \_ используемый адрес WS \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-176">**WS\_E\_ADDRESS\_IN\_USE**</span></span>
-   <span data-ttu-id="d55b6-177">**\_адрес WS \_ E \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="d55b6-177">**WS\_E\_ADDRESS\_NOT\_AVAILABLE**</span></span>
-   <span data-ttu-id="d55b6-178">**\_ \_ \_ отказано в доступе к конечной точке WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-178">**WS\_E\_ENDPOINT\_ACCESS\_DENIED**</span></span>
-   <span data-ttu-id="d55b6-179">**\_ \_ действие КОНЕЧНОЙ точки WS E \_ \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="d55b6-179">**WS\_E\_ENDPOINT\_ACTION\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="d55b6-180">**\_ \_ Конечная точка WS E \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="d55b6-180">**WS\_E\_ENDPOINT\_DISCONNECTED**</span></span>
-   <span data-ttu-id="d55b6-181">**\_ \_ сбой КОНЕЧНОЙ точки WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-181">**WS\_E\_ENDPOINT\_FAILURE**</span></span>
-   <span data-ttu-id="d55b6-182">**\_ \_ получена ошибка КОНЕЧНОЙ точки WS E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-182">**WS\_E\_ENDPOINT\_FAULT\_RECEIVED**</span></span>
-   <span data-ttu-id="d55b6-183">**\_ \_ Конечная точка WS E \_ \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="d55b6-183">**WS\_E\_ENDPOINT\_NOT\_AVAILABLE**</span></span>
-   <span data-ttu-id="d55b6-184">**\_ \_ Конечная точка WS E \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="d55b6-184">**WS\_E\_ENDPOINT\_NOT\_FOUND**</span></span>
-   <span data-ttu-id="d55b6-185">**\_ \_ Конечная точка WS E \_ слишком \_ занята**</span><span class="sxs-lookup"><span data-stu-id="d55b6-185">**WS\_E\_ENDPOINT\_TOO\_BUSY**</span></span>
-   <span data-ttu-id="d55b6-186">**\_ \_ Конечная точка WS E \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="d55b6-186">**WS\_E\_ENDPOINT\_UNREACHABLE**</span></span>
-   <span data-ttu-id="d55b6-187">**\_ \_ Недопустимый \_ \_ URL-адрес конечной точки WS E**</span><span class="sxs-lookup"><span data-stu-id="d55b6-187">**WS\_E\_INVALID\_ENDPOINT\_URL**</span></span>
-   <span data-ttu-id="d55b6-188">**\_ \_ Недопустимый \_ Формат WS E**</span><span class="sxs-lookup"><span data-stu-id="d55b6-188">**WS\_E\_INVALID\_FORMAT**</span></span>
-   <span data-ttu-id="d55b6-189">**\_ \_ Недопустимая операция WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-189">**WS\_E\_INVALID\_OPERATION**</span></span>
-   <span data-ttu-id="d55b6-190">**WS \_ E \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="d55b6-190">**WS\_E\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="d55b6-191">**\_ \_ нет \_ доступных переводов WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-191">**WS\_E\_NO\_TRANSLATION\_AVAILABLE**</span></span>
-   <span data-ttu-id="d55b6-192">**\_ \_ переполнение числового значения WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-192">**WS\_E\_NUMERIC\_OVERFLOW**</span></span>
-   <span data-ttu-id="d55b6-193">**\_ \_ сбой объекта WS \_ E**</span><span class="sxs-lookup"><span data-stu-id="d55b6-193">**WS\_E\_OBJECT\_FAULTED**</span></span>
-   <span data-ttu-id="d55b6-194">**\_Операция WS \_ E \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="d55b6-194">**WS\_E\_OPERATION\_ABANDONED**</span></span>
-   <span data-ttu-id="d55b6-195">**\_Операция WS \_ E \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="d55b6-195">**WS\_E\_OPERATION\_ABORTED**</span></span>
-   <span data-ttu-id="d55b6-196">**\_ \_ \_ время \_ ожидания операции WS E истекло**</span><span class="sxs-lookup"><span data-stu-id="d55b6-196">**WS\_E\_OPERATION\_TIMED\_OUT**</span></span>
-   <span data-ttu-id="d55b6-197">**Прочие службы WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-197">**WS\_E\_OTHER**</span></span>
-   <span data-ttu-id="d55b6-198">**\_ \_ \_ отказано в доступе к прокси-серверу WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-198">**WS\_E\_PROXY\_ACCESS\_DENIED**</span></span>
-   <span data-ttu-id="d55b6-199">**\_ \_ Сбой прокси-сервера WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-199">**WS\_E\_PROXY\_FAILURE**</span></span>
-   <span data-ttu-id="d55b6-200">**для \_ \_ прокси-сервера WS E \_ требуется \_ Обычная \_ Проверка подлинности**</span><span class="sxs-lookup"><span data-stu-id="d55b6-200">**WS\_E\_PROXY\_REQUIRES\_BASIC\_AUTH**</span></span>
-   <span data-ttu-id="d55b6-201">**для \_ \_ прокси-сервера WS E \_ требуется \_ Краткая \_ Проверка подлинности**</span><span class="sxs-lookup"><span data-stu-id="d55b6-201">**WS\_E\_PROXY\_REQUIRES\_DIGEST\_AUTH**</span></span>
-   <span data-ttu-id="d55b6-202">**для \_ \_ прокси-сервера WS E \_ требуется \_ \_ Проверка подлинности согласования**</span><span class="sxs-lookup"><span data-stu-id="d55b6-202">**WS\_E\_PROXY\_REQUIRES\_NEGOTIATE\_AUTH**</span></span>
-   <span data-ttu-id="d55b6-203">**для \_ \_ прокси-сервера WS E \_ требуется \_ \_ Проверка подлинности NTLM**</span><span class="sxs-lookup"><span data-stu-id="d55b6-203">**WS\_E\_PROXY\_REQUIRES\_NTLM\_AUTH**</span></span>
-   <span data-ttu-id="d55b6-204">**\_ \_ превышена квота WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-204">**WS\_E\_QUOTA\_EXCEEDED**</span></span>
-   <span data-ttu-id="d55b6-205">**\_ \_ \_ сбой системы безопасности WS \_ E**</span><span class="sxs-lookup"><span data-stu-id="d55b6-205">**WS\_E\_SECURITY\_SYSTEM\_FAILURE**</span></span>
-   <span data-ttu-id="d55b6-206">**\_ \_ \_ истек срок действия токена безопасности WS E \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-206">**WS\_E\_SECURITY\_TOKEN\_EXPIRED**</span></span>
-   <span data-ttu-id="d55b6-207">**\_ \_ \_ сбой проверки безопасности WS \_ E**</span><span class="sxs-lookup"><span data-stu-id="d55b6-207">**WS\_E\_SECURITY\_VERIFICATION\_FAILURE**</span></span>
-   <span data-ttu-id="d55b6-208">**для \_ сервера WS E \_ \_ требуется \_ Обычная \_ Проверка подлинности**</span><span class="sxs-lookup"><span data-stu-id="d55b6-208">**WS\_E\_SERVER\_REQUIRES\_BASIC\_AUTH**</span></span>
-   <span data-ttu-id="d55b6-209">**для \_ сервера WS E \_ \_ требуется \_ дайджест- \_ Проверка подлинности**</span><span class="sxs-lookup"><span data-stu-id="d55b6-209">**WS\_E\_SERVER\_REQUIRES\_DIGEST\_AUTH**</span></span>
-   <span data-ttu-id="d55b6-210">**\_сервер WS \_ E \_ требует \_ \_ проверки подлинности согласования**</span><span class="sxs-lookup"><span data-stu-id="d55b6-210">**WS\_E\_SERVER\_REQUIRES\_NEGOTIATE\_AUTH**</span></span>
-   <span data-ttu-id="d55b6-211">**для \_ сервера WS E \_ \_ требуется \_ \_ Проверка подлинности NTLM**</span><span class="sxs-lookup"><span data-stu-id="d55b6-211">**WS\_E\_SERVER\_REQUIRES\_NTLM\_AUTH**</span></span>
-   <span data-ttu-id="d55b6-212">**WS \_ S — \_ асинхронный**</span><span class="sxs-lookup"><span data-stu-id="d55b6-212">**WS\_S\_ASYNC**</span></span>
-   <span data-ttu-id="d55b6-213">**\_конец WS S \_**</span><span class="sxs-lookup"><span data-stu-id="d55b6-213">**WS\_S\_END**</span></span>

<span data-ttu-id="d55b6-214">Следующие функции являются частью трассировки:</span><span class="sxs-lookup"><span data-stu-id="d55b6-214">The following functions are part of tracing:</span></span>

-   [<span data-ttu-id="d55b6-215">**\_ \_ идентификатор свойства ошибки \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d55b6-215">**WS\_ERROR\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [<span data-ttu-id="d55b6-216">**\_код исключения \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d55b6-216">**WS\_EXCEPTION\_CODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

<span data-ttu-id="d55b6-217">В трассировку входит следующий маркер:</span><span class="sxs-lookup"><span data-stu-id="d55b6-217">The following handle is part of tracing:</span></span>

-   [<span data-ttu-id="d55b6-218">\_Ошибка WS</span><span class="sxs-lookup"><span data-stu-id="d55b6-218">WS\_ERROR</span></span>](ws-error.md)

<span data-ttu-id="d55b6-219">Следующая структура является частью трассировки:</span><span class="sxs-lookup"><span data-stu-id="d55b6-219">The following structure is part of tracing:</span></span>

-   [<span data-ttu-id="d55b6-220">**WS \_ Error, \_ свойство**</span><span class="sxs-lookup"><span data-stu-id="d55b6-220">**WS\_ERROR\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a><span data-ttu-id="d55b6-221">Безопасность</span><span class="sxs-lookup"><span data-stu-id="d55b6-221">Security</span></span>

<span data-ttu-id="d55b6-222">Существует ряд вопросов безопасности, которые следует учитывать пользователю объекта Error.</span><span class="sxs-lookup"><span data-stu-id="d55b6-222">There are a number of security considerations that the user of the error object should be aware of:</span></span>

-   <span data-ttu-id="d55b6-223">Объект Error может содержать ненадежные данные.</span><span class="sxs-lookup"><span data-stu-id="d55b6-223">The error object may contain untrusted data.</span></span> <span data-ttu-id="d55b6-224">Примеры: ошибки WS \_ и строки ошибок, которые могут храниться в объекте Error на основе данных, полученных по ненадежному каналу.</span><span class="sxs-lookup"><span data-stu-id="d55b6-224">Examples of this are: the WS\_FAULT, and the error strings, both of which can be stored in the error object based on information received over an untrusted channel.</span></span> <span data-ttu-id="d55b6-225">При проверке сведений в объекте Error и принятии решений на основе его значений необходимо соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="d55b6-225">The user of the error object should be careful when inspecting the information in the error object and making decisions based on its values.</span></span>
-   <span data-ttu-id="d55b6-226">Пользователь объекта Error должен вызвать [**всресетеррор**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) после проверки сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d55b6-226">A user of the error object should call [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) after inspecting the information about the error.</span></span> <span data-ttu-id="d55b6-227">Если этого не сделать, это может привести к накоплению памяти.</span><span class="sxs-lookup"><span data-stu-id="d55b6-227">Failing to do so can lead to memory accumulation.</span></span>
-   <span data-ttu-id="d55b6-228">Пользователь объекта ошибки должен быть очень осторожным при использовании \_ значения перекрытия "WS Full" \_ \_ в перечислении ошибок [**WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) , поскольку сформированная ошибка может содержать частные сведения, накопленные в ходе процесса записи ошибок.</span><span class="sxs-lookup"><span data-stu-id="d55b6-228">A user of the error object should be very careful when using the WS\_FULL\_FAULT\_DISCLOSURE value of the [**WS\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) enumeration, because the generated fault could contain private information that was accumulated as part of the error recording process.</span></span>

 

 




