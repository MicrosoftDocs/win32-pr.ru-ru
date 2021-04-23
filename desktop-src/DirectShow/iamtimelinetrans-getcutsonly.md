---
description: Метод Жеткутсонли определяет, визуализируется ли переход в виде вырезания. Если да, то переход выполняется мгновенно в вырезанной точке.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'Метод Иамтимелинетранс:: Жеткутсонли (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689447"
---
# <a name="iamtimelinetransgetcutsonly-method"></a><span data-ttu-id="62562-104">Метод Иамтимелинетранс:: Жеткутсонли</span><span class="sxs-lookup"><span data-stu-id="62562-104">IAMTimelineTrans::GetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="62562-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="62562-105">\[Deprecated.</span></span> <span data-ttu-id="62562-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62562-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="62562-107">`GetCutsOnly`Метод определяет, визуализируется ли переход в виде вырезания.</span><span class="sxs-lookup"><span data-stu-id="62562-107">The `GetCutsOnly` method determines whether the transition is rendered as a cut.</span></span> <span data-ttu-id="62562-108">Если да, то переход выполняется мгновенно в вырезанной точке.</span><span class="sxs-lookup"><span data-stu-id="62562-108">If so, the transition occurs instantaneously at the cut point.</span></span>

## <a name="syntax"></a><span data-ttu-id="62562-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62562-109">Syntax</span></span>


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="62562-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="62562-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62562-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="62562-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="62562-112">Получает логическое значение, указывающее, визуализируется ли переход в виде вырезания.</span><span class="sxs-lookup"><span data-stu-id="62562-112">Receives a Boolean value specifying whether the transition is rendered as a cut.</span></span> <span data-ttu-id="62562-113">Если **значение равно true**, то переход является мгновенно вырезанным.</span><span class="sxs-lookup"><span data-stu-id="62562-113">If **TRUE**, the transition is an instantaneous cut.</span></span> <span data-ttu-id="62562-114">Если **значение равно false**, переход выполняется в течение нормальной длительности.</span><span class="sxs-lookup"><span data-stu-id="62562-114">If **FALSE**, the transition occurs over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62562-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62562-115">Return value</span></span>

<span data-ttu-id="62562-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="62562-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62562-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62562-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62562-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62562-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="62562-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="62562-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="62562-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="62562-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="62562-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="62562-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62562-122">Требования</span><span class="sxs-lookup"><span data-stu-id="62562-122">Requirements</span></span>



| <span data-ttu-id="62562-123">Требование</span><span class="sxs-lookup"><span data-stu-id="62562-123">Requirement</span></span> | <span data-ttu-id="62562-124">Значение</span><span class="sxs-lookup"><span data-stu-id="62562-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62562-125">Header</span><span class="sxs-lookup"><span data-stu-id="62562-125">Header</span></span><br/>  | <dl> <span data-ttu-id="62562-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="62562-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="62562-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="62562-127">Library</span></span><br/> | <dl> <span data-ttu-id="62562-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62562-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62562-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62562-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62562-130">**Интерфейс Иамтимелинетранс**</span><span class="sxs-lookup"><span data-stu-id="62562-130">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="62562-131">**Иамтимелинетранс:: Сеткутсонли**</span><span class="sxs-lookup"><span data-stu-id="62562-131">**IAMTimelineTrans::SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[<span data-ttu-id="62562-132">**Иамтимелинетранс:: Жеткутпоинт**</span><span class="sxs-lookup"><span data-stu-id="62562-132">**IAMTimelineTrans::GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[<span data-ttu-id="62562-133">**Иамтимелине:: Транситионсенаблед**</span><span class="sxs-lookup"><span data-stu-id="62562-133">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="62562-134">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="62562-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




