---
title: Метод Ивмдрмлиценсе-License (Вмдрмсдк. h)
description: Метод КСМР извлекает лицензию как данные XML или.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Формат Windows Media для метода с лицензией
- Метод Ивмдрмлиценсе формат Windows Media, интерфейс
- Интерфейс Ивмдрмлиценсе интерфейса Windows Media Format, метод onlicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704474"
---
# <a name="iwmdrmlicensegetlicense-method"></a><span data-ttu-id="59eb6-106">Метод Ивмдрмлиценсе:: License</span><span class="sxs-lookup"><span data-stu-id="59eb6-106">IWMDRMLicense::GetLicense method</span></span>

<span data-ttu-id="59eb6-107">Метод **КСМР извлекает лицензию как** данные XML или.</span><span class="sxs-lookup"><span data-stu-id="59eb6-107">The **GetLicense** method retrieves the license as XML or XMR data.</span></span>

## <a name="syntax"></a><span data-ttu-id="59eb6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59eb6-108">Syntax</span></span>


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a><span data-ttu-id="59eb6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="59eb6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59eb6-110">*ппблиценсе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="59eb6-110">*ppbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb6-111">Получает лицензию.</span><span class="sxs-lookup"><span data-stu-id="59eb6-111">Receives the license.</span></span>

</dd> <dt>

<span data-ttu-id="59eb6-112">*пкблиценсе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="59eb6-112">*pcbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb6-113">Получает размер лицензии.</span><span class="sxs-lookup"><span data-stu-id="59eb6-113">Receives the size of the license.</span></span>

</dd> <dt>

<span data-ttu-id="59eb6-114">*пдвлиценсетипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="59eb6-114">*pdwLicenseType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb6-115">Получает тип возвращенной лицензии.</span><span class="sxs-lookup"><span data-stu-id="59eb6-115">Receives the type of the license returned.</span></span> <span data-ttu-id="59eb6-116">Это значение устанавливается равным одной из констант в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="59eb6-116">This value is set to one of the constants in the following table.</span></span>



| <span data-ttu-id="59eb6-117">Константа</span><span class="sxs-lookup"><span data-stu-id="59eb6-117">Constant</span></span>                  | <span data-ttu-id="59eb6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="59eb6-118">Description</span></span>                            |
|---------------------------|----------------------------------------|
| <span data-ttu-id="59eb6-119">\_ \_ XML типа лицензии \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="59eb6-119">WMDRM\_LICENSE\_TYPE\_XML</span></span> | <span data-ttu-id="59eb6-120">Полученная лицензия форматируется как XML.</span><span class="sxs-lookup"><span data-stu-id="59eb6-120">Retrieved license is formatted as XML.</span></span> |
| <span data-ttu-id="59eb6-121">\_тип лицензии \_ WMDRM \_ КСМР</span><span class="sxs-lookup"><span data-stu-id="59eb6-121">WMDRM\_LICENSE\_TYPE\_XMR</span></span> | <span data-ttu-id="59eb6-122">Полученная лицензия отформатирована как КСМР.</span><span class="sxs-lookup"><span data-stu-id="59eb6-122">Retrieved license is formatted as XMR.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59eb6-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59eb6-123">Return value</span></span>

<span data-ttu-id="59eb6-124">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="59eb6-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="59eb6-125">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="59eb6-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="59eb6-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="59eb6-126">Return code</span></span>                                                                          | <span data-ttu-id="59eb6-127">Описание</span><span class="sxs-lookup"><span data-stu-id="59eb6-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="59eb6-128"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="59eb6-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="59eb6-129">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="59eb6-129">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59eb6-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59eb6-130">Remarks</span></span>

<span data-ttu-id="59eb6-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="59eb6-131">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="59eb6-132">Требования</span><span class="sxs-lookup"><span data-stu-id="59eb6-132">Requirements</span></span>



| <span data-ttu-id="59eb6-133">Требование</span><span class="sxs-lookup"><span data-stu-id="59eb6-133">Requirement</span></span> | <span data-ttu-id="59eb6-134">Значение</span><span class="sxs-lookup"><span data-stu-id="59eb6-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59eb6-135">Header</span><span class="sxs-lookup"><span data-stu-id="59eb6-135">Header</span></span><br/>  | <dl> <span data-ttu-id="59eb6-136"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="59eb6-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="59eb6-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59eb6-137">Library</span></span><br/> | <dl> <span data-ttu-id="59eb6-138"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59eb6-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59eb6-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59eb6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59eb6-140">**жетлиценсепроперти**</span><span class="sxs-lookup"><span data-stu-id="59eb6-140">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[<span data-ttu-id="59eb6-141">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="59eb6-141">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





