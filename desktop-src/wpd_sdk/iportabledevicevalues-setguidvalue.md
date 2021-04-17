---
description: Метод Сетгуидвалуе добавляет новое значение GUID (Type VT \_ CLSID) или перезаписывает существующий.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: 'Метод Ипортабледевицевалуес:: Сетгуидвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9d9f85def6ba487163f7c4c7d7441a89e0747ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704473"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a><span data-ttu-id="abfca-103">Метод Ипортабледевицевалуес:: Сетгуидвалуе</span><span class="sxs-lookup"><span data-stu-id="abfca-103">IPortableDeviceValues::SetGuidValue method</span></span>

<span data-ttu-id="abfca-104">Метод **сетгуидвалуе** добавляет новое значение **GUID** (Type VT \_ CLSID) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="abfca-104">The **SetGuidValue** method adds a new **GUID** value (type VT\_CLSID) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="abfca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abfca-105">Syntax</span></span>


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a><span data-ttu-id="abfca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="abfca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abfca-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="abfca-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfca-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="abfca-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="abfca-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="abfca-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfca-110">Объект **рефгуид** , содержащий новое значение.</span><span class="sxs-lookup"><span data-stu-id="abfca-110">A **REFGUID** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abfca-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abfca-111">Return value</span></span>

<span data-ttu-id="abfca-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="abfca-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="abfca-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="abfca-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="abfca-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="abfca-114">Return code</span></span>                                                                          | <span data-ttu-id="abfca-115">Описание</span><span class="sxs-lookup"><span data-stu-id="abfca-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="abfca-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="abfca-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="abfca-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="abfca-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="abfca-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abfca-118">Remarks</span></span>

<span data-ttu-id="abfca-119">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="abfca-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="abfca-120">Требования</span><span class="sxs-lookup"><span data-stu-id="abfca-120">Requirements</span></span>



| <span data-ttu-id="abfca-121">Требование</span><span class="sxs-lookup"><span data-stu-id="abfca-121">Requirement</span></span> | <span data-ttu-id="abfca-122">Значение</span><span class="sxs-lookup"><span data-stu-id="abfca-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abfca-123">Header</span><span class="sxs-lookup"><span data-stu-id="abfca-123">Header</span></span><br/>  | <dl> <span data-ttu-id="abfca-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="abfca-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="abfca-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="abfca-125">Library</span></span><br/> | <dl> <span data-ttu-id="abfca-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abfca-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abfca-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abfca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abfca-128">Добавление ресурса в объект</span><span class="sxs-lookup"><span data-stu-id="abfca-128">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="abfca-129">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="abfca-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="abfca-130">**Ипортабледевицевалуес:: Жетгуидвалуе**</span><span class="sxs-lookup"><span data-stu-id="abfca-130">**IPortableDeviceValues::GetGuidValue**</span></span>](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




