---
description: Метод Сеткэйвалуе добавляет новое значение РЕФПРОПЕРТИКЭЙ (тип VT \_ Unknown) или перезаписывает существующий.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'Метод Ипортабледевицевалуес:: Сеткэйвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae55b47687043bba92afbab09f25de8a5fc679d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704269"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a><span data-ttu-id="74d97-103">Метод Ипортабледевицевалуес:: Сеткэйвалуе</span><span class="sxs-lookup"><span data-stu-id="74d97-103">IPortableDeviceValues::SetKeyValue method</span></span>

<span data-ttu-id="74d97-104">Метод **сеткэйвалуе** добавляет новое значение **РЕФПРОПЕРТИКЭЙ** (тип VT \_ Unknown) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="74d97-104">The **SetKeyValue** method adds a new **REFPROPERTYKEY** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="74d97-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74d97-105">Syntax</span></span>


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
);
```



## <a name="parameters"></a><span data-ttu-id="74d97-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74d97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74d97-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74d97-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d97-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="74d97-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="74d97-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74d97-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d97-110">Объект **рефпропертикэй** , указывающий новое значение.</span><span class="sxs-lookup"><span data-stu-id="74d97-110">A **REFPROPERTYKEY** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74d97-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74d97-111">Return value</span></span>

<span data-ttu-id="74d97-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="74d97-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="74d97-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="74d97-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="74d97-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="74d97-114">Return code</span></span>                                                                          | <span data-ttu-id="74d97-115">Описание</span><span class="sxs-lookup"><span data-stu-id="74d97-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="74d97-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="74d97-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="74d97-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="74d97-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74d97-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74d97-118">Remarks</span></span>

<span data-ttu-id="74d97-119">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="74d97-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="74d97-120">Существующий ключ памяти освобождается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="74d97-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="74d97-121">Требования</span><span class="sxs-lookup"><span data-stu-id="74d97-121">Requirements</span></span>



| <span data-ttu-id="74d97-122">Требование</span><span class="sxs-lookup"><span data-stu-id="74d97-122">Requirement</span></span> | <span data-ttu-id="74d97-123">Значение</span><span class="sxs-lookup"><span data-stu-id="74d97-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d97-124">Header</span><span class="sxs-lookup"><span data-stu-id="74d97-124">Header</span></span><br/>  | <dl> <span data-ttu-id="74d97-125"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="74d97-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="74d97-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74d97-126">Library</span></span><br/> | <dl> <span data-ttu-id="74d97-127"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74d97-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74d97-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74d97-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74d97-129">Добавление ресурса в объект</span><span class="sxs-lookup"><span data-stu-id="74d97-129">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="74d97-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="74d97-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="74d97-131">**Ипортабледевицевалуес:: Жеткэйвалуе**</span><span class="sxs-lookup"><span data-stu-id="74d97-131">**IPortableDeviceValues::GetKeyValue**</span></span>](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




