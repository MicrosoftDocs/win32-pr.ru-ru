---
title: Метод Ивмдрмлиценсеманажемент Сторелиценсе (Вмдрмсдк. h)
description: Метод Сторелиценсе включает лицензию, созданную за пределами локальной подсистемы DRM в локальном хранилище лицензий.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Формат Windows Media, Сторелиценсе метод
- Сторелиценсе метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Сторелиценсе
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717823"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a><span data-ttu-id="0ff0d-106">Метод Ивмдрмлиценсеманажемент:: Сторелиценсе</span><span class="sxs-lookup"><span data-stu-id="0ff0d-106">IWMDRMLicenseManagement::StoreLicense method</span></span>

<span data-ttu-id="0ff0d-107">Метод **сторелиценсе** включает лицензию, созданную за пределами локальной подсистемы DRM в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="0ff0d-107">The **StoreLicense** method includes a license that was generated outside of the local DRM subsystem in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff0d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ff0d-108">Syntax</span></span>


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="0ff0d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ff0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff0d-110">*бстрлиценсереспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ff0d-110">*bstrLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff0d-111">Строка ответа лицензии для декодирования и добавления в локальное хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="0ff0d-111">License response string to be decoded and added to the local license store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff0d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ff0d-112">Return value</span></span>

<span data-ttu-id="0ff0d-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0ff0d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0ff0d-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0ff0d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0ff0d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0ff0d-115">Return code</span></span>                                                                          | <span data-ttu-id="0ff0d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0ff0d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0ff0d-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0ff0d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0ff0d-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="0ff0d-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ff0d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ff0d-119">Remarks</span></span>

<span data-ttu-id="0ff0d-120">Этот метод можно использовать для добавления лицензий КСМР, созданных в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="0ff0d-120">You can use this method to add XMR licenses that you have created to the local license store.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff0d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0ff0d-121">Requirements</span></span>



| <span data-ttu-id="0ff0d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0ff0d-122">Requirement</span></span> | <span data-ttu-id="0ff0d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0ff0d-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff0d-124">Header</span><span class="sxs-lookup"><span data-stu-id="0ff0d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0ff0d-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ff0d-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ff0d-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ff0d-126">Library</span></span><br/> | <dl> <span data-ttu-id="0ff0d-127"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ff0d-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ff0d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ff0d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff0d-129">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="0ff0d-129">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





