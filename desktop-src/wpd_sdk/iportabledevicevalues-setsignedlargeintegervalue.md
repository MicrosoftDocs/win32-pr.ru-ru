---
description: Метод Сетсигнедларжеинтежервалуе добавляет новое значение ЛОНГЛОНГ (Type VT \_ I8) или перезаписывает существующий.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: 'Метод Ипортабледевицевалуес:: Сетсигнедларжеинтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f8c207a88e17c9a1ddf45d77e9da8b62a8396e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704266"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a><span data-ttu-id="29df4-103">Метод Ипортабледевицевалуес:: Сетсигнедларжеинтежервалуе</span><span class="sxs-lookup"><span data-stu-id="29df4-103">IPortableDeviceValues::SetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="29df4-104">Метод **сетсигнедларжеинтежервалуе** добавляет новое значение **ЛОНГЛОНГ** (Type VT \_ I8) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="29df4-104">The **SetSignedLargeIntegerValue** method adds a new **LONGLONG** value (type VT\_I8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="29df4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29df4-105">Syntax</span></span>


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
);
```



## <a name="parameters"></a><span data-ttu-id="29df4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="29df4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29df4-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29df4-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29df4-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="29df4-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="29df4-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29df4-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29df4-110">Объект **лонглонг** , указывающий новое значение.</span><span class="sxs-lookup"><span data-stu-id="29df4-110">A **LONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29df4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29df4-111">Return value</span></span>

<span data-ttu-id="29df4-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="29df4-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="29df4-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="29df4-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="29df4-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="29df4-114">Return code</span></span>                                                                          | <span data-ttu-id="29df4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="29df4-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="29df4-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="29df4-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="29df4-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="29df4-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29df4-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29df4-118">Remarks</span></span>

<span data-ttu-id="29df4-119">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="29df4-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="29df4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="29df4-120">Requirements</span></span>



| <span data-ttu-id="29df4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="29df4-121">Requirement</span></span> | <span data-ttu-id="29df4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="29df4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29df4-123">Header</span><span class="sxs-lookup"><span data-stu-id="29df4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="29df4-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="29df4-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="29df4-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="29df4-125">Library</span></span><br/> | <dl> <span data-ttu-id="29df4-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29df4-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29df4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29df4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29df4-128">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="29df4-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="29df4-129">**Ипортабледевицевалуес:: Жетсигнедларжеинтежервалуе**</span><span class="sxs-lookup"><span data-stu-id="29df4-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




