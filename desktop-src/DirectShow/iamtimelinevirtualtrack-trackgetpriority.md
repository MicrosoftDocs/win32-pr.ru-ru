---
description: Метод Траккжетприорити извлекает уровень приоритета объекта.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'Метод Иамтимелиневиртуалтракк:: Траккжетприорити (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689280"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a><span data-ttu-id="9e35d-103">Метод Иамтимелиневиртуалтракк:: Траккжетприорити</span><span class="sxs-lookup"><span data-stu-id="9e35d-103">IAMTimelineVirtualTrack::TrackGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="9e35d-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9e35d-104">\[Deprecated.</span></span> <span data-ttu-id="9e35d-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e35d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9e35d-106">`TrackGetPriority`Метод получает уровень приоритета объекта.</span><span class="sxs-lookup"><span data-stu-id="9e35d-106">The `TrackGetPriority` method retrieves the object's priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e35d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e35d-107">Syntax</span></span>


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="9e35d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e35d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e35d-109">*пприорити*</span><span class="sxs-lookup"><span data-stu-id="9e35d-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="9e35d-110">Указатель на переменную, которая получает уровень приоритета.</span><span class="sxs-lookup"><span data-stu-id="9e35d-110">Pointer to a variable that receives the priority level.</span></span> <span data-ttu-id="9e35d-111">Если объект не является частью временной шкалы, для него устанавливается значение – 1.</span><span class="sxs-lookup"><span data-stu-id="9e35d-111">If the object is not part of a timeline, the value is set to –1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e35d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e35d-112">Return value</span></span>

<span data-ttu-id="9e35d-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e35d-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e35d-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e35d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e35d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e35d-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9e35d-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="9e35d-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e35d-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e35d-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9e35d-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9e35d-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e35d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9e35d-119">Requirements</span></span>



| <span data-ttu-id="9e35d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9e35d-120">Requirement</span></span> | <span data-ttu-id="9e35d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9e35d-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e35d-122">Header</span><span class="sxs-lookup"><span data-stu-id="9e35d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9e35d-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e35d-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9e35d-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9e35d-124">Library</span></span><br/> | <dl> <span data-ttu-id="9e35d-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e35d-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e35d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e35d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e35d-127">**Интерфейс Иамтимелиневиртуалтракк**</span><span class="sxs-lookup"><span data-stu-id="9e35d-127">**IAMTimelineVirtualTrack Interface**</span></span>](iamtimelinevirtualtrack.md)
</dt> <dt>

[<span data-ttu-id="9e35d-128">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="9e35d-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




