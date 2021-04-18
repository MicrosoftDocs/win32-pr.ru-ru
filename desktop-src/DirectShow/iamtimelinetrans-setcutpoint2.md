---
description: 'Метод SetCutPoint2 задает время, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание. Этот метод эквивалентен Иамтимелинетранс:: Сеткутпоинт, но принимает значение РЕФТИМЕ.'
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'Метод Иамтимелинетранс:: SetCutPoint2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685159"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a><span data-ttu-id="5af35-104">Метод Иамтимелинетранс:: SetCutPoint2</span><span class="sxs-lookup"><span data-stu-id="5af35-104">IAMTimelineTrans::SetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="5af35-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5af35-105">\[Deprecated.</span></span> <span data-ttu-id="5af35-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5af35-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5af35-107">`SetCutPoint2`Метод задает время, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание.</span><span class="sxs-lookup"><span data-stu-id="5af35-107">The `SetCutPoint2` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="5af35-108">Этот метод эквивалентен [**иамтимелинетранс:: сеткутпоинт**](iamtimelinetrans-setcutpoint.md), но принимает значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="5af35-108">This method is equivalent to [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af35-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5af35-109">Syntax</span></span>


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="5af35-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5af35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af35-111">*тлтиме*</span><span class="sxs-lookup"><span data-stu-id="5af35-111">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="5af35-112">Вырезать точку относительно начала перехода (в секундах).</span><span class="sxs-lookup"><span data-stu-id="5af35-112">Cut point relative to the start of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af35-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5af35-113">Return value</span></span>

<span data-ttu-id="5af35-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5af35-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5af35-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5af35-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5af35-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5af35-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5af35-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="5af35-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5af35-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5af35-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5af35-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5af35-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5af35-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5af35-120">Requirements</span></span>



| <span data-ttu-id="5af35-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5af35-121">Requirement</span></span> | <span data-ttu-id="5af35-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5af35-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5af35-123">Header</span><span class="sxs-lookup"><span data-stu-id="5af35-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5af35-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5af35-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5af35-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5af35-125">Library</span></span><br/> | <dl> <span data-ttu-id="5af35-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5af35-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af35-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5af35-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af35-128">**Интерфейс Иамтимелинетранс**</span><span class="sxs-lookup"><span data-stu-id="5af35-128">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="5af35-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="5af35-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




