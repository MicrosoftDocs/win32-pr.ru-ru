---
title: IDXCoreAdapterList::GetAdapter
description: Извлекает конкретный адаптер по индексу из объекта списка адаптеров Дкскоре.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070431"
---
# <a name="idxcoreadapterlistgetadapter-method"></a><span data-ttu-id="c38a1-103">Метод Идкскореадаптерлист:: Adapter</span><span class="sxs-lookup"><span data-stu-id="c38a1-103">IDXCoreAdapterList::GetAdapter method</span></span>

<span data-ttu-id="c38a1-104">Извлекает конкретный адаптер по индексу из объекта списка адаптеров Дкскоре.</span><span class="sxs-lookup"><span data-stu-id="c38a1-104">Retrieves a specific adapter by index from a DXCore adapter list object.</span></span> <span data-ttu-id="c38a1-105">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="c38a1-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c38a1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c38a1-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="c38a1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c38a1-107">Parameters</span></span>

### <a name="index"></a><span data-ttu-id="c38a1-108">index</span><span class="sxs-lookup"><span data-stu-id="c38a1-108">index</span></span>

<span data-ttu-id="c38a1-109">Тип: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="c38a1-109">Type: **uint32_t**</span></span>

<span data-ttu-id="c38a1-110">Отсчитываемый от нуля индекс, идентифицирующий экземпляр адаптера в списке адаптеров Дкскоре.</span><span class="sxs-lookup"><span data-stu-id="c38a1-110">A zero-based index, identifying an adapter instance within the DXCore adapter list.</span></span>

### <a name="riid"></a><span data-ttu-id="c38a1-111">riid</span><span class="sxs-lookup"><span data-stu-id="c38a1-111">riid</span></span>

<span data-ttu-id="c38a1-112">Тип: **рефиид**</span><span class="sxs-lookup"><span data-stu-id="c38a1-112">Type: **REFIID**</span></span>

<span data-ttu-id="c38a1-113">Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в *ппвадаптер*.</span><span class="sxs-lookup"><span data-stu-id="c38a1-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="c38a1-114">Это должен быть идентификатор интерфейса (IID) [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="c38a1-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="c38a1-115">Ппвадаптер [out]</span><span class="sxs-lookup"><span data-stu-id="c38a1-115">ppvAdapter [out]</span></span>

<span data-ttu-id="c38a1-116">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="c38a1-116">Type: **void\*\***</span></span>

<span data-ttu-id="c38a1-117">Адрес указателя на интерфейс с идентификатором IID, указанным в параметре *riid* .</span><span class="sxs-lookup"><span data-stu-id="c38a1-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="c38a1-118">После успешного возврата *\* ппвадаптер* (адрес разыменования) содержит указатель на созданный адаптер дкскоре.</span><span class="sxs-lookup"><span data-stu-id="c38a1-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="c38a1-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c38a1-119">Returns</span></span>

<span data-ttu-id="c38a1-120">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="c38a1-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="c38a1-121">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="c38a1-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="c38a1-122">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c38a1-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="c38a1-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c38a1-123">Return value</span></span>|<span data-ttu-id="c38a1-124">Описание</span><span class="sxs-lookup"><span data-stu-id="c38a1-124">Description</span></span>|
|-|-|
|<span data-ttu-id="c38a1-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="c38a1-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="c38a1-126">*Индекс* действителен, но адаптер больше не находится в допустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="c38a1-126">The *index* is valid, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="c38a1-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c38a1-127">E_INVALIDARG</span></span>|<span data-ttu-id="c38a1-128">Указан недопустимый *индекс* .</span><span class="sxs-lookup"><span data-stu-id="c38a1-128">The provided *index* is not valid.</span></span>|
|<span data-ttu-id="c38a1-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="c38a1-129">E_NOINTERFACE</span></span>|<span data-ttu-id="c38a1-130">Указано недопустимое значение для *riid*.</span><span class="sxs-lookup"><span data-stu-id="c38a1-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="c38a1-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="c38a1-131">E_POINTER</span></span>|<span data-ttu-id="c38a1-132">`nullptr` был предоставлен для *ппвадаптер*.</span><span class="sxs-lookup"><span data-stu-id="c38a1-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c38a1-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c38a1-133">Remarks</span></span>

<span data-ttu-id="c38a1-134">Несколько вызовов, передающих индекс, представляющий тот же адаптер, возвращают идентичные указатели интерфейса, даже в разных списках адаптеров.</span><span class="sxs-lookup"><span data-stu-id="c38a1-134">Multiple calls passing an index that represents the same adapter return identical interface pointers, even across different adapter lists.</span></span> <span data-ttu-id="c38a1-135">В результате можно сравнивать указатели интерфейса, чтобы определить, ссылаются ли несколько указателей на один и тот же объект адаптера.</span><span class="sxs-lookup"><span data-stu-id="c38a1-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="c38a1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c38a1-136">See also</span></span>

<span data-ttu-id="c38a1-137">[Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="c38a1-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>