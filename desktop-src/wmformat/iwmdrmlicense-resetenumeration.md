---
title: Метод Ивмдрмлиценсе Ресетенумератион (Вмдрмсдк. h)
description: Метод Ресетенумератион сбрасывает список лицензий до исходного состояния. Активная лицензия станет первой лицензией в списке.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Формат Windows Media, Ресетенумератион метод
- Ресетенумератион метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Ресетенумератион
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704291"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a><span data-ttu-id="4ea09-107">Метод Ивмдрмлиценсе:: Ресетенумератион</span><span class="sxs-lookup"><span data-stu-id="4ea09-107">IWMDRMLicense::ResetEnumeration method</span></span>

<span data-ttu-id="4ea09-108">Метод **ресетенумератион** сбрасывает список лицензий до исходного состояния.</span><span class="sxs-lookup"><span data-stu-id="4ea09-108">The **ResetEnumeration** method resets the license list to its original state.</span></span> <span data-ttu-id="4ea09-109">Активная лицензия станет первой лицензией в списке.</span><span class="sxs-lookup"><span data-stu-id="4ea09-109">The active license becomes the first license in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea09-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ea09-110">Syntax</span></span>


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a><span data-ttu-id="4ea09-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ea09-111">Parameters</span></span>

<span data-ttu-id="4ea09-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4ea09-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ea09-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ea09-113">Return value</span></span>

<span data-ttu-id="4ea09-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4ea09-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4ea09-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4ea09-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4ea09-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4ea09-116">Return code</span></span>                                                                                                | <span data-ttu-id="4ea09-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4ea09-117">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="4ea09-118"><dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="4ea09-118"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="4ea09-119">Требуется обновленный список отзыва содержимого.</span><span class="sxs-lookup"><span data-stu-id="4ea09-119">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="4ea09-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4ea09-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="4ea09-121">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4ea09-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="4ea09-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ea09-122">Remarks</span></span>

<span data-ttu-id="4ea09-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="4ea09-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ea09-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4ea09-124">Requirements</span></span>



| <span data-ttu-id="4ea09-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4ea09-125">Requirement</span></span> | <span data-ttu-id="4ea09-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4ea09-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea09-127">Header</span><span class="sxs-lookup"><span data-stu-id="4ea09-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4ea09-128"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ea09-128"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ea09-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4ea09-129">Library</span></span><br/> | <dl> <span data-ttu-id="4ea09-130"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ea09-130"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea09-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ea09-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea09-132">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="4ea09-132">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





