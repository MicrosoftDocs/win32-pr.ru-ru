---
description: 'Метод Сетдефаулттранситионб задает переход по умолчанию. Этот метод эквивалентен Иамтимелине:: Сетдефаулттранситион, но принимает значение BSTR, а не указатель на GUID.'
ms.assetid: 1998fd31-2ab8-477e-89ee-93ca92dc10ec
title: 'Метод Иамтимелине:: Сетдефаулттранситионб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 221491dd0be97f1808e469d956c189bf61458278
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685162"
---
# <a name="iamtimelinesetdefaulttransitionb-method"></a><span data-ttu-id="35920-104">Метод Иамтимелине:: Сетдефаулттранситионб</span><span class="sxs-lookup"><span data-stu-id="35920-104">IAMTimeline::SetDefaultTransitionB method</span></span>

> [!Note]  
> <span data-ttu-id="35920-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="35920-105">\[Deprecated.</span></span> <span data-ttu-id="35920-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="35920-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="35920-107">`SetDefaultTransitionB`Метод задает переход по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35920-107">The `SetDefaultTransitionB` method sets the default transition.</span></span> <span data-ttu-id="35920-108">Этот метод эквивалентен [**иамтимелине:: сетдефаулттранситион**](iamtimeline-setdefaulttransition.md), но принимает значение BSTR, а не указатель на GUID.</span><span class="sxs-lookup"><span data-stu-id="35920-108">This method is equivalent to [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md), but takes a BSTR value, rather than a pointer to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="35920-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35920-109">Syntax</span></span>


```C++
HRESULT SetDefaultTransitionB(
   BSTR pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="35920-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="35920-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35920-111">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="35920-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="35920-112">Значение BSTR, представляющее GUID перехода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35920-112">BSTR value representing the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35920-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35920-113">Return value</span></span>

<span data-ttu-id="35920-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="35920-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="35920-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="35920-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="35920-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35920-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="35920-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="35920-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="35920-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="35920-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="35920-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="35920-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="35920-120">Требования</span><span class="sxs-lookup"><span data-stu-id="35920-120">Requirements</span></span>



| <span data-ttu-id="35920-121">Требование</span><span class="sxs-lookup"><span data-stu-id="35920-121">Requirement</span></span> | <span data-ttu-id="35920-122">Значение</span><span class="sxs-lookup"><span data-stu-id="35920-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35920-123">Header</span><span class="sxs-lookup"><span data-stu-id="35920-123">Header</span></span><br/>  | <dl> <span data-ttu-id="35920-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="35920-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="35920-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="35920-125">Library</span></span><br/> | <dl> <span data-ttu-id="35920-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35920-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35920-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35920-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35920-128">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="35920-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="35920-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="35920-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




