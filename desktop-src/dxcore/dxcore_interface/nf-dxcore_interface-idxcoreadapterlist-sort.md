---
title: IDXCoreAdapterList::Sort
description: Сортирует объект списка адаптеров Дкскоре на основе предоставленного входного массива критериев сортировки.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134430"
---
# <a name="idxcoreadapterlistsort-method"></a><span data-ttu-id="88e1b-103">Метод Идкскореадаптерлист:: Sort</span><span class="sxs-lookup"><span data-stu-id="88e1b-103">IDXCoreAdapterList::Sort method</span></span>

## <a name="description"></a><span data-ttu-id="88e1b-104">Описание</span><span class="sxs-lookup"><span data-stu-id="88e1b-104">Description</span></span>

<span data-ttu-id="88e1b-105">Сортирует объект списка адаптеров Дкскоре на основе предоставленного входного массива критериев сортировки, где элементы массива ранее в массиве критериев имеют более высокий вес.</span><span class="sxs-lookup"><span data-stu-id="88e1b-105">Sorts a DXCore adapter list object based on a provided input array of sort criteria, where array items earlier in the array of criteria are given a higher weight.</span></span> <span data-ttu-id="88e1b-106">**Сортировка** помогает легко найти идеальный адаптер в списке адаптеров.</span><span class="sxs-lookup"><span data-stu-id="88e1b-106">**Sort** helps you to more easily find your ideal adapter in an adapter list.</span></span>

## <a name="syntax"></a><span data-ttu-id="88e1b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88e1b-107">Syntax</span></span>

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a><span data-ttu-id="88e1b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="88e1b-108">Parameters</span></span>

### <a name="numpreferences"></a><span data-ttu-id="88e1b-109">нумпреференцес</span><span class="sxs-lookup"><span data-stu-id="88e1b-109">numPreferences</span></span>

<span data-ttu-id="88e1b-110">Тип: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="88e1b-110">Type: **uint32_t**</span></span>

<span data-ttu-id="88e1b-111">Количество элементов в массиве, на которое указывает параметр *Preferences* .</span><span class="sxs-lookup"><span data-stu-id="88e1b-111">The number of elements that are in the array pointed to by the *preferences* parameter.</span></span>

### <a name="preferences-in"></a><span data-ttu-id="88e1b-112">предпочтения [в]</span><span class="sxs-lookup"><span data-stu-id="88e1b-112">preferences [in]</span></span>

<span data-ttu-id="88e1b-113">Тип: **const [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) \***</span><span class="sxs-lookup"><span data-stu-id="88e1b-113">Type: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)\***</span></span>

<span data-ttu-id="88e1b-114">Указатель на константный массив значений [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) , представляющих критерий сортировки.</span><span class="sxs-lookup"><span data-stu-id="88e1b-114">A pointer to a constant array of [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) values, representing sort criteria.</span></span>

## <a name="returns"></a><span data-ttu-id="88e1b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88e1b-115">Returns</span></span>

<span data-ttu-id="88e1b-116">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="88e1b-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="88e1b-117">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="88e1b-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="88e1b-118">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="88e1b-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="88e1b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88e1b-119">Return value</span></span>|<span data-ttu-id="88e1b-120">Описание</span><span class="sxs-lookup"><span data-stu-id="88e1b-120">Description</span></span>|
|-|-|
|<span data-ttu-id="88e1b-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="88e1b-121">E_INVALIDARG</span></span>|<span data-ttu-id="88e1b-122">Аргумент *нумпреференцес* равен нулю, либо аргументу *Preferences* является `nullptr` .</span><span class="sxs-lookup"><span data-stu-id="88e1b-122">The *numPreferences* argument is zero, or the *preferences* argument is `nullptr`.</span></span>|

## <a name="remarks"></a><span data-ttu-id="88e1b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88e1b-123">Remarks</span></span>

<span data-ttu-id="88e1b-124">В случаях, когда указанное значение [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) не распознается операционной системой (ОС), оно игнорируется и не приводит к сбою API.</span><span class="sxs-lookup"><span data-stu-id="88e1b-124">In cases where a provided [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value isn't recognized by the operating system (OS), it is ignored, and won't cause the API to fail.</span></span> <span data-ttu-id="88e1b-125">Известные значения **дкскореадаптерпреференце** по-прежнему будут учитываться в этом случае.</span><span class="sxs-lookup"><span data-stu-id="88e1b-125">Known **DXCoreAdapterPreference** values will still be considered in this case.</span></span> <span data-ttu-id="88e1b-126">Чтобы определить, понят ли тип сортировки для API, вызовите метод [идкскореадаптерлист:: исадаптерпреференцесуппортед](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="88e1b-126">To determine whether a sort type is understood by the API, call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

<span data-ttu-id="88e1b-127">Значения **дкскореадаптерпреференце** , которые происходят ранее в предоставленном массиве *предпочтений* , обрабатываются с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="88e1b-127">**DXCoreAdapterPreference** values that occur earlier in the provided *preferences* array are treated with higher priority.</span></span> 

<span data-ttu-id="88e1b-128">Дополнительные сведения о том, какая логика применяется к каждому типу, см. в документации по перечислению **дкскореадаптерпреференце** .</span><span class="sxs-lookup"><span data-stu-id="88e1b-128">Refer to the **DXCoreAdapterPreference** enumeration documentation for details about what logic is applied for each type.</span></span> <span data-ttu-id="88e1b-129">Внутренняя логика типа может разрабатываться по мере разработки ОС.</span><span class="sxs-lookup"><span data-stu-id="88e1b-129">The internal logic for a type may develop as the OS develops.</span></span>

<span data-ttu-id="88e1b-130">При **сортировке** элементы списка адаптеров дкскоре будут отсортированы от наиболее предпочтительных до наименьшего.</span><span class="sxs-lookup"><span data-stu-id="88e1b-130">When **Sort** returns, items in the DXCore adapter list will have been sorted from most preferable to least preferable.</span></span> <span data-ttu-id="88e1b-131">Таким образом, вызов [идкскореадаптерлист:: Adapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) с индексом 0 получает адаптер, который наилучшим образом соответствует запрошенным типам предпочтений сортировки. индекс 1 — это следующее лучшее соответствие и т. д.</span><span class="sxs-lookup"><span data-stu-id="88e1b-131">So, calling [IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) with index 0 retrieves the adapter that best matches the requested sort preference types; index 1 is the next best match, and so on.</span></span>

## <a name="see-also"></a><span data-ttu-id="88e1b-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88e1b-132">See also</span></span>

<span data-ttu-id="88e1b-133">[Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="88e1b-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>