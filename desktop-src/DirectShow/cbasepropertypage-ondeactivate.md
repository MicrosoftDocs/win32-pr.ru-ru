---
description: Метод OnDeactivate вызывается при уничтожении окна диалогового окна.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Метод Кбасепропертипаже. OnDeactivate (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669361"
---
# <a name="cbasepropertypageondeactivate-method"></a><span data-ttu-id="95267-103">Кбасепропертипаже. OnDeactivate, метод</span><span class="sxs-lookup"><span data-stu-id="95267-103">CBasePropertyPage.OnDeactivate method</span></span>

<span data-ttu-id="95267-104">`OnDeactivate`Метод вызывается при уничтожении окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="95267-104">The `OnDeactivate` method is called when the dialog box window is destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="95267-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95267-105">Syntax</span></span>


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a><span data-ttu-id="95267-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95267-106">Parameters</span></span>

<span data-ttu-id="95267-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="95267-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95267-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95267-108">Return value</span></span>

<span data-ttu-id="95267-109">Реализация базового класса возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="95267-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="95267-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95267-110">Remarks</span></span>

<span data-ttu-id="95267-111">Метод [**кбасепропертипаже::D еактивате**](cbasepropertypage-deactivate.md) вызывает `OnDeactivate` метод.</span><span class="sxs-lookup"><span data-stu-id="95267-111">The [**CBasePropertyPage::Deactivate**](cbasepropertypage-deactivate.md) method calls the `OnDeactivate` method.</span></span> <span data-ttu-id="95267-112">Переопределите, `OnDeactivate` чтобы освободить все ресурсы, полученные производным классом в методе [**кбасепропертипаже:: OnActivate**](cbasepropertypage-onactivate.md) , или для выполнения других задач по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="95267-112">Override `OnDeactivate` to release any resources that the derived class obtained in the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, or to perform other tasks as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="95267-113">Требования</span><span class="sxs-lookup"><span data-stu-id="95267-113">Requirements</span></span>



| <span data-ttu-id="95267-114">Требование</span><span class="sxs-lookup"><span data-stu-id="95267-114">Requirement</span></span> | <span data-ttu-id="95267-115">Значение</span><span class="sxs-lookup"><span data-stu-id="95267-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95267-116">Header</span><span class="sxs-lookup"><span data-stu-id="95267-116">Header</span></span><br/>  | <dl> <span data-ttu-id="95267-117"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95267-117"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="95267-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95267-118">Library</span></span><br/> | <dl> <span data-ttu-id="95267-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="95267-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95267-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95267-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95267-121">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="95267-121">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




