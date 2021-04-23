---
description: Метод Сетипортабледевицекэйколлектионвалуе добавляет новое значение Сетипортабледевицекэйколлектионвалуе (тип VT \_ Unknown) или перезаписывает существующий.
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: 'Метод Ипортабледевицевалуес:: Сетипортабледевицекэйколлектионвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: face82230b9dd3bf6cbde18aaee8dd857e17d0a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704278"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="d27dc-103">Метод Ипортабледевицевалуес:: Сетипортабледевицекэйколлектионвалуе</span><span class="sxs-lookup"><span data-stu-id="d27dc-103">IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="d27dc-104">Метод **сетипортабледевицекэйколлектионвалуе** добавляет новое значение **СЕТИПОРТАБЛЕДЕВИЦЕКЭЙКОЛЛЕКТИОНВАЛУЕ** (тип VT \_ Unknown) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="d27dc-104">The **SetIPortableDeviceKeyCollectionValue** method adds a new **SetIPortableDeviceKeyCollectionValue** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="d27dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d27dc-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="d27dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d27dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27dc-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d27dc-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d27dc-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="d27dc-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="d27dc-109">*pValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d27dc-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d27dc-110">Указатель на интерфейс **ипортабледевицекэйколлектион** , указывающий новое значение.</span><span class="sxs-lookup"><span data-stu-id="d27dc-110">Pointer to an **IPortableDeviceKeyCollection** interface that specifies the new value.</span></span> <span data-ttu-id="d27dc-111">Пакет SDK копирует ссылку на отправленный интерфейс и вызывает **AddRef** для него.</span><span class="sxs-lookup"><span data-stu-id="d27dc-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27dc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d27dc-112">Return value</span></span>

<span data-ttu-id="d27dc-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d27dc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d27dc-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d27dc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d27dc-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d27dc-115">Return code</span></span>                                                                          | <span data-ttu-id="d27dc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d27dc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d27dc-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d27dc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d27dc-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d27dc-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d27dc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d27dc-119">Remarks</span></span>

<span data-ttu-id="d27dc-120">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="d27dc-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="d27dc-121">Существующий ключ памяти освобождается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="d27dc-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="d27dc-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d27dc-122">Requirements</span></span>



| <span data-ttu-id="d27dc-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d27dc-123">Requirement</span></span> | <span data-ttu-id="d27dc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d27dc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d27dc-125">Header</span><span class="sxs-lookup"><span data-stu-id="d27dc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d27dc-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d27dc-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d27dc-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d27dc-127">Library</span></span><br/> | <dl> <span data-ttu-id="d27dc-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d27dc-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d27dc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d27dc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d27dc-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="d27dc-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d27dc-131">**Ипортабледевицевалуес:: Жетипортабледевицекэйколлектионвалуе**</span><span class="sxs-lookup"><span data-stu-id="d27dc-131">**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




