---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Создает список объектов адаптера, представляющих текущее состояние адаптера системы, и удовлетворяет указанным критериям.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488036"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a><span data-ttu-id="2d0c6-103">Метод Идкскореадаптерфактори:: Креатеадаптерлист</span><span class="sxs-lookup"><span data-stu-id="2d0c6-103">IDXCoreAdapterFactory::CreateAdapterList method</span></span>

<span data-ttu-id="2d0c6-104">Создает список объектов адаптера, представляющих текущее состояние адаптера системы, и удовлетворяет указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-104">Generates a list of adapter objects representing the current adapter state of the system, and meeting the criteria specified.</span></span> <span data-ttu-id="2d0c6-105">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="2d0c6-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d0c6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d0c6-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a><span data-ttu-id="2d0c6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d0c6-107">Parameters</span></span>

### <a name="numattributes"></a><span data-ttu-id="2d0c6-108">нуматтрибутес</span><span class="sxs-lookup"><span data-stu-id="2d0c6-108">numAttributes</span></span>

<span data-ttu-id="2d0c6-109">Тип: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="2d0c6-109">Type: **uint32_t**</span></span>

<span data-ttu-id="2d0c6-110">Число элементов в массиве, на которое указывает аргумент *филтераттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="2d0c6-110">The number of elements in the array pointed to by the *filterAttributes* argument.</span></span>

### <a name="filterattributes-in"></a><span data-ttu-id="2d0c6-111">Филтераттрибутес [in]</span><span class="sxs-lookup"><span data-stu-id="2d0c6-111">filterAttributes [in]</span></span>

<span data-ttu-id="2d0c6-112">Тип: **константа \* GUID**</span><span class="sxs-lookup"><span data-stu-id="2d0c6-112">Type: **const GUID\***</span></span>

<span data-ttu-id="2d0c6-113">Указатель на массив идентификаторов GUID атрибутов адаптера.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-113">A pointer to an array of adapter attribute GUIDs.</span></span> <span data-ttu-id="2d0c6-114">Список идентификаторов GUID атрибутов см. в разделе [идентификаторы GUID атрибута адаптера дкскоре](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="2d0c6-114">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span> <span data-ttu-id="2d0c6-115">Необходимо указать по крайней мере один GUID.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-115">At least one GUID must be provided.</span></span> <span data-ttu-id="2d0c6-116">В случае, если в массиве указано более одного идентификатора GUID, в возвращаемый список будут включаться только те адаптеры, которые соответствуют *всем* запрошенным атрибутам.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-116">In the case that more than one GUID is provided in the array, only adapters that meet *all* of the requested attributes will be included in the returned list.</span></span>

### <a name="riid"></a><span data-ttu-id="2d0c6-117">riid</span><span class="sxs-lookup"><span data-stu-id="2d0c6-117">riid</span></span>

<span data-ttu-id="2d0c6-118">Тип: **рефиид**</span><span class="sxs-lookup"><span data-stu-id="2d0c6-118">Type: **REFIID**</span></span>

<span data-ttu-id="2d0c6-119">Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в *ппвадаптерлист*.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-119">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapterList*.</span></span> <span data-ttu-id="2d0c6-120">Это должен быть идентификатор интерфейса (IID) [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md).</span><span class="sxs-lookup"><span data-stu-id="2d0c6-120">This is expected to be the interface identifier (IID) of [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span></span>

### <a name="ppvadapterlist-out"></a><span data-ttu-id="2d0c6-121">Ппвадаптерлист [out]</span><span class="sxs-lookup"><span data-stu-id="2d0c6-121">ppvAdapterList [out]</span></span>

<span data-ttu-id="2d0c6-122">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="2d0c6-122">Type: **void\*\***</span></span>

<span data-ttu-id="2d0c6-123">Адрес указателя на интерфейс с идентификатором IID, указанным в параметре *riid* .</span><span class="sxs-lookup"><span data-stu-id="2d0c6-123">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="2d0c6-124">После успешного возврата *\* ппвадаптерлист* (адрес разыменования) содержит указатель на созданный список адаптеров.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-124">Upon successful return, *\*ppvAdapterList* (the dereferenced address) contains a pointer to the adapter list created.</span></span>

## <a name="returns"></a><span data-ttu-id="2d0c6-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d0c6-125">Returns</span></span>

<span data-ttu-id="2d0c6-126">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="2d0c6-126">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="2d0c6-127">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-127">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="2d0c6-128">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-128">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="2d0c6-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d0c6-129">Return value</span></span>|<span data-ttu-id="2d0c6-130">Описание</span><span class="sxs-lookup"><span data-stu-id="2d0c6-130">Description</span></span>|
|-|-|
|<span data-ttu-id="2d0c6-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2d0c6-131">E_INVALIDARG</span></span>|<span data-ttu-id="2d0c6-132">`nullptr` был предоставлен для *филтераттрибутес*, или для *нуматтрибутес* предоставлено значение 0.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-132">`nullptr` was provided for *filterAttributes*, or 0 was provided for *numAttributes*.</span></span>|
|<span data-ttu-id="2d0c6-133">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="2d0c6-133">E_NOINTERFACE</span></span>|<span data-ttu-id="2d0c6-134">Указано недопустимое значение для *riid*.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-134">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="2d0c6-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="2d0c6-135">E_POINTER</span></span>|<span data-ttu-id="2d0c6-136">`nullptr` был предоставлен для *ппвадаптерлист*.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-136">`nullptr` was provided for *ppvAdapterList*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2d0c6-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d0c6-137">Remarks</span></span>

<span data-ttu-id="2d0c6-138">Даже если адаптеры не найдены, при условии, что аргументы являются допустимыми, **креатеадаптерлист** создает допустимый объект [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) и возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-138">Even if no adapters are found, as long as the arguments are valid, **CreateAdapterList** creates a valid [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object, and returns **S_OK**.</span></span> <span data-ttu-id="2d0c6-139">После создания адаптеры в этом конкретном списке не изменятся.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-139">Once generated, the adapters in this specific list won't change.</span></span> <span data-ttu-id="2d0c6-140">Но список будет считаться устаревшим, если один из адаптеров позже станет недопустимым, или если поступит новый адаптер, отвечающий указанным условиям фильтра.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-140">But the list will be considered stale if one of the adapters later becomes invalid, or if a new adapter arrives that meets the provided filter criteria.</span></span> <span data-ttu-id="2d0c6-141">Список, возвращаемый функцией **креатеадаптерлист** , не упорядочивается каким-либо образом, но Упорядочение списка выполняется по нескольким вызовам и даже при перезапуске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-141">The list returned by **CreateAdapterList** is not ordered in any particular way, but the ordering of a list is consistent across multiple calls, and even across operating system restarts.</span></span> <span data-ttu-id="2d0c6-142">Порядок сортировки может измениться при изменении конфигурации системы, включая добавление или удаление адаптера или обновление драйвера на существующем адаптере.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-142">The ordering may change upon system configuration changes, including the addition or removal of an adapter, or a driver update on an existing adapter.</span></span> <span data-ttu-id="2d0c6-143">Вы можете зарегистрировать эти изменения с помощью [идкскореадаптерфактори:: регистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) , используя тип уведомления **дкскоренотификатионтипе. адаптерлистстале**.</span><span class="sxs-lookup"><span data-stu-id="2d0c6-143">You can register for these changes with [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) using the notification type **DXCoreNotificationType.AdapterListStale**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d0c6-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d0c6-144">See also</span></span>

<span data-ttu-id="2d0c6-145">[Идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="2d0c6-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>