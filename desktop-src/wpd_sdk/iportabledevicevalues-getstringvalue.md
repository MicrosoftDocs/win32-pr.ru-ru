---
description: Метод GetStringValue извлекает строковое значение (тип VT \_ LPWSTR), заданное ключом.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'Метод Ипортабледевицевалуес:: GetStringValue (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698962"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a><span data-ttu-id="1a30a-103">Метод Ипортабледевицевалуес:: GetStringValue</span><span class="sxs-lookup"><span data-stu-id="1a30a-103">IPortableDeviceValues::GetStringValue method</span></span>

<span data-ttu-id="1a30a-104">Метод **GetStringValue** извлекает строковое значение (тип VT \_ LPWSTR), заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="1a30a-104">The **GetStringValue** method retrieves a string value (type VT\_LPWSTR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a30a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a30a-105">Syntax</span></span>


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="1a30a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a30a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a30a-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a30a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a30a-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="1a30a-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="1a30a-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1a30a-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a30a-110">Указатель на полученное значение **LPWSTR** .</span><span class="sxs-lookup"><span data-stu-id="1a30a-110">Pointer to the retrieved **LPWSTR** value.</span></span> <span data-ttu-id="1a30a-111">Вызывающий объект отвечает за вызов **CoTaskMemFree** для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="1a30a-111">The caller is responsible for calling **CoTaskMemFree** to release the memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a30a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a30a-112">Return value</span></span>

<span data-ttu-id="1a30a-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1a30a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1a30a-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1a30a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1a30a-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1a30a-115">Return code</span></span>                                                                                                            | <span data-ttu-id="1a30a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1a30a-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a30a-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1a30a-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="1a30a-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1a30a-118">The method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="1a30a-119"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a30a-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="1a30a-120">Свойство, заданное *ключом* , не является типом **LPWSTR** .</span><span class="sxs-lookup"><span data-stu-id="1a30a-120">The property specified by *key* is not an **LPWSTR** type.</span></span><br/> |
| <dl> <span data-ttu-id="1a30a-121"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="1a30a-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="1a30a-122">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1a30a-122">The property specified by *key* is not in the collection.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="1a30a-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="1a30a-123">Examples</span></span>

<span data-ttu-id="1a30a-124">Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="1a30a-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a30a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1a30a-125">Requirements</span></span>



| <span data-ttu-id="1a30a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1a30a-126">Requirement</span></span> | <span data-ttu-id="1a30a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1a30a-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a30a-128">Header</span><span class="sxs-lookup"><span data-stu-id="1a30a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1a30a-129"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a30a-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a30a-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1a30a-130">Library</span></span><br/> | <dl> <span data-ttu-id="1a30a-131"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a30a-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a30a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a30a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a30a-133">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="1a30a-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="1a30a-134">**Ипортабледевицевалуес:: GetAt**</span><span class="sxs-lookup"><span data-stu-id="1a30a-134">**IPortableDeviceValues::GetAt**</span></span>](iportabledevicevalues-getat.md)
</dt> <dt>

[<span data-ttu-id="1a30a-135">**Ипортабледевицевалуес:: SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="1a30a-135">**IPortableDeviceValues::SetStringValue**</span></span>](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[<span data-ttu-id="1a30a-136">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="1a30a-136">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="1a30a-137">Получение поддерживаемых форматов службы</span><span class="sxs-lookup"><span data-stu-id="1a30a-137">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="1a30a-138">Получение поддерживаемых методов службы</span><span class="sxs-lookup"><span data-stu-id="1a30a-138">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




