---
description: Метод Жетнекстсрк ищет в дорожке следующий источник, который отображается в указанное время или позже.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'Метод Иамтимелинетракк:: Жетнекстсрк (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674958"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a><span data-ttu-id="f3dee-103">Метод Иамтимелинетракк:: Жетнекстсрк</span><span class="sxs-lookup"><span data-stu-id="f3dee-103">IAMTimelineTrack::GetNextSrc method</span></span>

> [!Note]  
> <span data-ttu-id="f3dee-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f3dee-104">\[Deprecated.</span></span> <span data-ttu-id="f3dee-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3dee-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f3dee-106">`GetNextSrc`Метод выполняет поиск следующего источника, который отображается в указанном времени или более поздней версии, в дорожке.</span><span class="sxs-lookup"><span data-stu-id="f3dee-106">The `GetNextSrc` method searches the track for the next source that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3dee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3dee-107">Syntax</span></span>


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="f3dee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3dee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3dee-109">*ппсрк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f3dee-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3dee-110">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="f3dee-110">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f3dee-111">*\Sub*</span><span class="sxs-lookup"><span data-stu-id="f3dee-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="f3dee-112">Указатель на переменную, которая содержит время начала поиска в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="f3dee-112">Pointer to a variable that contains the start time for the search, in 100-nanosecond units.</span></span> <span data-ttu-id="f3dee-113">Если метод получает источник, ему присваивается значение времени окончания источника.</span><span class="sxs-lookup"><span data-stu-id="f3dee-113">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="f3dee-114">Если метод не получает источник, значение станет недопустимым и приложение не должно его использовать.</span><span class="sxs-lookup"><span data-stu-id="f3dee-114">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3dee-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3dee-115">Return value</span></span>

<span data-ttu-id="f3dee-116">Возвращает \_ значение ОК, если метод получает источник, или \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f3dee-116">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3dee-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3dee-117">Remarks</span></span>

<span data-ttu-id="f3dee-118">Если время, заданное в *схеме* координат, находится между временем начала и окончания источника, метод извлекает этот источник.</span><span class="sxs-lookup"><span data-stu-id="f3dee-118">If the time specified by *pInOut* falls between the start and stop times of a source, the method retrieves that source.</span></span>

<span data-ttu-id="f3dee-119">Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **иамтимелинеобж** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="f3dee-119">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="f3dee-120">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="f3dee-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="f3dee-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f3dee-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f3dee-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f3dee-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f3dee-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f3dee-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3dee-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f3dee-124">Requirements</span></span>



| <span data-ttu-id="f3dee-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f3dee-125">Requirement</span></span> | <span data-ttu-id="f3dee-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f3dee-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3dee-127">Header</span><span class="sxs-lookup"><span data-stu-id="f3dee-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f3dee-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3dee-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f3dee-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f3dee-129">Library</span></span><br/> | <dl> <span data-ttu-id="f3dee-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3dee-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3dee-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3dee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3dee-132">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="f3dee-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="f3dee-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f3dee-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




