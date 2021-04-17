---
description: Метод Копивалуестопропертисторе копирует все значения из коллекции в интерфейс Ипропертисторе.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'Метод Ипортабледевицевалуес:: Копивалуестопропертисторе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708394"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a><span data-ttu-id="0abb1-103">Метод Ипортабледевицевалуес:: Копивалуестопропертисторе</span><span class="sxs-lookup"><span data-stu-id="0abb1-103">IPortableDeviceValues::CopyValuesToPropertyStore method</span></span>

<span data-ttu-id="0abb1-104">Метод **копивалуестопропертисторе** копирует все значения из коллекции в интерфейс **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="0abb1-104">The **CopyValuesToPropertyStore** method copies all the values from a collection into an **IPropertyStore** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0abb1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0abb1-105">Syntax</span></span>


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="0abb1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0abb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0abb1-107">*pStore* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0abb1-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0abb1-108">Указатель на объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="0abb1-108">Pointer to a store object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0abb1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0abb1-109">Return value</span></span>

<span data-ttu-id="0abb1-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0abb1-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0abb1-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0abb1-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0abb1-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0abb1-112">Return code</span></span>                                                                          | <span data-ttu-id="0abb1-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0abb1-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0abb1-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0abb1-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0abb1-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="0abb1-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0abb1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0abb1-116">Remarks</span></span>

<span data-ttu-id="0abb1-117">Этот метод не преобразует значения VT \_ LPWSTR в VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="0abb1-117">This method does not convert values of VT\_LPWSTR into VT\_BSTR.</span></span> <span data-ttu-id="0abb1-118">Многие внешние приложения или компоненты, взаимодействующие с приложением, например некоторые приложения оболочки, используют интерфейс **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="0abb1-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="0abb1-119">Этот метод обеспечивает быстрый и простой способ обмена данными с этими программами.</span><span class="sxs-lookup"><span data-stu-id="0abb1-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="0abb1-120">Этот метод поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="0abb1-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="0abb1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0abb1-121">Requirements</span></span>



| <span data-ttu-id="0abb1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0abb1-122">Requirement</span></span> | <span data-ttu-id="0abb1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0abb1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0abb1-124">Header</span><span class="sxs-lookup"><span data-stu-id="0abb1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0abb1-125"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="0abb1-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0abb1-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0abb1-126">Library</span></span><br/> | <dl> <span data-ttu-id="0abb1-127"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0abb1-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0abb1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0abb1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abb1-129">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="0abb1-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0abb1-130">**Ипортабледевицевалуес:: Копивалуесфромпропертисторе**</span><span class="sxs-lookup"><span data-stu-id="0abb1-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span></span>](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




