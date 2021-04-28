---
description: Метод конструктора Кбасеконтролвидео. Кбасеконтролвидео.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Конструктор Кбасеконтролвидео. Кбасеконтролвидео (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096352"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="06cc3-103">Кбасеконтролвидео. Кбасеконтролвидео, конструктор</span><span class="sxs-lookup"><span data-stu-id="06cc3-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="06cc3-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="06cc3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06cc3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06cc3-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="06cc3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06cc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06cc3-107">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="06cc3-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="06cc3-108">Указатель на объект фильтра мультимедиа-владельца.</span><span class="sxs-lookup"><span data-stu-id="06cc3-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="06cc3-109">*пинтерфацелокк*</span><span class="sxs-lookup"><span data-stu-id="06cc3-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="06cc3-110">Указатель на критическую секцию, используемую для блокировки.</span><span class="sxs-lookup"><span data-stu-id="06cc3-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="06cc3-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="06cc3-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="06cc3-112">Указатель на описание объекта.</span><span class="sxs-lookup"><span data-stu-id="06cc3-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="06cc3-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="06cc3-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="06cc3-114">Указатель на управляющий интерфейс **IUnknown** , если объект является частью статистической функции; в противном случае **значение должно быть равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="06cc3-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="06cc3-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="06cc3-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="06cc3-116">Указатель на переменную, которая получает значение HRESULT, указывающее на успешность или ошибку метода конструктора.</span><span class="sxs-lookup"><span data-stu-id="06cc3-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06cc3-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="06cc3-117">Remarks</span></span>

<span data-ttu-id="06cc3-118">Объект реализует интерфейс элемента управления [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="06cc3-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="06cc3-119">Для всех методов интерфейса из [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) , реализуемых этим классом, требуется, чтобы фильтр был правильно подключен.</span><span class="sxs-lookup"><span data-stu-id="06cc3-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="06cc3-120">По этой причине классу передается ПИН-код, с которым он должен синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="06cc3-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="06cc3-121">При вызове метода интерфейса объект определяет, что ПИН-код все еще подключен.</span><span class="sxs-lookup"><span data-stu-id="06cc3-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="06cc3-122">Требования</span><span class="sxs-lookup"><span data-stu-id="06cc3-122">Requirements</span></span>



| <span data-ttu-id="06cc3-123">Требование</span><span class="sxs-lookup"><span data-stu-id="06cc3-123">Requirement</span></span> | <span data-ttu-id="06cc3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="06cc3-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06cc3-125">Header</span><span class="sxs-lookup"><span data-stu-id="06cc3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="06cc3-126"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06cc3-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06cc3-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06cc3-127">Library</span></span><br/> | <dl> <span data-ttu-id="06cc3-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="06cc3-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06cc3-129">См. также</span><span class="sxs-lookup"><span data-stu-id="06cc3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06cc3-130">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="06cc3-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




