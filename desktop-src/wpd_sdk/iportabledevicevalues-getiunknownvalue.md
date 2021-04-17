---
description: Метод Жетиункновнвалуе извлекает значение интерфейса IUnknown (тип VT \_ Unknown), заданный ключом.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'Метод Ипортабледевицевалуес:: Жетиункновнвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718155"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a><span data-ttu-id="df9b1-103">Метод Ипортабледевицевалуес:: Жетиункновнвалуе</span><span class="sxs-lookup"><span data-stu-id="df9b1-103">IPortableDeviceValues::GetIUnknownValue method</span></span>

<span data-ttu-id="df9b1-104">Метод **жетиункновнвалуе** извлекает значение интерфейса **IUnknown** (тип VT \_ Unknown), заданный ключом.</span><span class="sxs-lookup"><span data-stu-id="df9b1-104">The **GetIUnknownValue** method retrieves an **IUnknown** interface value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="df9b1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df9b1-105">Syntax</span></span>


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="df9b1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df9b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df9b1-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df9b1-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9b1-108">Ключ **рефпропертикэй** , указывающий извлекаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="df9b1-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="df9b1-109">*ппвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="df9b1-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df9b1-110">Адрес переменной, которая получает указатель на полученный интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="df9b1-110">Address of a variable that receives a pointer to the retrieved **IUnknown** interface.</span></span> <span data-ttu-id="df9b1-111">Вызывающий объект отвечает за вызов метода **Release** на полученном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="df9b1-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df9b1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df9b1-112">Return value</span></span>

<span data-ttu-id="df9b1-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="df9b1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="df9b1-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="df9b1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="df9b1-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="df9b1-115">Return code</span></span>                                                                                                            | <span data-ttu-id="df9b1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="df9b1-116">Description</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df9b1-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="df9b1-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="df9b1-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="df9b1-118">The method succeeded.</span></span><br/>                                             |
| <dl> <span data-ttu-id="df9b1-119"><dt>**\_вытипемисматч E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df9b1-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="df9b1-120">Свойство, заданное *ключом* , не является интерфейсом **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="df9b1-120">The property specified by *key* is not an **IUnknown** interface.</span></span><br/> |
| <dl> <span data-ttu-id="df9b1-121"><dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt></span><span class="sxs-lookup"><span data-stu-id="df9b1-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="df9b1-122">Свойство, указанное *ключом* , отсутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="df9b1-122">The property specified by *key* is not in the collection.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="df9b1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="df9b1-123">Requirements</span></span>



| <span data-ttu-id="df9b1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="df9b1-124">Requirement</span></span> | <span data-ttu-id="df9b1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="df9b1-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df9b1-126">Header</span><span class="sxs-lookup"><span data-stu-id="df9b1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="df9b1-127"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="df9b1-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="df9b1-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="df9b1-128">Library</span></span><br/> | <dl> <span data-ttu-id="df9b1-129"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df9b1-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df9b1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df9b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9b1-131">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="df9b1-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="df9b1-132">**Ипортабледевицевалуес:: Сетиункновнвалуе**</span><span class="sxs-lookup"><span data-stu-id="df9b1-132">**IPortableDeviceValues::SetIUnknownValue**</span></span>](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




