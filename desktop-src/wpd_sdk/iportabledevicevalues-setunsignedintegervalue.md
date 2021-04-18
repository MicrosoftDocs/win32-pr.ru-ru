---
description: Метод Сетунсигнединтежервалуе добавляет новое значение типа ULONG (тип VT \_ UI4) или перезаписывает существующий.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'Метод Ипортабледевицевалуес:: Сетунсигнединтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704264"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a><span data-ttu-id="b3c06-103">Метод Ипортабледевицевалуес:: Сетунсигнединтежервалуе</span><span class="sxs-lookup"><span data-stu-id="b3c06-103">IPortableDeviceValues::SetUnsignedIntegerValue method</span></span>

<span data-ttu-id="b3c06-104">Метод **сетунсигнединтежервалуе** добавляет новое значение типа **ulong** (тип VT \_ UI4) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="b3c06-104">The **SetUnsignedIntegerValue** method adds a new **ULONG** value (type VT\_UI4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c06-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3c06-105">Syntax</span></span>


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
);
```



## <a name="parameters"></a><span data-ttu-id="b3c06-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3c06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c06-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3c06-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c06-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="b3c06-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="b3c06-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3c06-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c06-110">**Ulong** , задающее новое значение.</span><span class="sxs-lookup"><span data-stu-id="b3c06-110">A **ULONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c06-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3c06-111">Return value</span></span>

<span data-ttu-id="b3c06-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b3c06-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b3c06-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b3c06-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b3c06-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b3c06-114">Return code</span></span>                                                                          | <span data-ttu-id="b3c06-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b3c06-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b3c06-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c06-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b3c06-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="b3c06-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b3c06-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3c06-118">Remarks</span></span>

<span data-ttu-id="b3c06-119">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="b3c06-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="examples"></a><span data-ttu-id="b3c06-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="b3c06-120">Examples</span></span>

<span data-ttu-id="b3c06-121">Пример использования этого метода см. в разделе [**Указание сведений о клиенте**](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="b3c06-121">For an example of how to use this method, see [**Specifying Client Information**](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c06-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b3c06-122">Requirements</span></span>



| <span data-ttu-id="b3c06-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b3c06-123">Requirement</span></span> | <span data-ttu-id="b3c06-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b3c06-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c06-125">Header</span><span class="sxs-lookup"><span data-stu-id="b3c06-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b3c06-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c06-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3c06-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b3c06-127">Library</span></span><br/> | <dl> <span data-ttu-id="b3c06-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3c06-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c06-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3c06-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c06-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="b3c06-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b3c06-131">**Ипортабледевицевалуес:: Жетунсигнединтежервалуе**</span><span class="sxs-lookup"><span data-stu-id="b3c06-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span></span>](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="b3c06-132">**Указание сведений о клиенте**</span><span class="sxs-lookup"><span data-stu-id="b3c06-132">**Specifying Client Information**</span></span>](specifying-client-information.md)
</dt> </dl>

 

 




