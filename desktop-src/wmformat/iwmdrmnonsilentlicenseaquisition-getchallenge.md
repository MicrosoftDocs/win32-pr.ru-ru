---
title: Метод Ивмдрмнонсилентлиценсеакуиситион (Вмдрмсдк. h)
description: Метод метода WebMethod извлекает запрос лицензии, который должен быть опубликован на сервере лицензирования.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Метод вызова Windows Media Format
- Метод Ивмдрмнонсилентлиценсеакуиситион формат Windows Media, интерфейс
- Интерфейс Ивмдрмнонсилентлиценсеакуиситион интерфейса Windows Media Format, метод Challenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675389"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a><span data-ttu-id="4fc03-106">Метод Ивмдрмнонсилентлиценсеакуиситион:: Challenge</span><span class="sxs-lookup"><span data-stu-id="4fc03-106">IWMDRMNonSilentLicenseAquisition::GetChallenge method</span></span>

<span data-ttu-id="4fc03-107">Метод **метода WebMethod** извлекает запрос лицензии, который должен быть опубликован на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="4fc03-107">The **GetChallenge** method retrieves the license challenge that should be posted to the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc03-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fc03-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="4fc03-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fc03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc03-110">*пбстрчалленже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4fc03-110">*pbstrChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc03-111">Адрес переменной, которая получает запрос лицензии.</span><span class="sxs-lookup"><span data-stu-id="4fc03-111">Address of a variable that receives the license challenge.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc03-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fc03-112">Return value</span></span>

<span data-ttu-id="4fc03-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4fc03-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4fc03-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4fc03-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4fc03-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4fc03-115">Return code</span></span>                                                                          | <span data-ttu-id="4fc03-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4fc03-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4fc03-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4fc03-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4fc03-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4fc03-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4fc03-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fc03-119">Remarks</span></span>

<span data-ttu-id="4fc03-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="4fc03-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc03-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4fc03-121">Requirements</span></span>



| <span data-ttu-id="4fc03-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4fc03-122">Requirement</span></span> | <span data-ttu-id="4fc03-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4fc03-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc03-124">Header</span><span class="sxs-lookup"><span data-stu-id="4fc03-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4fc03-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc03-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fc03-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4fc03-126">Library</span></span><br/> | <dl> <span data-ttu-id="4fc03-127"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fc03-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc03-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fc03-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc03-129">**Интерфейс Ивмдрмнонсилентлиценсеакуиситион**</span><span class="sxs-lookup"><span data-stu-id="4fc03-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





