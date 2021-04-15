---
description: Метод GetDuration2 извлекает Длительность временной шкалы. Этот метод эквивалентен Иамтимелине::-Duration, но принимает параметр типа Double.
ms.assetid: 49f5eed3-7fab-4f08-b65c-300349b197cb
title: 'Метод Иамтимелине:: GetDuration2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc840e642f6c08825f6f53869229e9cc27e87b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651995"
---
# <a name="iamtimelinegetduration2-method"></a><span data-ttu-id="1d92d-104">Метод Иамтимелине:: GetDuration2</span><span class="sxs-lookup"><span data-stu-id="1d92d-104">IAMTimeline::GetDuration2 method</span></span>

> [!Note]  
> <span data-ttu-id="1d92d-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1d92d-105">\[Deprecated.</span></span> <span data-ttu-id="1d92d-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1d92d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1d92d-107">`GetDuration2`Метод получает Длительность временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="1d92d-107">The `GetDuration2` method retrieves the duration of the timeline.</span></span> <span data-ttu-id="1d92d-108">Этот метод эквивалентен [**иамтимелине::-Duration**](iamtimeline-getduration.md), но принимает параметр типа **Double**.</span><span class="sxs-lookup"><span data-stu-id="1d92d-108">This method is equivalent to [**IAMTimeline::GetDuration**](iamtimeline-getduration.md), but takes a parameter of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d92d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d92d-109">Syntax</span></span>


```C++
HRESULT GetDuration2(
   double *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="1d92d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d92d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d92d-111">*пдуратион*</span><span class="sxs-lookup"><span data-stu-id="1d92d-111">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="1d92d-112">Получает длительность временной шкалы в долях секунды.</span><span class="sxs-lookup"><span data-stu-id="1d92d-112">Receives the duration of the timeline, in fractional seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d92d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d92d-113">Return value</span></span>

<span data-ttu-id="1d92d-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d92d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d92d-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d92d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d92d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d92d-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d92d-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="1d92d-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1d92d-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1d92d-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1d92d-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1d92d-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d92d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1d92d-120">Requirements</span></span>



| <span data-ttu-id="1d92d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1d92d-121">Requirement</span></span> | <span data-ttu-id="1d92d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1d92d-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d92d-123">Header</span><span class="sxs-lookup"><span data-stu-id="1d92d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1d92d-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d92d-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1d92d-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d92d-125">Library</span></span><br/> | <dl> <span data-ttu-id="1d92d-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d92d-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d92d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d92d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d92d-128">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="1d92d-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="1d92d-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="1d92d-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




