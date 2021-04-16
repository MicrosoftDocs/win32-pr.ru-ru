---
description: Метод Втракксвапприоритиес переключает уровни приоритета двух дорожек.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'Метод Иамтимелинекомп:: Втракксвапприоритиес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689504"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a><span data-ttu-id="d0c34-103">Метод Иамтимелинекомп:: Втракксвапприоритиес</span><span class="sxs-lookup"><span data-stu-id="d0c34-103">IAMTimelineComp::VTrackSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="d0c34-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d0c34-104">\[Deprecated.</span></span> <span data-ttu-id="d0c34-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0c34-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d0c34-106">`VTrackSwapPriorities`Метод переключает уровни приоритета двух дорожек.</span><span class="sxs-lookup"><span data-stu-id="d0c34-106">The `VTrackSwapPriorities` method switches the priority levels of two tracks.</span></span>

<span data-ttu-id="d0c34-107">При наличии двух уровней приоритета этот метод переключает Виртуальные дорожки с этими приоритетами.</span><span class="sxs-lookup"><span data-stu-id="d0c34-107">Given two priority levels, this method switches the virtual tracks at those priorities.</span></span> <span data-ttu-id="d0c34-108">Когда метод возвращает значение, запись, которая была на первом уровне приоритета, теперь находится на втором уровне приоритета, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="d0c34-108">When the method returns, the track that was at the first priority level is now at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c34-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0c34-109">Syntax</span></span>


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a><span data-ttu-id="d0c34-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0c34-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c34-111">*виртуалтракка*</span><span class="sxs-lookup"><span data-stu-id="d0c34-111">*VirtualTrackA*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c34-112">Первый уровень приоритета для переключения виртуальных дорожек.</span><span class="sxs-lookup"><span data-stu-id="d0c34-112">First priority level at which to swap virtual tracks.</span></span>

</dd> <dt>

<span data-ttu-id="d0c34-113">*виртуалтраккб*</span><span class="sxs-lookup"><span data-stu-id="d0c34-113">*VirtualTrackB*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c34-114">Второй уровень приоритета для переключения виртуальных дорожек.</span><span class="sxs-lookup"><span data-stu-id="d0c34-114">Second priority level at which to swap virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c34-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0c34-115">Return value</span></span>

<span data-ttu-id="d0c34-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d0c34-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d0c34-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0c34-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0c34-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0c34-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d0c34-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d0c34-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d0c34-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d0c34-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d0c34-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d0c34-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0c34-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d0c34-122">Requirements</span></span>



| <span data-ttu-id="d0c34-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d0c34-123">Requirement</span></span> | <span data-ttu-id="d0c34-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d0c34-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c34-125">Header</span><span class="sxs-lookup"><span data-stu-id="d0c34-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d0c34-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c34-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d0c34-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d0c34-127">Library</span></span><br/> | <dl> <span data-ttu-id="d0c34-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0c34-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c34-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0c34-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c34-130">**Интерфейс Иамтимелинекомп**</span><span class="sxs-lookup"><span data-stu-id="d0c34-130">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="d0c34-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="d0c34-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




