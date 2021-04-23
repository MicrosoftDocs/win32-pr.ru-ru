---
description: Метод конструктора.
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
ms.openlocfilehash: dea0548079f8eb703f0c17557cab6a5e634cf242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688774"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="cf757-103">Кбасеконтролвидео. Кбасеконтролвидео, конструктор</span><span class="sxs-lookup"><span data-stu-id="cf757-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="cf757-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="cf757-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf757-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf757-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="cf757-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf757-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf757-107">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="cf757-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="cf757-108">Указатель на объект фильтра мультимедиа-владельца.</span><span class="sxs-lookup"><span data-stu-id="cf757-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="cf757-109">*пинтерфацелокк*</span><span class="sxs-lookup"><span data-stu-id="cf757-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="cf757-110">Указатель на критическую секцию, используемую для блокировки.</span><span class="sxs-lookup"><span data-stu-id="cf757-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="cf757-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="cf757-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cf757-112">Указатель на описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cf757-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="cf757-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="cf757-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="cf757-114">Указатель на управляющий интерфейс **IUnknown** , если объект является частью статистической функции; в противном случае **значение должно быть равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="cf757-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cf757-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="cf757-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cf757-116">Указатель на переменную, которая получает значение HRESULT, указывающее на успешность или ошибку метода конструктора.</span><span class="sxs-lookup"><span data-stu-id="cf757-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf757-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf757-117">Remarks</span></span>

<span data-ttu-id="cf757-118">Объект реализует интерфейс элемента управления [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="cf757-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="cf757-119">Для всех методов интерфейса из [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) , реализуемых этим классом, требуется, чтобы фильтр был правильно подключен.</span><span class="sxs-lookup"><span data-stu-id="cf757-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="cf757-120">По этой причине классу передается ПИН-код, с которым он должен синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="cf757-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="cf757-121">При вызове метода интерфейса объект определяет, что ПИН-код все еще подключен.</span><span class="sxs-lookup"><span data-stu-id="cf757-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf757-122">Требования</span><span class="sxs-lookup"><span data-stu-id="cf757-122">Requirements</span></span>



| <span data-ttu-id="cf757-123">Требование</span><span class="sxs-lookup"><span data-stu-id="cf757-123">Requirement</span></span> | <span data-ttu-id="cf757-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cf757-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf757-125">Header</span><span class="sxs-lookup"><span data-stu-id="cf757-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cf757-126"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf757-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cf757-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf757-127">Library</span></span><br/> | <dl> <span data-ttu-id="cf757-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cf757-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf757-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf757-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf757-130">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="cf757-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




