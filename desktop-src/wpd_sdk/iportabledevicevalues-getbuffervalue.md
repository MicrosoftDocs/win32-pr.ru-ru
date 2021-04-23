---
description: Метод Жетбуффервалуе извлекает значение массива байтов (тип VT \_ vector \| VT \_ UI1), заданный ключом.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'Метод Ипортабледевицевалуес:: Жетбуффервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708478"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a><span data-ttu-id="dfa36-103">Метод Ипортабледевицевалуес:: Жетбуффервалуе</span><span class="sxs-lookup"><span data-stu-id="dfa36-103">IPortableDeviceValues::GetBufferValue method</span></span>

<span data-ttu-id="dfa36-104">Метод **жетбуффервалуе** извлекает значение **массива БАЙТОВ** (тип VT \_ vector \| VT \_ UI1), заданный ключом.</span><span class="sxs-lookup"><span data-stu-id="dfa36-104">The **GetBufferValue** method retrieves a **byte array** value (type VT\_VECTOR \| VT\_UI1) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa36-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfa36-105">Syntax</span></span>


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a><span data-ttu-id="dfa36-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfa36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa36-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfa36-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa36-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="dfa36-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="dfa36-109">*ппвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfa36-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa36-110">Указатель на полученное **\* *значение Byte _. Вызывающий объект отвечает за освобождение памяти путем вызова _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="dfa36-110">Pointer to the retrieved \**BYTE\**_ value. The caller is responsible for freeing the memory by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="dfa36-111">*пкбвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfa36-111">*pcbValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa36-112">Указатель на размер *ппвалуе* в байтах.</span><span class="sxs-lookup"><span data-stu-id="dfa36-112">Pointer to the size of *ppValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa36-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfa36-113">Return value</span></span>

<span data-ttu-id="dfa36-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dfa36-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dfa36-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="dfa36-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dfa36-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dfa36-116">Return code</span></span>                                                                                                            | <span data-ttu-id="dfa36-117">Описание</span><span class="sxs-lookup"><span data-stu-id="dfa36-117">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfa36-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa36-118"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="dfa36-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="dfa36-119">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="dfa36-120"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa36-120"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="dfa36-121">Свойство, указанное *ключом* , не является типом **Byte** \* .</span><span class="sxs-lookup"><span data-stu-id="dfa36-121">The property specified by *key* is not a **BYTE**\* type.</span></span><br/> |
| <dl> <span data-ttu-id="dfa36-122"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa36-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="dfa36-123">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="dfa36-123">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfa36-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfa36-124">Remarks</span></span>

<span data-ttu-id="dfa36-125">Получение буфера **со значением NULL** или буфера нулевого размера не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfa36-125">Retrieving a **NULL** buffer or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa36-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dfa36-126">Requirements</span></span>



| <span data-ttu-id="dfa36-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dfa36-127">Requirement</span></span> | <span data-ttu-id="dfa36-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dfa36-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa36-129">Header</span><span class="sxs-lookup"><span data-stu-id="dfa36-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dfa36-130"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa36-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfa36-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dfa36-131">Library</span></span><br/> | <dl> <span data-ttu-id="dfa36-132"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfa36-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfa36-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfa36-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa36-134">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="dfa36-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="dfa36-135">**Ипортабледевицевалуес:: Сетбуффервалуе**</span><span class="sxs-lookup"><span data-stu-id="dfa36-135">**IPortableDeviceValues::SetBufferValue**</span></span>](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




