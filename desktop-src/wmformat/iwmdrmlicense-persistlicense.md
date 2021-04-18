---
title: Метод Ивмдрмлиценсе Персистлиценсе (Вмдрмсдк. h)
description: Метод Персистлиценсе сохраняет текущую лицензию из временного хранилища в постоянное локальное хранилище лицензий.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Формат Windows Media, Персистлиценсе метод
- Персистлиценсе метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Персистлиценсе
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704401"
---
# <a name="iwmdrmlicensepersistlicense-method"></a><span data-ttu-id="fdb33-106">Ивмдрмлиценсе: метод:P Ерсистлиценсе</span><span class="sxs-lookup"><span data-stu-id="fdb33-106">IWMDRMLicense::PersistLicense method</span></span>

<span data-ttu-id="fdb33-107">Метод **персистлиценсе** сохраняет текущую лицензию из временного хранилища в постоянное локальное хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="fdb33-107">The **PersistLicense** method saves the current license from the temporary store into the permanent local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb33-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdb33-108">Syntax</span></span>


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a><span data-ttu-id="fdb33-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdb33-109">Parameters</span></span>

<span data-ttu-id="fdb33-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fdb33-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdb33-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdb33-111">Return value</span></span>

<span data-ttu-id="fdb33-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fdb33-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fdb33-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fdb33-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fdb33-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fdb33-114">Return code</span></span>                                                                          | <span data-ttu-id="fdb33-115">Описание</span><span class="sxs-lookup"><span data-stu-id="fdb33-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fdb33-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fdb33-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fdb33-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="fdb33-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fdb33-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fdb33-118">Remarks</span></span>

<span data-ttu-id="fdb33-119">Если текущая лицензия не находится во временном хранилище, этот метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="fdb33-119">If the current license is not in the temporary store, this method will fail.</span></span>

<span data-ttu-id="fdb33-120">Можно вызвать [**канперсист**](iwmdrmlicense-canpersist.md) , чтобы запросить, разрешено ли сохранение лицензии.</span><span class="sxs-lookup"><span data-stu-id="fdb33-120">You can call [**CanPersist**](iwmdrmlicense-canpersist.md) to query whether the license is allowed to be persisted.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdb33-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fdb33-121">Requirements</span></span>



| <span data-ttu-id="fdb33-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fdb33-122">Requirement</span></span> | <span data-ttu-id="fdb33-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fdb33-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb33-124">Header</span><span class="sxs-lookup"><span data-stu-id="fdb33-124">Header</span></span><br/> | <dl> <span data-ttu-id="fdb33-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdb33-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdb33-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdb33-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb33-127">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="fdb33-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





