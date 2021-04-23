---
description: Метод GetAt извлекает объект PROPERTYKEY из коллекции по индексу.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'Метод Ипортабледевицекэйколлектион:: GetAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708349"
---
# <a name="iportabledevicekeycollectiongetat-method"></a><span data-ttu-id="05381-103">Метод Ипортабледевицекэйколлектион:: GetAt</span><span class="sxs-lookup"><span data-stu-id="05381-103">IPortableDeviceKeyCollection::GetAt method</span></span>

<span data-ttu-id="05381-104">Метод **GetAt** извлекает объект **PROPERTYKEY** из коллекции по индексу.</span><span class="sxs-lookup"><span data-stu-id="05381-104">The **GetAt** method retrieves a **PROPERTYKEY** from the collection by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="05381-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05381-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a><span data-ttu-id="05381-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05381-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05381-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05381-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05381-108">**Параметр DWORD** , содержащий индекс извлекаемого ключа.</span><span class="sxs-lookup"><span data-stu-id="05381-108">**DWORD** that contains the index of the key to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="05381-109">*pKey* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="05381-109">*pKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05381-110">Указатель на объект **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="05381-110">Pointer to a **PROPERTYKEY** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05381-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05381-111">Return value</span></span>

<span data-ttu-id="05381-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="05381-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="05381-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="05381-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="05381-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="05381-114">Return code</span></span>                                                                                  | <span data-ttu-id="05381-115">Описание</span><span class="sxs-lookup"><span data-stu-id="05381-115">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="05381-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="05381-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="05381-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="05381-117">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="05381-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="05381-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="05381-119">Переданный индекс был вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="05381-119">The index passed in was out of range.</span></span><br/>     |
| <dl> <span data-ttu-id="05381-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="05381-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="05381-121">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="05381-121">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="05381-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="05381-122">Examples</span></span>

<span data-ttu-id="05381-123">Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="05381-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05381-124">Требования</span><span class="sxs-lookup"><span data-stu-id="05381-124">Requirements</span></span>



| <span data-ttu-id="05381-125">Требование</span><span class="sxs-lookup"><span data-stu-id="05381-125">Requirement</span></span> | <span data-ttu-id="05381-126">Значение</span><span class="sxs-lookup"><span data-stu-id="05381-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05381-127">Header</span><span class="sxs-lookup"><span data-stu-id="05381-127">Header</span></span><br/>  | <dl> <span data-ttu-id="05381-128"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="05381-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="05381-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05381-129">Library</span></span><br/> | <dl> <span data-ttu-id="05381-130"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05381-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05381-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05381-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05381-132">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="05381-132">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="05381-133">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="05381-133">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="05381-134">Получение поддерживаемых методов службы</span><span class="sxs-lookup"><span data-stu-id="05381-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




