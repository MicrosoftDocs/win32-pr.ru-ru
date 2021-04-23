---
description: Метод Зеробетвин удаляет все данные из трассировки в указанное время. Этот метод разделяет все объекты, охватывающие указанный диапазон времени, и удаляет части, попадающие в диапазон.
ms.assetid: df173a3c-147b-4f2d-9bcb-a8c2873f5420
title: 'Метод Иамтимелинетракк:: Зеробетвин (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bef669bae5e5e5c4c31a49b545fcfc7f58285f97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685227"
---
# <a name="iamtimelinetrackzerobetween-method"></a><span data-ttu-id="fd196-104">Метод Иамтимелинетракк:: Зеробетвин</span><span class="sxs-lookup"><span data-stu-id="fd196-104">IAMTimelineTrack::ZeroBetween method</span></span>

> [!Note]  
> <span data-ttu-id="fd196-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="fd196-105">\[Deprecated.</span></span> <span data-ttu-id="fd196-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fd196-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fd196-107">`ZeroBetween`Метод удаляет все данные из трассировки в указанное время.</span><span class="sxs-lookup"><span data-stu-id="fd196-107">The `ZeroBetween` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="fd196-108">Этот метод разделяет все объекты, охватывающие указанный диапазон времени, и удаляет части, попадающие в диапазон.</span><span class="sxs-lookup"><span data-stu-id="fd196-108">This method splits any objects that span the specified time range and removes the pieces that fall within the range.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd196-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd196-109">Syntax</span></span>


```C++
HRESULT ZeroBetween(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="fd196-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd196-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd196-111">*ртстарт*</span><span class="sxs-lookup"><span data-stu-id="fd196-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="fd196-112">Начало диапазона для очистки, в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="fd196-112">Beginning of the range to clear, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="fd196-113">*ртенд*</span><span class="sxs-lookup"><span data-stu-id="fd196-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="fd196-114">Конец диапазона, который необходимо очистить, в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="fd196-114">End of the range to clear, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd196-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd196-115">Return value</span></span>

<span data-ttu-id="fd196-116">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd196-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fd196-117">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="fd196-117">Possible values include the following.</span></span>



| <span data-ttu-id="fd196-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fd196-118">Return code</span></span>                                                                             | <span data-ttu-id="fd196-119">Описание</span><span class="sxs-lookup"><span data-stu-id="fd196-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fd196-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="fd196-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="fd196-121">Диапазон времени превышает все, что находится в дорожке.</span><span class="sxs-lookup"><span data-stu-id="fd196-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="fd196-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fd196-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="fd196-123">Успешно.</span><span class="sxs-lookup"><span data-stu-id="fd196-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="fd196-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd196-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd196-125">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="fd196-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fd196-126">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fd196-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fd196-127">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fd196-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd196-128">Требования</span><span class="sxs-lookup"><span data-stu-id="fd196-128">Requirements</span></span>



| <span data-ttu-id="fd196-129">Требование</span><span class="sxs-lookup"><span data-stu-id="fd196-129">Requirement</span></span> | <span data-ttu-id="fd196-130">Значение</span><span class="sxs-lookup"><span data-stu-id="fd196-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd196-131">Header</span><span class="sxs-lookup"><span data-stu-id="fd196-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fd196-132"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd196-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fd196-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd196-133">Library</span></span><br/> | <dl> <span data-ttu-id="fd196-134"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd196-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd196-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd196-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd196-136">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="fd196-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="fd196-137">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="fd196-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




