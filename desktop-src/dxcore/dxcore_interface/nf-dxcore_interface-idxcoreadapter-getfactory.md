---
title: IDXCoreAdapter::GetFactory
description: 'Извлекает указатель интерфейса [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) на объект фабрики адаптера дкскоре. | Идкскореадаптер:: псевдо'
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 1ac3e7fccd39b9b03ecb7016494a610519d26afa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273536"
---
# <a name="idxcoreadaptergetfactory-method"></a><span data-ttu-id="34ea6-104">Метод Идкскореадаптер:: псевдо</span><span class="sxs-lookup"><span data-stu-id="34ea6-104">IDXCoreAdapter::GetFactory method</span></span>

<span data-ttu-id="34ea6-105">Извлекает указатель интерфейса [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) на объект фабрики адаптера дкскоре.</span><span class="sxs-lookup"><span data-stu-id="34ea6-105">Retrieves an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface pointer to the DXCore adapter factory object.</span></span> <span data-ttu-id="34ea6-106">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="34ea6-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="34ea6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34ea6-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a><span data-ttu-id="34ea6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="34ea6-108">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="34ea6-109">riid</span><span class="sxs-lookup"><span data-stu-id="34ea6-109">riid</span></span>

<span data-ttu-id="34ea6-110">Тип: **рефиид**</span><span class="sxs-lookup"><span data-stu-id="34ea6-110">Type: **REFIID**</span></span>

<span data-ttu-id="34ea6-111">Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в *ппвфактори*.</span><span class="sxs-lookup"><span data-stu-id="34ea6-111">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="34ea6-112">Это должен быть идентификатор интерфейса (IID) [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="34ea6-112">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="34ea6-113">Ппвфактори [out]</span><span class="sxs-lookup"><span data-stu-id="34ea6-113">ppvFactory [out]</span></span>

<span data-ttu-id="34ea6-114">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="34ea6-114">Type: **void\*\***</span></span>

<span data-ttu-id="34ea6-115">Адрес указателя на интерфейс с идентификатором IID, указанным в параметре *riid* .</span><span class="sxs-lookup"><span data-stu-id="34ea6-115">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="34ea6-116">После успешного возврата *\* ппвфактори* (адрес разыменования) содержит указатель на существующий объект фабрики адаптера дкскоре.</span><span class="sxs-lookup"><span data-stu-id="34ea6-116">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object.</span></span> <span data-ttu-id="34ea6-117">Перед возвращением функция увеличивает счетчик ссылок в интерфейсе [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) объекта фабрики.</span><span class="sxs-lookup"><span data-stu-id="34ea6-117">Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span>

## <a name="returns"></a><span data-ttu-id="34ea6-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34ea6-118">Returns</span></span>

<span data-ttu-id="34ea6-119">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="34ea6-119">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="34ea6-120">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="34ea6-120">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="34ea6-121">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="34ea6-121">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="34ea6-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34ea6-122">Return value</span></span>|<span data-ttu-id="34ea6-123">Описание</span><span class="sxs-lookup"><span data-stu-id="34ea6-123">Description</span></span>|
|-|-|
|<span data-ttu-id="34ea6-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="34ea6-124">E_NOINTERFACE</span></span>|<span data-ttu-id="34ea6-125">Указано недопустимое значение для *riid*.</span><span class="sxs-lookup"><span data-stu-id="34ea6-125">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="34ea6-126">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="34ea6-126">E_POINTER</span></span>|<span data-ttu-id="34ea6-127">`nullptr` был предоставлен для *ппвфактори*.</span><span class="sxs-lookup"><span data-stu-id="34ea6-127">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="34ea6-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34ea6-128">Remarks</span></span>

<span data-ttu-id="34ea6-129">В течение времени, когда ссылка существует в интерфейсе [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) , интерфейсе [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) или интерфейсе [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) , дополнительные вызовы [Дкскорекреатеадаптерфактори](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)GetObject или [IDXCoreAdapter::]() GetObject будут возвращать указатели на один и тот же объект, увеличивая число ссылок в интерфейсе **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="34ea6-129">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory]() will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="34ea6-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34ea6-130">See also</span></span>

<span data-ttu-id="34ea6-131">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="34ea6-131">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
