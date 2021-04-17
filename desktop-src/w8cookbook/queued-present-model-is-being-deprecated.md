---
title: Текущая модель в очереди устарела
description: Текущая модель в очереди устарела
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "105700973"
---
# <a name="queued-present-model-is-being-deprecated"></a><span data-ttu-id="41bf3-103">Текущая модель в очереди устарела</span><span class="sxs-lookup"><span data-stu-id="41bf3-103">Queued present model is being deprecated</span></span>

## <a name="platforms"></a><span data-ttu-id="41bf3-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="41bf3-104">Platforms</span></span>

<span data-ttu-id="41bf3-105">**Клиенты** — после Windows 8</span><span class="sxs-lookup"><span data-stu-id="41bf3-105">**Clients** – After Windows 8</span></span>  
<span data-ttu-id="41bf3-106">**Серверы** — после Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="41bf3-106">**Servers** – After Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="41bf3-107">Описание</span><span class="sxs-lookup"><span data-stu-id="41bf3-107">Description</span></span>

<span data-ttu-id="41bf3-108">В выпуске Windows после Windows 8 эти API-интерфейсы будут возвращать E \_ нотимпл:</span><span class="sxs-lookup"><span data-stu-id="41bf3-108">In the Windows release after Windows 8, these APIs will return E\_NOTIMPL:</span></span>

-   <span data-ttu-id="41bf3-109">двмсетпресентпараметерс</span><span class="sxs-lookup"><span data-stu-id="41bf3-109">DwmSetPresentParameters</span></span>
-   <span data-ttu-id="41bf3-110">двмсетдксфрамедуратион</span><span class="sxs-lookup"><span data-stu-id="41bf3-110">DwmSetDxFrameDuration</span></span>
-   <span data-ttu-id="41bf3-111">двммодифипревиаусдксфрамедуратион</span><span class="sxs-lookup"><span data-stu-id="41bf3-111">DwmModifyPreviousDxFrameDuration</span></span>

<span data-ttu-id="41bf3-112">Кроме того, этот API принимает только значение NULL для параметра HWND:</span><span class="sxs-lookup"><span data-stu-id="41bf3-112">In addition, this API will only accept the NULL value for the hwnd parameter:</span></span>

-   <span data-ttu-id="41bf3-113">двмжеткомпоситионтимингинфо</span><span class="sxs-lookup"><span data-stu-id="41bf3-113">DwmGetCompositionTimingInfo</span></span>

<span data-ttu-id="41bf3-114">Мы будем прекращать поддержку Двмжеткомпоситионтимингинфо с HWND! = NULL и удалим связанные функции.</span><span class="sxs-lookup"><span data-stu-id="41bf3-114">We will stop supporting DwmGetCompositionTimingInfo with hwnd != NULL and remove associated functionality.</span></span> <span data-ttu-id="41bf3-115">Если указано значение HWND, отличное от NULL, этот API вернет E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="41bf3-115">If non-NULL value for hwnd is specified, this API will return E\_INVALIDARG.</span></span>

<span data-ttu-id="41bf3-116">Мы также рекомендуем использовать API Двмжеткомпоситионтимингинфо и предлагать, что разработчики переключаются на модель перелистывания DXGI и соответствующий API статистики DX Present.</span><span class="sxs-lookup"><span data-stu-id="41bf3-116">We also discourage the use of DwmGetCompositionTimingInfo API and suggest that developers switch to the DXGI flip model and associated DX present statistics API.</span></span>

## <a name="manifestation"></a><span data-ttu-id="41bf3-117">Проявление</span><span class="sxs-lookup"><span data-stu-id="41bf3-117">Manifestation</span></span>

<span data-ttu-id="41bf3-118">Приложения, использующие поставленную в очередь модель, будут работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="41bf3-118">Applications that use the queued present model will not function correctly.</span></span> <span data-ttu-id="41bf3-119">Точный уровень манифеста зависит от конкретного приложения, но может варьироваться от неправильного времени презентации при неожиданном выходе приложения.</span><span class="sxs-lookup"><span data-stu-id="41bf3-119">The exact manifestation depends on the particular application, but can range from incorrect presentation timing to the application exiting unexpectedly).</span></span> <span data-ttu-id="41bf3-120">На практике мы не будем видеть многие (если они есть) такие приложения.</span><span class="sxs-lookup"><span data-stu-id="41bf3-120">In practice, we do not expect to see many (if any) such applications.</span></span> <span data-ttu-id="41bf3-121">Эта модель использовалась проигрывателем Windows Media Player, которая не будет использоваться в ОС Microsoft Vista (и, возможно, в старом проигрывателе Zune).</span><span class="sxs-lookup"><span data-stu-id="41bf3-121">This model was used by Vista media player, which will not be used on Windows 8 (and possibly the old Zune player).</span></span> <span data-ttu-id="41bf3-122">В настоящее время у нас нет сведений о других приложениях, фактически использующих эту модель.</span><span class="sxs-lookup"><span data-stu-id="41bf3-122">At this time we don’t have info about any other applications actually using this model.</span></span>

## <a name="solution"></a><span data-ttu-id="41bf3-123">Решение</span><span class="sxs-lookup"><span data-stu-id="41bf3-123">Solution</span></span>

<span data-ttu-id="41bf3-124">Разработчикам необходимо использовать режим представления DXGI representation, а не в очереди (доступен в среде выполнения DX9 с момента выпуска Windows 7, а также в средах выполнения СОДЕРЖИМЫМ DX10 и DX11 в Windows 8).</span><span class="sxs-lookup"><span data-stu-id="41bf3-124">Developers need to use the DXGI flip presentation mode instead of queued present (available in DX9 runtime since Windows 7, and on DX10 and DX11 runtimes in Windows 8).</span></span>

## <a name="tests"></a><span data-ttu-id="41bf3-125">Тесты</span><span class="sxs-lookup"><span data-stu-id="41bf3-125">Tests</span></span>

<span data-ttu-id="41bf3-126">Выполните общие тесты, чтобы убедиться, что входящие компоненты Windows и основные продукты продолжают работать в следующей версии Windows.</span><span class="sxs-lookup"><span data-stu-id="41bf3-126">Run general tests to ensure that inbox Windows components and major products continue to work on the next version of Windows.</span></span>

 

 




