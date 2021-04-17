---
description: Метод Сетипортабледевицевалуесвалуе добавляет новое значение Ипортабледевицевалуес (тип VT \_ Unknown) или перезаписывает существующий.
ms.assetid: 3e51964e-6ee0-4885-94ca-cc8000b456b4
title: 'Метод Ипортабледевицевалуес:: Сетипортабледевицевалуесвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 265a5d3633dfa8252ff7afd4042a41e476040d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704272"
---
# <a name="iportabledevicevaluessetiportabledevicevaluesvalue-method"></a><span data-ttu-id="ecb6d-103">Метод Ипортабледевицевалуес:: Сетипортабледевицевалуесвалуе</span><span class="sxs-lookup"><span data-stu-id="ecb6d-103">IPortableDeviceValues::SetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="ecb6d-104">Метод **сетипортабледевицевалуесвалуе** добавляет новое значение **ИПОРТАБЛЕДЕВИЦЕВАЛУЕС** (тип VT \_ Unknown) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="ecb6d-104">The **SetIPortableDeviceValuesValue** method adds a new **IPortableDeviceValues** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb6d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecb6d-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesValue(
  [in] REFPROPERTYKEY        key,
  [in] IPortableDeviceValues *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="ecb6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecb6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb6d-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecb6d-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb6d-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="ecb6d-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="ecb6d-109">*pValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecb6d-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb6d-110">Указатель на интерфейс **ипортабледевицевалуес** , указывающий новое значение.</span><span class="sxs-lookup"><span data-stu-id="ecb6d-110">Pointer to an **IPortableDeviceValues** interface that specifies the new value.</span></span> <span data-ttu-id="ecb6d-111">Пакет SDK копирует ссылку на отправленный интерфейс и вызывает **AddRef** для него.</span><span class="sxs-lookup"><span data-stu-id="ecb6d-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb6d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecb6d-112">Return value</span></span>

<span data-ttu-id="ecb6d-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ecb6d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ecb6d-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ecb6d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ecb6d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ecb6d-115">Return code</span></span>                                                                          | <span data-ttu-id="ecb6d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ecb6d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ecb6d-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ecb6d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ecb6d-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ecb6d-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ecb6d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ecb6d-119">Remarks</span></span>

<span data-ttu-id="ecb6d-120">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="ecb6d-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="ecb6d-121">Существующий ключ памяти освобождается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="ecb6d-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb6d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ecb6d-122">Requirements</span></span>



| <span data-ttu-id="ecb6d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ecb6d-123">Requirement</span></span> | <span data-ttu-id="ecb6d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ecb6d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb6d-125">Header</span><span class="sxs-lookup"><span data-stu-id="ecb6d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ecb6d-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb6d-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecb6d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ecb6d-127">Library</span></span><br/> | <dl> <span data-ttu-id="ecb6d-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecb6d-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb6d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecb6d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb6d-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="ecb6d-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ecb6d-131">**Ипортабледевицевалуес:: Жетипортабледевицевалуесвалуе**</span><span class="sxs-lookup"><span data-stu-id="ecb6d-131">**IPortableDeviceValues::GetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-getiportabledevicevaluesvalue.md)
</dt> </dl>

 

 




