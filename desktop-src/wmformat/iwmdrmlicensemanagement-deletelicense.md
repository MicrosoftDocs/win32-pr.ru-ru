---
title: Метод Ивмдрмлиценсеманажемент Делетелиценсе (Вмдрмсдк. h)
description: Метод Делетелиценсе удаляет лицензию из временного локального хранилища лицензий.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Формат Windows Media, Делетелиценсе метод
- Делетелиценсе метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Делетелиценсе
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717953"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a><span data-ttu-id="81ba3-106">Ивмдрмлиценсеманажемент: метод:D Елетелиценсе</span><span class="sxs-lookup"><span data-stu-id="81ba3-106">IWMDRMLicenseManagement::DeleteLicense method</span></span>

<span data-ttu-id="81ba3-107">Метод **делетелиценсе** удаляет лицензию из временного локального хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="81ba3-107">The **DeleteLicense** method removes a license from the temporary local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ba3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81ba3-108">Syntax</span></span>


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="81ba3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="81ba3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ba3-110">*бстркид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81ba3-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ba3-111">Идентификатор ключа (Детская) удаляемой лицензии.</span><span class="sxs-lookup"><span data-stu-id="81ba3-111">Key ID (KID) of the license to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="81ba3-112">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81ba3-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ba3-113">Флаги параметра удаления лицензии.</span><span class="sxs-lookup"><span data-stu-id="81ba3-113">License deletion option flags.</span></span> <span data-ttu-id="81ba3-114">Задайте одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="81ba3-114">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="81ba3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="81ba3-115">Value</span></span>                                    | <span data-ttu-id="81ba3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="81ba3-116">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ba3-117">\_Лицензия на удаление WMDRM \_ \_ немедленно</span><span class="sxs-lookup"><span data-stu-id="81ba3-117">WMDRM\_DELETE\_LICENSE\_IMMEDIATELY</span></span>      | <span data-ttu-id="81ba3-118">Указывает, что лицензия должна быть немедленно удалена из хранилища.</span><span class="sxs-lookup"><span data-stu-id="81ba3-118">Specifies that the license should be removed from the store immediately.</span></span>                                                                                                                              |
| <span data-ttu-id="81ba3-119">\_ \_ лицензионный маркер удаления WMDRM \_ \_ для \_ очистки</span><span class="sxs-lookup"><span data-stu-id="81ba3-119">WMDRM\_DELETE\_LICENSE\_MARK\_FOR\_PURGE</span></span> | <span data-ttu-id="81ba3-120">Указывает, что лицензия должна быть помечена для удаления, но не должна удаляться из хранилища до тех пор, пока не будет вызван метод [**клеанлиценсесторе**](iwmdrmlicensemanagement-cleanlicensestore.md) .</span><span class="sxs-lookup"><span data-stu-id="81ba3-120">Specifies that the license should be marked for deletion, but should not be removed from the store until the [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) method is called.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ba3-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81ba3-121">Return value</span></span>

<span data-ttu-id="81ba3-122">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="81ba3-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="81ba3-123">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="81ba3-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="81ba3-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="81ba3-124">Return code</span></span>                                                                                            | <span data-ttu-id="81ba3-125">Описание</span><span class="sxs-lookup"><span data-stu-id="81ba3-125">Description</span></span>                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81ba3-126"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="81ba3-126"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="81ba3-127">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="81ba3-127">The method succeeded.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="81ba3-128"><dt>**DRM \_ E \_ лиценсенотфаунд**</dt></span><span class="sxs-lookup"><span data-stu-id="81ba3-128"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="81ba3-129">Указанная лицензия не существует в хранилище.</span><span class="sxs-lookup"><span data-stu-id="81ba3-129">The specified license does not exist in the store.</span></span><br/> <span data-ttu-id="81ba3-130">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="81ba3-130">- OR -</span></span><br/> <span data-ttu-id="81ba3-131">Хранилище не найдено.</span><span class="sxs-lookup"><span data-stu-id="81ba3-131">The store was not found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81ba3-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81ba3-132">Remarks</span></span>

<span data-ttu-id="81ba3-133">Чтобы удалить лицензии из постоянного локального хранилища лицензий, необходимо использовать отзыв лицензий.</span><span class="sxs-lookup"><span data-stu-id="81ba3-133">To delete licenses from the permanent local license store, you must use license revocation.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ba3-134">Требования</span><span class="sxs-lookup"><span data-stu-id="81ba3-134">Requirements</span></span>



| <span data-ttu-id="81ba3-135">Требование</span><span class="sxs-lookup"><span data-stu-id="81ba3-135">Requirement</span></span> | <span data-ttu-id="81ba3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="81ba3-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81ba3-137">Header</span><span class="sxs-lookup"><span data-stu-id="81ba3-137">Header</span></span><br/>  | <dl> <span data-ttu-id="81ba3-138"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="81ba3-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="81ba3-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81ba3-139">Library</span></span><br/> | <dl> <span data-ttu-id="81ba3-140"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81ba3-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81ba3-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81ba3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ba3-142">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="81ba3-142">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





