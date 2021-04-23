---
description: Метод Жетфлоатвалуе извлекает значение FLOAT (тип VT \_ R4), заданное ключом.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'Метод Ипортабледевицевалуес:: Жетфлоатвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648702"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a><span data-ttu-id="224ae-103">Метод Ипортабледевицевалуес:: Жетфлоатвалуе</span><span class="sxs-lookup"><span data-stu-id="224ae-103">IPortableDeviceValues::GetFloatValue method</span></span>

<span data-ttu-id="224ae-104">Метод **жетфлоатвалуе** извлекает значение **float** (тип VT \_ R4), заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="224ae-104">The **GetFloatValue** method retrieves a **FLOAT** value (type VT\_R4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="224ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="224ae-105">Syntax</span></span>


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="224ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="224ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224ae-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="224ae-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="224ae-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="224ae-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="224ae-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="224ae-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="224ae-110">Указатель на полученное значение **float** .</span><span class="sxs-lookup"><span data-stu-id="224ae-110">Pointer to the retrieved **FLOAT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="224ae-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="224ae-111">Return value</span></span>

<span data-ttu-id="224ae-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="224ae-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="224ae-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="224ae-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="224ae-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="224ae-114">Return code</span></span>                                                                                             | <span data-ttu-id="224ae-115">Описание</span><span class="sxs-lookup"><span data-stu-id="224ae-115">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="224ae-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="224ae-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="224ae-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="224ae-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="224ae-118"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="224ae-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>    | <span data-ttu-id="224ae-119">Свойство, указанное *ключом* , не имеет тип **float** .</span><span class="sxs-lookup"><span data-stu-id="224ae-119">The property specified by *key* is not a **FLOAT** type.</span></span><br/>  |
| <dl> <span data-ttu-id="224ae-120"><dt>**идентификатор "E \_ prop" \_ \_ не поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="224ae-120"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="224ae-121">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="224ae-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="224ae-122">Требования</span><span class="sxs-lookup"><span data-stu-id="224ae-122">Requirements</span></span>



| <span data-ttu-id="224ae-123">Требование</span><span class="sxs-lookup"><span data-stu-id="224ae-123">Requirement</span></span> | <span data-ttu-id="224ae-124">Значение</span><span class="sxs-lookup"><span data-stu-id="224ae-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="224ae-125">Header</span><span class="sxs-lookup"><span data-stu-id="224ae-125">Header</span></span><br/>  | <dl> <span data-ttu-id="224ae-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="224ae-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="224ae-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="224ae-127">Library</span></span><br/> | <dl> <span data-ttu-id="224ae-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="224ae-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="224ae-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="224ae-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224ae-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="224ae-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="224ae-131">**Ипортабледевицевалуес:: Сетфлоатвалуе**</span><span class="sxs-lookup"><span data-stu-id="224ae-131">**IPortableDeviceValues::SetFloatValue**</span></span>](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




