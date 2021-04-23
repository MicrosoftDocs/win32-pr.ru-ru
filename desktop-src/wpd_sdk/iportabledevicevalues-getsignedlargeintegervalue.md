---
description: Метод Жетсигнедларжеинтежервалуе извлекает значение ЛОНГЛОНГ (Type VT \_ I8), заданное ключом.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: 'Метод Ипортабледевицевалуес:: Жетсигнедларжеинтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5fc41c263ffdef540300a08f88665a6489fa9d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675971"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a><span data-ttu-id="e5b12-103">Метод Ипортабледевицевалуес:: Жетсигнедларжеинтежервалуе</span><span class="sxs-lookup"><span data-stu-id="e5b12-103">IPortableDeviceValues::GetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="e5b12-104">Метод **жетсигнедларжеинтежервалуе** извлекает значение **ЛОНГЛОНГ** (Type VT \_ I8), заданное ключом.</span><span class="sxs-lookup"><span data-stu-id="e5b12-104">The **GetSignedLargeIntegerValue** method retrieves a **LONGLONG** value (type VT\_I8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b12-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5b12-105">Syntax</span></span>


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e5b12-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5b12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b12-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5b12-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b12-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="e5b12-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e5b12-109">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5b12-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b12-110">Указатель на полученное значение **ulong** .</span><span class="sxs-lookup"><span data-stu-id="e5b12-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b12-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5b12-111">Return value</span></span>

<span data-ttu-id="e5b12-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e5b12-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e5b12-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e5b12-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e5b12-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e5b12-114">Return code</span></span>                                                                                                            | <span data-ttu-id="e5b12-115">Описание</span><span class="sxs-lookup"><span data-stu-id="e5b12-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5b12-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e5b12-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="e5b12-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="e5b12-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="e5b12-118"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e5b12-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="e5b12-119">Свойство, указанное *ключом* , не является типом **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="e5b12-119">The property specified by *key* is not a **LONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="e5b12-120"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="e5b12-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="e5b12-121">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5b12-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="e5b12-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e5b12-122">Requirements</span></span>



| <span data-ttu-id="e5b12-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e5b12-123">Requirement</span></span> | <span data-ttu-id="e5b12-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e5b12-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b12-125">Header</span><span class="sxs-lookup"><span data-stu-id="e5b12-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e5b12-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b12-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5b12-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5b12-127">Library</span></span><br/> | <dl> <span data-ttu-id="e5b12-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5b12-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b12-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5b12-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b12-130">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="e5b12-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e5b12-131">**Ипортабледевицевалуес:: Сетсигнедларжеинтежервалуе**</span><span class="sxs-lookup"><span data-stu-id="e5b12-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




