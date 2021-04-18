---
description: Метод Сетунсигнедларжеинтежервалуе добавляет новое значение УЛОНГЛОНГ (тип VT \_ UI8) или перезаписывает существующий.
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: 'Метод Ипортабледевицевалуес:: Сетунсигнедларжеинтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c1ade76b4242c7508cb325e90c567349afcdc9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704263"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a><span data-ttu-id="9e2bd-103">Метод Ипортабледевицевалуес:: Сетунсигнедларжеинтежервалуе</span><span class="sxs-lookup"><span data-stu-id="9e2bd-103">IPortableDeviceValues::SetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="9e2bd-104">Метод **сетунсигнедларжеинтежервалуе** добавляет новое значение **УЛОНГЛОНГ** (тип VT \_ UI8) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="9e2bd-104">The **SetUnsignedLargeIntegerValue** method adds a new **ULONGLONG** value (type VT\_UI8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e2bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e2bd-105">Syntax</span></span>


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
);
```



## <a name="parameters"></a><span data-ttu-id="9e2bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e2bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e2bd-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e2bd-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e2bd-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="9e2bd-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="9e2bd-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e2bd-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e2bd-110">Объект **улонглонг** , указывающий новое значение.</span><span class="sxs-lookup"><span data-stu-id="9e2bd-110">A **ULONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e2bd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e2bd-111">Return value</span></span>

<span data-ttu-id="9e2bd-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9e2bd-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9e2bd-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9e2bd-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9e2bd-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9e2bd-114">Return code</span></span>                                                                          | <span data-ttu-id="9e2bd-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9e2bd-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9e2bd-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9e2bd-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9e2bd-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="9e2bd-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9e2bd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9e2bd-118">Requirements</span></span>



| <span data-ttu-id="9e2bd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9e2bd-119">Requirement</span></span> | <span data-ttu-id="9e2bd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9e2bd-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2bd-121">Header</span><span class="sxs-lookup"><span data-stu-id="9e2bd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9e2bd-122"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e2bd-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e2bd-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9e2bd-123">Library</span></span><br/> | <dl> <span data-ttu-id="9e2bd-124"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e2bd-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e2bd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e2bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e2bd-126">Добавление ресурса в объект</span><span class="sxs-lookup"><span data-stu-id="9e2bd-126">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="9e2bd-127">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="9e2bd-127">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="9e2bd-128">**Ипортабледевицевалуес:: Жетунсигнедларжеинтежервалуе**</span><span class="sxs-lookup"><span data-stu-id="9e2bd-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




