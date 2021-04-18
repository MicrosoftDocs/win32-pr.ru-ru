---
description: Метод Жетбулвалуе Извлекает логическое значение (тип VT \_ bool), заданное ключом.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'Метод Ипортабледевицевалуес:: Жетбулвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651807"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a><span data-ttu-id="d2094-103">Метод Ипортабледевицевалуес:: Жетбулвалуе</span><span class="sxs-lookup"><span data-stu-id="d2094-103">IPortableDeviceValues::GetBoolValue method</span></span>

<span data-ttu-id="d2094-104">Метод **жетбулвалуе** извлекает **логическое** значение (тип VT \_ bool), заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="d2094-104">The **GetBoolValue** method retrieves a **Boolean** value (type VT\_BOOL) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2094-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2094-105">Syntax</span></span>


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="d2094-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2094-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2094-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2094-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2094-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="d2094-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d2094-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d2094-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2094-110">Указатель на полученное **логическое** значение.</span><span class="sxs-lookup"><span data-stu-id="d2094-110">Pointer to the retrieved **BOOL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2094-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2094-111">Return value</span></span>

<span data-ttu-id="d2094-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d2094-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d2094-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d2094-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d2094-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d2094-114">Return code</span></span>                                                                                                            | <span data-ttu-id="d2094-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d2094-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2094-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d2094-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="d2094-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d2094-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d2094-118"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d2094-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="d2094-119">Свойство, заданное *ключом* , не является типом **bool** .</span><span class="sxs-lookup"><span data-stu-id="d2094-119">The property specified by *key* is not a **BOOL** type.</span></span><br/>   |
| <dl> <span data-ttu-id="d2094-120"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="d2094-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="d2094-121">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="d2094-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="d2094-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="d2094-122">Examples</span></span>

<span data-ttu-id="d2094-123">Пример использования этого метода см. в разделе [Задание свойств для одного объекта](setting-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="d2094-123">For an example of how to use this method, see [Setting Properties for a Single Object](setting-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2094-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d2094-124">Requirements</span></span>



| <span data-ttu-id="d2094-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d2094-125">Requirement</span></span> | <span data-ttu-id="d2094-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d2094-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2094-127">Header</span><span class="sxs-lookup"><span data-stu-id="d2094-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d2094-128"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2094-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2094-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2094-129">Library</span></span><br/> | <dl> <span data-ttu-id="d2094-130"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2094-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2094-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2094-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2094-132">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="d2094-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d2094-133">**Ипортабледевицевалуес:: SetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="d2094-133">**IPortableDeviceValues::SetBoolValue**</span></span>](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[<span data-ttu-id="d2094-134">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="d2094-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="d2094-135">Задание свойств для одного объекта</span><span class="sxs-lookup"><span data-stu-id="d2094-135">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="d2094-136">Запись свойств содержимого объекта</span><span class="sxs-lookup"><span data-stu-id="d2094-136">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




