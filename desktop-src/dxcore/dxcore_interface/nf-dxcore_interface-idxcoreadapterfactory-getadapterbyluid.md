---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Возвращает объект адаптера Дкскоре ([идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md)) для указанного LUID, если он доступен.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413387"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a><span data-ttu-id="b0792-103">Метод Идкскореадаптерфактори:: Жетадаптербилуид</span><span class="sxs-lookup"><span data-stu-id="b0792-103">IDXCoreAdapterFactory::GetAdapterByLuid method</span></span>

<span data-ttu-id="b0792-104">Возвращает объект адаптера Дкскоре ([идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md)) для указанного LUID, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="b0792-104">Retrieves the DXCore adapter object ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) for a specified LUID, if available.</span></span> <span data-ttu-id="b0792-105">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="b0792-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0792-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0792-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="b0792-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0792-107">Parameters</span></span>

### <a name="adapterluid"></a><span data-ttu-id="b0792-108">адаптерлуид</span><span class="sxs-lookup"><span data-stu-id="b0792-108">adapterLUID</span></span>

<span data-ttu-id="b0792-109">Тип: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span><span class="sxs-lookup"><span data-stu-id="b0792-109">Type: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span></span>

<span data-ttu-id="b0792-110">Локально уникальное значение, идентифицирующее экземпляр адаптера.</span><span class="sxs-lookup"><span data-stu-id="b0792-110">The locally unique value that identifies the adapter instance.</span></span>

### <a name="riid-in"></a><span data-ttu-id="b0792-111">riid [in]</span><span class="sxs-lookup"><span data-stu-id="b0792-111">riid [in]</span></span>

<span data-ttu-id="b0792-112">Тип: **рефиид**</span><span class="sxs-lookup"><span data-stu-id="b0792-112">Type: **REFIID**</span></span>

<span data-ttu-id="b0792-113">Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в *ппвадаптер*.</span><span class="sxs-lookup"><span data-stu-id="b0792-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="b0792-114">Это должен быть идентификатор интерфейса (IID) [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="b0792-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="b0792-115">Ппвадаптер [out]</span><span class="sxs-lookup"><span data-stu-id="b0792-115">ppvAdapter [out]</span></span>

<span data-ttu-id="b0792-116">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="b0792-116">Type: **void\*\***</span></span>

<span data-ttu-id="b0792-117">Адрес указателя на интерфейс с идентификатором IID, указанным в параметре *riid* .</span><span class="sxs-lookup"><span data-stu-id="b0792-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="b0792-118">После успешного возврата *\* ппвадаптер* (адрес разыменования) содержит указатель на созданный адаптер дкскоре.</span><span class="sxs-lookup"><span data-stu-id="b0792-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="b0792-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0792-119">Returns</span></span>

<span data-ttu-id="b0792-120">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="b0792-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="b0792-121">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="b0792-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="b0792-122">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="b0792-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="b0792-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0792-123">Return value</span></span>|<span data-ttu-id="b0792-124">Описание</span><span class="sxs-lookup"><span data-stu-id="b0792-124">Description</span></span>|
|-|-|
|<span data-ttu-id="b0792-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="b0792-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="b0792-126">LUID адаптера, переданный в *адаптерлуид* , распознан, но адаптер больше не находится в допустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="b0792-126">The adapter LUID passed in *adapterLUID* is recognized, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="b0792-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b0792-127">E_INVALIDARG</span></span>|<span data-ttu-id="b0792-128">Такой LUID адаптера отсутствует, так как значение, переданное в *адаптерлуид* , доступно через дкскоре.</span><span class="sxs-lookup"><span data-stu-id="b0792-128">No such adapter LUID as the value passed in *adapterLUID* is available through DXCore.</span></span>|
|<span data-ttu-id="b0792-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="b0792-129">E_NOINTERFACE</span></span>|<span data-ttu-id="b0792-130">Указано недопустимое значение для *riid*.</span><span class="sxs-lookup"><span data-stu-id="b0792-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="b0792-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="b0792-131">E_POINTER</span></span>|<span data-ttu-id="b0792-132">`nullptr` был предоставлен для *ппвадаптер*.</span><span class="sxs-lookup"><span data-stu-id="b0792-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b0792-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0792-133">Remarks</span></span>

<span data-ttu-id="b0792-134">Несколько вызовов, передающих один и тот же [LUID](/windows/win32/api/winnt/ns-winnt-luid) , возвращают идентичные указатели интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b0792-134">Multiple calls passing the same [LUID](/windows/win32/api/winnt/ns-winnt-luid) return identical interface pointers.</span></span> <span data-ttu-id="b0792-135">В результате можно сравнивать указатели интерфейса, чтобы определить, ссылаются ли несколько указателей на один и тот же объект адаптера.</span><span class="sxs-lookup"><span data-stu-id="b0792-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0792-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0792-136">See also</span></span>

<span data-ttu-id="b0792-137">[Идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="b0792-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>