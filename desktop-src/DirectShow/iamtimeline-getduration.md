---
description: Метод методаической длительности извлекает Длительность временной шкалы.
ms.assetid: d60269b8-597a-4ba4-932a-54b4a36e9a7a
title: Метод Иамтимелине::-Duration (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98257c40bf2072a2b8881a4744cdbe6d3a4e7df5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675381"
---
# <a name="iamtimelinegetduration-method"></a><span data-ttu-id="657b8-103">Метод Иамтимелине:: Duration</span><span class="sxs-lookup"><span data-stu-id="657b8-103">IAMTimeline::GetDuration method</span></span>

> [!Note]  
> <span data-ttu-id="657b8-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="657b8-104">\[Deprecated.</span></span> <span data-ttu-id="657b8-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="657b8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="657b8-106">`GetDuration`Метод получает Длительность временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="657b8-106">The `GetDuration` method retrieves the duration of the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="657b8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="657b8-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   REFERENCE_TIME *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="657b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="657b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="657b8-109">*пдуратион*</span><span class="sxs-lookup"><span data-stu-id="657b8-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="657b8-110">Получает длительность временной шкалы в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="657b8-110">Receives the duration of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="657b8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="657b8-111">Return value</span></span>

<span data-ttu-id="657b8-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="657b8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="657b8-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="657b8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="657b8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="657b8-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="657b8-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="657b8-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="657b8-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="657b8-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="657b8-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="657b8-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="657b8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="657b8-118">Requirements</span></span>



| <span data-ttu-id="657b8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="657b8-119">Requirement</span></span> | <span data-ttu-id="657b8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="657b8-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="657b8-121">Header</span><span class="sxs-lookup"><span data-stu-id="657b8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="657b8-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="657b8-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="657b8-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="657b8-123">Library</span></span><br/> | <dl> <span data-ttu-id="657b8-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="657b8-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="657b8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="657b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657b8-126">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="657b8-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="657b8-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="657b8-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




