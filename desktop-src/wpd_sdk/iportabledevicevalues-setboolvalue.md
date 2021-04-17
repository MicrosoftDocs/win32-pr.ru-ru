---
description: Метод SetBoolValue добавляет новое логическое значение (тип VT \_ bool) или перезаписывает существующий.
ms.assetid: add30665-78f7-4037-801e-af51a4ab2f60
title: 'Метод Ипортабледевицевалуес:: SetBoolValue (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7adf311e863c08873aa8300f9e940d4a5b49417f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717839"
---
# <a name="iportabledevicevaluessetboolvalue-method"></a><span data-ttu-id="47753-103">Метод Ипортабледевицевалуес:: SetBoolValue</span><span class="sxs-lookup"><span data-stu-id="47753-103">IPortableDeviceValues::SetBoolValue method</span></span>

<span data-ttu-id="47753-104">Метод **SetBoolValue** добавляет новое **логическое** значение (тип VT \_ bool) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="47753-104">The **SetBoolValue** method adds a new **Boolean** value (type VT\_BOOL) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="47753-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47753-105">Syntax</span></span>


```C++
HRESULT SetBoolValue(
  [in]       REFPROPERTYKEY key,
  [in] const BOOL           Value
);
```



## <a name="parameters"></a><span data-ttu-id="47753-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47753-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47753-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47753-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47753-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="47753-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="47753-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47753-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47753-110">**Bool** , указывающий новое значение.</span><span class="sxs-lookup"><span data-stu-id="47753-110">A **BOOL** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47753-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47753-111">Return value</span></span>

<span data-ttu-id="47753-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="47753-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="47753-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="47753-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="47753-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="47753-114">Return code</span></span>                                                                          | <span data-ttu-id="47753-115">Описание</span><span class="sxs-lookup"><span data-stu-id="47753-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="47753-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="47753-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="47753-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="47753-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="47753-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47753-118">Remarks</span></span>

<span data-ttu-id="47753-119">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="47753-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="47753-120">Существующий ключ памяти освобождается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="47753-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="47753-121">Требования</span><span class="sxs-lookup"><span data-stu-id="47753-121">Requirements</span></span>



| <span data-ttu-id="47753-122">Требование</span><span class="sxs-lookup"><span data-stu-id="47753-122">Requirement</span></span> | <span data-ttu-id="47753-123">Значение</span><span class="sxs-lookup"><span data-stu-id="47753-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47753-124">Header</span><span class="sxs-lookup"><span data-stu-id="47753-124">Header</span></span><br/>  | <dl> <span data-ttu-id="47753-125"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="47753-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="47753-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47753-126">Library</span></span><br/> | <dl> <span data-ttu-id="47753-127"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47753-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47753-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47753-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47753-129">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="47753-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="47753-130">**Ипортабледевицевалуес:: Жетбулвалуе**</span><span class="sxs-lookup"><span data-stu-id="47753-130">**IPortableDeviceValues::GetBoolValue**</span></span>](iportabledevicevalues-getboolvalue.md)
</dt> </dl>

 

 




