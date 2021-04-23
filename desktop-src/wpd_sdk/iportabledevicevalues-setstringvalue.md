---
description: Метод SetStringValue добавляет новое строковое значение (Type VT \_ LPWSTR) или перезаписывает существующий.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'Метод Ипортабледевицевалуес:: SetStringValue (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704265"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a><span data-ttu-id="da2d3-103">Метод Ипортабледевицевалуес:: SetStringValue</span><span class="sxs-lookup"><span data-stu-id="da2d3-103">IPortableDeviceValues::SetStringValue method</span></span>

<span data-ttu-id="da2d3-104">Метод **SetStringValue** добавляет новое строковое значение (Type VT \_ LPWSTR) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="da2d3-104">The **SetStringValue** method adds a new string value (type VT\_LPWSTR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="da2d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da2d3-105">Syntax</span></span>


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a><span data-ttu-id="da2d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da2d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da2d3-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da2d3-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2d3-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="da2d3-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="da2d3-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da2d3-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2d3-110">Объект **лпквстр** , указывающий новое значение.</span><span class="sxs-lookup"><span data-stu-id="da2d3-110">A **LPCWSTR** that specifies the new value.</span></span> <span data-ttu-id="da2d3-111">Строка копируется, поэтому вызывающий объект может освободить память, выделенную для этого значения, после вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="da2d3-111">The string is copied, so the caller can release the memory allocated for this value after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da2d3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da2d3-112">Return value</span></span>

<span data-ttu-id="da2d3-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="da2d3-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="da2d3-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="da2d3-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="da2d3-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="da2d3-115">Return code</span></span>                                                                          | <span data-ttu-id="da2d3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="da2d3-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="da2d3-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="da2d3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="da2d3-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="da2d3-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="da2d3-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da2d3-119">Remarks</span></span>

<span data-ttu-id="da2d3-120">Любая существующая память ключа будет выпущена соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="da2d3-120">Any existing key memory will be released appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="da2d3-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="da2d3-121">Examples</span></span>

<span data-ttu-id="da2d3-122">Пример использования этого метода см. в разделе [Указание сведений о клиенте](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="da2d3-122">For an example of how to use this method, see [Specifying Client Information](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da2d3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="da2d3-123">Requirements</span></span>



| <span data-ttu-id="da2d3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="da2d3-124">Requirement</span></span> | <span data-ttu-id="da2d3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="da2d3-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da2d3-126">Header</span><span class="sxs-lookup"><span data-stu-id="da2d3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="da2d3-127"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="da2d3-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="da2d3-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da2d3-128">Library</span></span><br/> | <dl> <span data-ttu-id="da2d3-129"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da2d3-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da2d3-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da2d3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da2d3-131">Добавление ресурса в объект</span><span class="sxs-lookup"><span data-stu-id="da2d3-131">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="da2d3-132">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="da2d3-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="da2d3-133">**Ипортабледевицевалуес:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="da2d3-133">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[<span data-ttu-id="da2d3-134">Задание свойств для одного объекта</span><span class="sxs-lookup"><span data-stu-id="da2d3-134">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="da2d3-135">Задание свойств для нескольких объектов</span><span class="sxs-lookup"><span data-stu-id="da2d3-135">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> <dt>

[<span data-ttu-id="da2d3-136">Указание сведений о клиенте</span><span class="sxs-lookup"><span data-stu-id="da2d3-136">Specifying Client Information</span></span>](specifying-client-information.md)
</dt> <dt>

[<span data-ttu-id="da2d3-137">Запись свойств содержимого объекта</span><span class="sxs-lookup"><span data-stu-id="da2d3-137">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




