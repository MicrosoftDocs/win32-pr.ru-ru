---
title: DXCoreCreateAdapterFactory
description: Создает фабрику адаптера Дкскоре, которую можно использовать для создания последующих объектов Дкскоре.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987763"
---
# <a name="dxcorecreateadapterfactory-function"></a><span data-ttu-id="2bbb2-103">Функция Дкскорекреатеадаптерфактори</span><span class="sxs-lookup"><span data-stu-id="2bbb2-103">DXCoreCreateAdapterFactory function</span></span>

## <a name="description"></a><span data-ttu-id="2bbb2-104">Описание</span><span class="sxs-lookup"><span data-stu-id="2bbb2-104">Description</span></span>

<span data-ttu-id="2bbb2-105">Создает фабрику адаптера Дкскоре, которую можно использовать для создания последующих объектов Дкскоре.</span><span class="sxs-lookup"><span data-stu-id="2bbb2-105">Creates a DXCore adapter factory, which you can use to generate further DXCore objects.</span></span> <span data-ttu-id="2bbb2-106">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="2bbb2-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="2bbb2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bbb2-107">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="2bbb2-108">riid</span><span class="sxs-lookup"><span data-stu-id="2bbb2-108">riid</span></span>

<span data-ttu-id="2bbb2-109">Тип: **рефиид**</span><span class="sxs-lookup"><span data-stu-id="2bbb2-109">Type: **REFIID**</span></span>

<span data-ttu-id="2bbb2-110">Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в *ппвфактори*.</span><span class="sxs-lookup"><span data-stu-id="2bbb2-110">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="2bbb2-111">Это должен быть идентификатор интерфейса (IID) [идкскореадаптерфактори](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="2bbb2-111">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="2bbb2-112">Ппвфактори [out]</span><span class="sxs-lookup"><span data-stu-id="2bbb2-112">ppvFactory [out]</span></span>

<span data-ttu-id="2bbb2-113">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="2bbb2-113">Type: **void\*\***</span></span>

<span data-ttu-id="2bbb2-114">Адрес указателя на интерфейс с идентификатором IID, указанным в параметре *riid* .</span><span class="sxs-lookup"><span data-stu-id="2bbb2-114">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="2bbb2-115">После успешного возврата *\* ппвфактори* (адрес разыменования) содержит указатель на созданную фабрику дкскоре.</span><span class="sxs-lookup"><span data-stu-id="2bbb2-115">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the DXCore factory created.</span></span>

## <a name="returns"></a><span data-ttu-id="2bbb2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bbb2-116">Returns</span></span>

<span data-ttu-id="2bbb2-117">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="2bbb2-117">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="2bbb2-118">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="2bbb2-118">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="2bbb2-119">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2bbb2-119">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="2bbb2-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bbb2-120">Return value</span></span>|<span data-ttu-id="2bbb2-121">Описание</span><span class="sxs-lookup"><span data-stu-id="2bbb2-121">Description</span></span>|
|-|-|
|<span data-ttu-id="2bbb2-122">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="2bbb2-122">E_NOINTERFACE</span></span>|<span data-ttu-id="2bbb2-123">Указано недопустимое значение для *riid*.</span><span class="sxs-lookup"><span data-stu-id="2bbb2-123">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="2bbb2-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="2bbb2-124">E_POINTER</span></span>|<span data-ttu-id="2bbb2-125">`nullptr` был предоставлен для *ппвфактори*.</span><span class="sxs-lookup"><span data-stu-id="2bbb2-125">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2bbb2-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bbb2-126">Remarks</span></span>

<span data-ttu-id="2bbb2-127">В течение времени, когда ссылка существует в интерфейсе [идкскореадаптерфактори](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) , интерфейсе [идкскореадаптерлист](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) или интерфейсе [идкскореадаптер](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) , дополнительные вызовы **Дкскорекреатеадаптерфактори**, [IDXCoreAdapterList::](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)GetObject или [IDXCoreAdapter::](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) GetObject будут возвращать указатели на один и тот же объект, увеличивая число ссылок в интерфейсе **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="2bbb2-127">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bbb2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bbb2-128">See also</span></span>

<span data-ttu-id="2bbb2-129">[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="2bbb2-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>