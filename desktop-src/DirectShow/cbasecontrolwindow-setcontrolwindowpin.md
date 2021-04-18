---
description: Метод Сетконтролвиндовпин задает ПИН-код для синхронизации.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Кбасеконтролвиндов. Сетконтролвиндовпин, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658059"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a><span data-ttu-id="eaf20-103">Кбасеконтролвиндов. Сетконтролвиндовпин, метод</span><span class="sxs-lookup"><span data-stu-id="eaf20-103">CBaseControlWindow.SetControlWindowPin method</span></span>

<span data-ttu-id="eaf20-104">`SetControlWindowPin`Метод задает ПИН-код для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="eaf20-104">The `SetControlWindowPin` method sets the pin with which to synchronize.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eaf20-105">Syntax</span></span>


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="eaf20-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eaf20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf20-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="eaf20-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="eaf20-108">Указатель на ПИН-код, с которым синхронизируется интерфейс.</span><span class="sxs-lookup"><span data-stu-id="eaf20-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf20-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eaf20-109">Return value</span></span>

<span data-ttu-id="eaf20-110">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="eaf20-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaf20-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eaf20-111">Remarks</span></span>

<span data-ttu-id="eaf20-112">Эта функция члена задает \_ переменную члена m ппин, равную параметру ппин.</span><span class="sxs-lookup"><span data-stu-id="eaf20-112">This member function sets the m\_pPin member variable equal to the pPin parameter.</span></span> <span data-ttu-id="eaf20-113">Как описано в конструкторе, интерфейс можно вызывать только после успешного подключения фильтра.</span><span class="sxs-lookup"><span data-stu-id="eaf20-113">As described in the constructor, the interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="eaf20-114">Объект передается через эту функцию-член в закрепление, с которым она должна быть синхронизирована; в большинстве случаев он определяет, подключен ли ПИН-код каждый раз, когда он имеет метод интерфейса, и \_ при сбое ВОЗВРАЩАЕТ VFW E \_ Not \_ Connected.</span><span class="sxs-lookup"><span data-stu-id="eaf20-114">The object is passed in through this member function to the pin with which it should synchronize; in most cases, it will determine if the pin is connected whenever it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf20-115">Требования</span><span class="sxs-lookup"><span data-stu-id="eaf20-115">Requirements</span></span>



| <span data-ttu-id="eaf20-116">Требование</span><span class="sxs-lookup"><span data-stu-id="eaf20-116">Requirement</span></span> | <span data-ttu-id="eaf20-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eaf20-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf20-118">Header</span><span class="sxs-lookup"><span data-stu-id="eaf20-118">Header</span></span><br/>  | <dl> <span data-ttu-id="eaf20-119"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eaf20-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eaf20-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eaf20-120">Library</span></span><br/> | <dl> <span data-ttu-id="eaf20-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="eaf20-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf20-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eaf20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf20-123">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="eaf20-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




