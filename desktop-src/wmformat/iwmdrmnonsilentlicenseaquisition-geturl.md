---
title: Метод GetURL Ивмдрмнонсилентлиценсеакуиситион (Вмдрмсдк. h)
description: Метод GetURL извлекает URL-адрес, на который должен быть опубликован запрос лицензии.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Формат Windows Media для метода GetURL
- Метод GetURL Windows Media Format, интерфейс Ивмдрмнонсилентлиценсеакуиситион
- Интерфейс Ивмдрмнонсилентлиценсеакуиситион Windows Media Format, метод GetURL
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675045"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a><span data-ttu-id="a502a-106">Метод Ивмдрмнонсилентлиценсеакуиситион:: GetURL</span><span class="sxs-lookup"><span data-stu-id="a502a-106">IWMDRMNonSilentLicenseAquisition::GetURL method</span></span>

<span data-ttu-id="a502a-107">Метод **getURL** извлекает URL-адрес, на который должен быть опубликован запрос лицензии.</span><span class="sxs-lookup"><span data-stu-id="a502a-107">The **GetURL** method retrieves the URL to which the license challenge should be posted.</span></span>

## <a name="syntax"></a><span data-ttu-id="a502a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a502a-108">Syntax</span></span>


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a><span data-ttu-id="a502a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a502a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a502a-110">*пбструрл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a502a-110">*pbstrURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a502a-111">Адрес переменной, которая получает URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a502a-111">Address of a variable that receives the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a502a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a502a-112">Return value</span></span>

<span data-ttu-id="a502a-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a502a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a502a-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a502a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a502a-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a502a-115">Return code</span></span>                                                                          | <span data-ttu-id="a502a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a502a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a502a-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a502a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a502a-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a502a-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a502a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a502a-119">Remarks</span></span>

<span data-ttu-id="a502a-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="a502a-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a502a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a502a-121">Requirements</span></span>



| <span data-ttu-id="a502a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a502a-122">Requirement</span></span> | <span data-ttu-id="a502a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a502a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a502a-124">Header</span><span class="sxs-lookup"><span data-stu-id="a502a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a502a-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="a502a-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="a502a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a502a-126">Library</span></span><br/> | <dl> <span data-ttu-id="a502a-127"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a502a-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a502a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a502a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a502a-129">**Интерфейс Ивмдрмнонсилентлиценсеакуиситион**</span><span class="sxs-lookup"><span data-stu-id="a502a-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





