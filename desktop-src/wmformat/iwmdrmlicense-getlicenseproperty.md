---
title: Метод Ивмдрмлиценсе Жетлиценсепроперти (Вмдрмсдк. h)
description: Метод Жетлиценсепроперти извлекает свойство из текущей лицензии.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Формат Windows Media, Жетлиценсепроперти метод
- Жетлиценсепроперти метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Жетлиценсепроперти
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704171"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a><span data-ttu-id="68e22-106">Метод Ивмдрмлиценсе:: Жетлиценсепроперти</span><span class="sxs-lookup"><span data-stu-id="68e22-106">IWMDRMLicense::GetLicenseProperty method</span></span>

<span data-ttu-id="68e22-107">Метод **жетлиценсепроперти** извлекает свойство из текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="68e22-107">The **GetLicenseProperty** method retrieves a property from the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e22-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68e22-108">Syntax</span></span>


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a><span data-ttu-id="68e22-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="68e22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68e22-110">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68e22-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68e22-111">Имя извлекаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="68e22-111">Name of the property to retrieve.</span></span> <span data-ttu-id="68e22-112">Задайте одну из констант в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="68e22-112">Set to one of the constants in the following table:</span></span>



| <span data-ttu-id="68e22-113">Константа</span><span class="sxs-lookup"><span data-stu-id="68e22-113">Constant</span></span>                   | <span data-ttu-id="68e22-114">Описание</span><span class="sxs-lookup"><span data-stu-id="68e22-114">Description</span></span>                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68e22-115">g \_ всзвмдрмнет, \_ отзыв</span><span class="sxs-lookup"><span data-stu-id="68e22-115">g\_wszWMDRMNet\_Revocation</span></span> | <span data-ttu-id="68e22-116">Используйте для получения списка отзыва Windows Media DRM для сетевых устройств для текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="68e22-116">Use to get the Windows Media DRM for Network Devices revocation list for the current license.</span></span>                        |
| <span data-ttu-id="68e22-117">g \_ всзвмдрм \_ саплевел</span><span class="sxs-lookup"><span data-stu-id="68e22-117">g\_wszWMDRM\_SAPLEVEL</span></span>      | <span data-ttu-id="68e22-118">Используйте, чтобы получить уровень защищенного звукового пути (SAP), необходимый для воспроизведения содержимого, охваченного текущей лицензией.</span><span class="sxs-lookup"><span data-stu-id="68e22-118">Use to get the Secure Audio Path (SAP) level required to play content covered by the current license.</span></span>                |
| <span data-ttu-id="68e22-119">g \_ всзвмдрм \_ сапрекуиред</span><span class="sxs-lookup"><span data-stu-id="68e22-119">g\_wszWMDRM\_SAPRequired</span></span>   | <span data-ttu-id="68e22-120">Используйте, чтобы определить, требуется ли для текущей лицензии использование SAP для воспроизведения содержимого.</span><span class="sxs-lookup"><span data-stu-id="68e22-120">Use to ascertain whether the current license requires SAP be used to play the content.</span></span>                               |
| <span data-ttu-id="68e22-121">g \_ всзвмдрм \_ SOURCEID</span><span class="sxs-lookup"><span data-stu-id="68e22-121">g\_wszWMDRM\_SOURCEID</span></span>      | <span data-ttu-id="68e22-122">Используйте, чтобы получить идентификатор источника для текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="68e22-122">Use to get the source identifier for the current license.</span></span>                                                            |
| <span data-ttu-id="68e22-123">g \_ всзвмдрм \_ приоритет</span><span class="sxs-lookup"><span data-stu-id="68e22-123">g\_wszWMDRM\_PRIORITY</span></span>      | <span data-ttu-id="68e22-124">Используйте для получения приоритета текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="68e22-124">Use to get the priority of the current license.</span></span> <span data-ttu-id="68e22-125">Лицензии с более высоким приоритетом применяются до лицензий с более низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="68e22-125">Higher priority licenses are applied before lower priority licenses.</span></span> |
| <span data-ttu-id="68e22-126">g \_ всзвмдрм \_</span><span class="sxs-lookup"><span data-stu-id="68e22-126">g\_wszWMDRM\_UplinkID</span></span>      | <span data-ttu-id="68e22-127">Используйте, чтобы получить идентификатор ключа корневой лицензии в цепочке лицензий, к которой принадлежит Текущая лицензия.</span><span class="sxs-lookup"><span data-stu-id="68e22-127">Use to get the key ID of the root license in the license chain that the current license belongs to.</span></span>                  |



 

</dd> <dt>

<span data-ttu-id="68e22-128">*ппропвариант* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68e22-128">*ppropVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68e22-129">Получает значение свойства.</span><span class="sxs-lookup"><span data-stu-id="68e22-129">Receives the property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68e22-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68e22-130">Return value</span></span>

<span data-ttu-id="68e22-131">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="68e22-131">The method returns an **HRESULT**.</span></span> <span data-ttu-id="68e22-132">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="68e22-132">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="68e22-133">Код возврата</span><span class="sxs-lookup"><span data-stu-id="68e22-133">Return code</span></span>                                                                          | <span data-ttu-id="68e22-134">Описание</span><span class="sxs-lookup"><span data-stu-id="68e22-134">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="68e22-135"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="68e22-135"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="68e22-136">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="68e22-136">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68e22-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68e22-137">Remarks</span></span>

<span data-ttu-id="68e22-138">Нет.</span><span class="sxs-lookup"><span data-stu-id="68e22-138">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="68e22-139">Требования</span><span class="sxs-lookup"><span data-stu-id="68e22-139">Requirements</span></span>



| <span data-ttu-id="68e22-140">Требование</span><span class="sxs-lookup"><span data-stu-id="68e22-140">Requirement</span></span> | <span data-ttu-id="68e22-141">Значение</span><span class="sxs-lookup"><span data-stu-id="68e22-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68e22-142">Header</span><span class="sxs-lookup"><span data-stu-id="68e22-142">Header</span></span><br/>  | <dl> <span data-ttu-id="68e22-143"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="68e22-143"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="68e22-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68e22-144">Library</span></span><br/> | <dl> <span data-ttu-id="68e22-145"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68e22-145"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68e22-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68e22-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e22-147">**Лицензия**</span><span class="sxs-lookup"><span data-stu-id="68e22-147">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)
</dt> <dt>

[<span data-ttu-id="68e22-148">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="68e22-148">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





