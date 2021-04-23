---
title: Метод Ивмдрмлиценсе-Next (Вмдрмсдк. h)
description: Метод GetNext загружает сведения о следующем элементе в списке.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Метод GetNext Windows Media Format
- Метод GetNext Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод GetNext
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704229"
---
# <a name="iwmdrmlicensegetnext-method"></a><span data-ttu-id="769c8-106">Метод Ивмдрмлиценсе:: GetNext</span><span class="sxs-lookup"><span data-stu-id="769c8-106">IWMDRMLicense::GetNext method</span></span>

<span data-ttu-id="769c8-107">Метод **GetNext** загружает сведения о следующем элементе в списке.</span><span class="sxs-lookup"><span data-stu-id="769c8-107">The **GetNext** method loads the information about the next item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="769c8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="769c8-108">Syntax</span></span>


```C++
HRESULT GetNext();
```



## <a name="parameters"></a><span data-ttu-id="769c8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="769c8-109">Parameters</span></span>

<span data-ttu-id="769c8-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="769c8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="769c8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="769c8-111">Return value</span></span>

<span data-ttu-id="769c8-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="769c8-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="769c8-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="769c8-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="769c8-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="769c8-114">Return code</span></span>                                                                                                | <span data-ttu-id="769c8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="769c8-115">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="769c8-116"><dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="769c8-116"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="769c8-117">Требуется обновленный список отзыва содержимого.</span><span class="sxs-lookup"><span data-stu-id="769c8-117">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="769c8-118"><dt>**Ошибка \_ больше \_ нет \_ элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="769c8-118"><dt>**ERROR\_NO\_MORE\_ITEMS**</dt></span></span> </dl>      | <span data-ttu-id="769c8-119">В списке больше нет элементов.</span><span class="sxs-lookup"><span data-stu-id="769c8-119">There are no more items in the list.</span></span><br/>          |
| <dl> <span data-ttu-id="769c8-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="769c8-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="769c8-121">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="769c8-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="769c8-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="769c8-122">Remarks</span></span>

<span data-ttu-id="769c8-123">Методы интерфейса [**ивмдрмлиценсе**](iwmdrmlicense.md) предоставляют данные об одной лицензии за раз.</span><span class="sxs-lookup"><span data-stu-id="769c8-123">The methods of the [**IWMDRMLicense**](iwmdrmlicense.md) interface provide data about a single license at a time.</span></span> <span data-ttu-id="769c8-124">Базовый объект содержит список из одной или нескольких лицензий.</span><span class="sxs-lookup"><span data-stu-id="769c8-124">The underlying object contains a list of one or more licenses.</span></span> <span data-ttu-id="769c8-125">При вызове этого метода интерфейс перемещает свои внутренние ссылки на следующую лицензию в списке.</span><span class="sxs-lookup"><span data-stu-id="769c8-125">When you call this method, the interface moves its internal references to the next license in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="769c8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="769c8-126">Requirements</span></span>



| <span data-ttu-id="769c8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="769c8-127">Requirement</span></span> | <span data-ttu-id="769c8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="769c8-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="769c8-129">Header</span><span class="sxs-lookup"><span data-stu-id="769c8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="769c8-130"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="769c8-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="769c8-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="769c8-131">Library</span></span><br/> | <dl> <span data-ttu-id="769c8-132"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="769c8-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="769c8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="769c8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="769c8-134">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="769c8-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





