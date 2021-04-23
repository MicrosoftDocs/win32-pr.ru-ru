---
title: Метод Ивмдрмлиценсе Канперсист (Вмдрмсдк. h)
description: Метод Канперсист запрашивает возможность сохранения лицензии в локальном хранилище лицензий.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Формат Windows Media, Канперсист метод
- Канперсист метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Канперсист
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704477"
---
# <a name="iwmdrmlicensecanpersist-method"></a><span data-ttu-id="127da-106">Метод Ивмдрмлиценсе:: Канперсист</span><span class="sxs-lookup"><span data-stu-id="127da-106">IWMDRMLicense::CanPersist method</span></span>

<span data-ttu-id="127da-107">Метод **канперсист** запрашивает возможность сохранения лицензии в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="127da-107">The **CanPersist** method queries whether the license can be persisted on in a local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="127da-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="127da-108">Syntax</span></span>


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a><span data-ttu-id="127da-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="127da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="127da-110">*пфканперсист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="127da-110">*pfCanPersist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="127da-111">Значение TRUE указывает, что лицензия может быть сохранена.</span><span class="sxs-lookup"><span data-stu-id="127da-111">TRUE indicates that the license can be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="127da-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="127da-112">Return value</span></span>

<span data-ttu-id="127da-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="127da-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="127da-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="127da-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="127da-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="127da-115">Return code</span></span>                                                                          | <span data-ttu-id="127da-116">Описание</span><span class="sxs-lookup"><span data-stu-id="127da-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="127da-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="127da-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="127da-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="127da-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="127da-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="127da-119">Remarks</span></span>

<span data-ttu-id="127da-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="127da-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="127da-121">Требования</span><span class="sxs-lookup"><span data-stu-id="127da-121">Requirements</span></span>



| <span data-ttu-id="127da-122">Требование</span><span class="sxs-lookup"><span data-stu-id="127da-122">Requirement</span></span> | <span data-ttu-id="127da-123">Значение</span><span class="sxs-lookup"><span data-stu-id="127da-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="127da-124">Header</span><span class="sxs-lookup"><span data-stu-id="127da-124">Header</span></span><br/> | <dl> <span data-ttu-id="127da-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="127da-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="127da-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="127da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127da-127">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="127da-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





