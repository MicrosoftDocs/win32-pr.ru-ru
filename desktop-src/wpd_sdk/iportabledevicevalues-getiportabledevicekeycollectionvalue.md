---
description: Метод Жетипортабледевицекэйколлектионвалуе извлекает значение Ипортабледевицекэйколлектион (тип VT \_ Unknown), заданный ключом.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'Метод Ипортабледевицевалуес:: Жетипортабледевицекэйколлектионвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675501"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="c1dc1-103">Метод Ипортабледевицевалуес:: Жетипортабледевицекэйколлектионвалуе</span><span class="sxs-lookup"><span data-stu-id="c1dc1-103">IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="c1dc1-104">Метод **жетипортабледевицекэйколлектионвалуе** извлекает значение **ИПОРТАБЛЕДЕВИЦЕКЭЙКОЛЛЕКТИОН** (тип VT \_ Unknown), заданный ключом.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-104">The **GetIPortableDeviceKeyCollectionValue** method retrieves an **IPortableDeviceKeyCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1dc1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1dc1-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="c1dc1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1dc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1dc1-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1dc1-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dc1-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c1dc1-109">*ппвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c1dc1-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dc1-110">Указатель на полученный указатель интерфейса [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c1dc1-110">Pointer to the retrieved [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface pointer.</span></span> <span data-ttu-id="c1dc1-111">Вызывающий объект отвечает за вызов метода **Release** на полученном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1dc1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1dc1-112">Return value</span></span>

<span data-ttu-id="c1dc1-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c1dc1-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c1dc1-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c1dc1-115">Return code</span></span>                                                                                                            | <span data-ttu-id="c1dc1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c1dc1-116">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1dc1-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c1dc1-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="c1dc1-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-118">The method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="c1dc1-119"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1dc1-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="c1dc1-120">Свойство, заданное *ключом* , не является интерфейсом **ипортабледевицекэйколлектион** .</span><span class="sxs-lookup"><span data-stu-id="c1dc1-120">The property specified by *key* is not an **IPortableDeviceKeyCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="c1dc1-121"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="c1dc1-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="c1dc1-122">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-122">The property specified by *key* is not in the collection.</span></span><br/>                             |



 

## <a name="examples"></a><span data-ttu-id="c1dc1-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="c1dc1-123">Examples</span></span>

<span data-ttu-id="c1dc1-124">Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="c1dc1-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1dc1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c1dc1-125">Requirements</span></span>



| <span data-ttu-id="c1dc1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c1dc1-126">Requirement</span></span> | <span data-ttu-id="c1dc1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c1dc1-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dc1-128">Header</span><span class="sxs-lookup"><span data-stu-id="c1dc1-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c1dc1-129"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1dc1-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1dc1-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1dc1-130">Library</span></span><br/> | <dl> <span data-ttu-id="c1dc1-131"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1dc1-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1dc1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1dc1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1dc1-133">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="c1dc1-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c1dc1-134">**Ипортабледевицевалуес:: Сетипортабледевицекэйколлектионвалуе**</span><span class="sxs-lookup"><span data-stu-id="c1dc1-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[<span data-ttu-id="c1dc1-135">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="c1dc1-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="c1dc1-136">Получение поддерживаемых методов службы</span><span class="sxs-lookup"><span data-stu-id="c1dc1-136">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




