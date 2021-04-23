---
description: Метод Копивалуесфромпропертисторе копирует содержимое объекта Ипропертисторе в коллекцию.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'Метод Ипортабледевицевалуес:: Копивалуесфромпропертисторе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718051"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a><span data-ttu-id="2af7a-103">Метод Ипортабледевицевалуес:: Копивалуесфромпропертисторе</span><span class="sxs-lookup"><span data-stu-id="2af7a-103">IPortableDeviceValues::CopyValuesFromPropertyStore method</span></span>

<span data-ttu-id="2af7a-104">Метод **копивалуесфромпропертисторе** копирует содержимое объекта **ипропертисторе** в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="2af7a-104">The **CopyValuesFromPropertyStore** method copies the contents of an **IPropertyStore** into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2af7a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2af7a-105">Syntax</span></span>


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="2af7a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2af7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2af7a-107">*pStore* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2af7a-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2af7a-108">Указатель на **ипропертисторе** , который необходимо скопировать в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="2af7a-108">Pointer to an **IPropertyStore** to copy into the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2af7a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2af7a-109">Return value</span></span>

<span data-ttu-id="2af7a-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2af7a-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2af7a-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2af7a-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2af7a-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2af7a-112">Return code</span></span>                                                                          | <span data-ttu-id="2af7a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2af7a-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2af7a-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2af7a-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2af7a-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="2af7a-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2af7a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2af7a-116">Remarks</span></span>

<span data-ttu-id="2af7a-117">Этот метод автоматически преобразует все значения **VT \_ BSTR** в значения **VT \_ LPWSTR** .</span><span class="sxs-lookup"><span data-stu-id="2af7a-117">This method automatically converts all **VT\_BSTR** values to **VT\_LPWSTR** values.</span></span>

<span data-ttu-id="2af7a-118">Многие внешние приложения или компоненты, взаимодействующие с приложением, например некоторые приложения оболочки, используют интерфейс **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="2af7a-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="2af7a-119">Этот метод обеспечивает быстрый и простой способ обмена данными с этими программами.</span><span class="sxs-lookup"><span data-stu-id="2af7a-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="2af7a-120">Этот метод поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="2af7a-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="2af7a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2af7a-121">Requirements</span></span>



| <span data-ttu-id="2af7a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2af7a-122">Requirement</span></span> | <span data-ttu-id="2af7a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2af7a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af7a-124">Header</span><span class="sxs-lookup"><span data-stu-id="2af7a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2af7a-125"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2af7a-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2af7a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2af7a-126">Library</span></span><br/> | <dl> <span data-ttu-id="2af7a-127"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2af7a-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2af7a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2af7a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2af7a-129">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="2af7a-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="2af7a-130">**Ипортабледевицевалуес:: Копивалуестопропертисторе**</span><span class="sxs-lookup"><span data-stu-id="2af7a-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span></span>](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




