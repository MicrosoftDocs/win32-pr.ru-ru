---
description: 'Метод GetNextSrc2 ищет в дорожке следующий источник, который отображается в указанное время или позже. Этот метод эквивалентен Иамтимелинетракк:: Жетнекстсрк, но принимает значение РЕФТИМЕ.'
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'Метод Иамтимелинетракк:: GetNextSrc2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685242"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a><span data-ttu-id="cbb30-104">Метод Иамтимелинетракк:: GetNextSrc2</span><span class="sxs-lookup"><span data-stu-id="cbb30-104">IAMTimelineTrack::GetNextSrc2 method</span></span>

> [!Note]  
> <span data-ttu-id="cbb30-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cbb30-105">\[Deprecated.</span></span> <span data-ttu-id="cbb30-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cbb30-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cbb30-107">`GetNextSrc2`Метод выполняет поиск следующего источника, который отображается в указанном времени или более поздней версии, в дорожке.</span><span class="sxs-lookup"><span data-stu-id="cbb30-107">The `GetNextSrc2` method searches the track for the next source that appears at the specified time or later.</span></span> <span data-ttu-id="cbb30-108">Этот метод эквивалентен [**иамтимелинетракк:: жетнекстсрк**](iamtimelinetrack-getnextsrc.md), но принимает значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="cbb30-108">This method is equivalent to [**IAMTimelineTrack::GetNextSrc**](iamtimelinetrack-getnextsrc.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb30-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbb30-109">Syntax</span></span>


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="cbb30-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbb30-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbb30-111">*ппсрк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cbb30-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb30-112">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="cbb30-112">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cbb30-113">*\Sub*</span><span class="sxs-lookup"><span data-stu-id="cbb30-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb30-114">В поле входные данные содержит время начала поиска в секундах.</span><span class="sxs-lookup"><span data-stu-id="cbb30-114">On input, contains the start time for the search, in seconds.</span></span> <span data-ttu-id="cbb30-115">Если метод получает источник, ему присваивается значение времени окончания источника.</span><span class="sxs-lookup"><span data-stu-id="cbb30-115">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="cbb30-116">Если метод не получает источник, значение станет недопустимым и приложение не должно его использовать.</span><span class="sxs-lookup"><span data-stu-id="cbb30-116">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbb30-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbb30-117">Return value</span></span>

<span data-ttu-id="cbb30-118">Возвращает \_ значение ОК, если метод получает источник, или \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cbb30-118">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbb30-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbb30-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cbb30-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="cbb30-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cbb30-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cbb30-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cbb30-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cbb30-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cbb30-123">Требования</span><span class="sxs-lookup"><span data-stu-id="cbb30-123">Requirements</span></span>



| <span data-ttu-id="cbb30-124">Требование</span><span class="sxs-lookup"><span data-stu-id="cbb30-124">Requirement</span></span> | <span data-ttu-id="cbb30-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cbb30-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb30-126">Header</span><span class="sxs-lookup"><span data-stu-id="cbb30-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cbb30-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbb30-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cbb30-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbb30-128">Library</span></span><br/> | <dl> <span data-ttu-id="cbb30-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbb30-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbb30-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbb30-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb30-131">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="cbb30-131">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="cbb30-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="cbb30-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




