---
description: Метод Сеткутпоинт задает время, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'Метод Иамтимелинетранс:: Сеткутпоинт (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685427"
---
# <a name="iamtimelinetranssetcutpoint-method"></a><span data-ttu-id="53182-103">Метод Иамтимелинетранс:: Сеткутпоинт</span><span class="sxs-lookup"><span data-stu-id="53182-103">IAMTimelineTrans::SetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="53182-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="53182-104">\[Deprecated.</span></span> <span data-ttu-id="53182-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53182-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53182-106">`SetCutPoint`Метод задает время, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание.</span><span class="sxs-lookup"><span data-stu-id="53182-106">The `SetCutPoint` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span>

## <a name="syntax"></a><span data-ttu-id="53182-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53182-107">Syntax</span></span>


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="53182-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53182-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53182-109">*тлтиме*</span><span class="sxs-lookup"><span data-stu-id="53182-109">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="53182-110">Отрезать точку относительно начала перехода, в единицах с 100 нс.</span><span class="sxs-lookup"><span data-stu-id="53182-110">Cut point relative to the start of the transition, in 100-nanosecond units.</span></span> <span data-ttu-id="53182-111">Если значение выходит за границы перехода, оно усекается до ближайшего допустимого времени.</span><span class="sxs-lookup"><span data-stu-id="53182-111">If the value falls outside the bounds of the transition, it is truncated to the nearest valid time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53182-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53182-112">Return value</span></span>

<span data-ttu-id="53182-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="53182-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53182-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53182-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53182-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53182-115">Remarks</span></span>

<span data-ttu-id="53182-116">По умолчанию вырезанная точка является серединой перехода.</span><span class="sxs-lookup"><span data-stu-id="53182-116">By default, the cut-point is the middle of the transition.</span></span> <span data-ttu-id="53182-117">Например, в переходе, охватывающем одну секунду, вырезанная точка по умолчанию составляет 0,5 секунд в процессе перехода.</span><span class="sxs-lookup"><span data-stu-id="53182-117">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

> [!Note]  
> <span data-ttu-id="53182-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="53182-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="53182-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="53182-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="53182-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="53182-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53182-121">Требования</span><span class="sxs-lookup"><span data-stu-id="53182-121">Requirements</span></span>



| <span data-ttu-id="53182-122">Требование</span><span class="sxs-lookup"><span data-stu-id="53182-122">Requirement</span></span> | <span data-ttu-id="53182-123">Значение</span><span class="sxs-lookup"><span data-stu-id="53182-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53182-124">Header</span><span class="sxs-lookup"><span data-stu-id="53182-124">Header</span></span><br/>  | <dl> <span data-ttu-id="53182-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="53182-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="53182-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53182-126">Library</span></span><br/> | <dl> <span data-ttu-id="53182-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53182-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53182-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53182-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53182-129">**Интерфейс Иамтимелинетранс**</span><span class="sxs-lookup"><span data-stu-id="53182-129">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="53182-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="53182-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




