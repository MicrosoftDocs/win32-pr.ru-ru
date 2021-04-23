---
description: Метод Транситионсенаблед определяет, включены ли переходы.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'Метод Иамтимелине:: Транситионсенаблед (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689039"
---
# <a name="iamtimelinetransitionsenabled-method"></a><span data-ttu-id="cb337-103">Метод Иамтимелине:: Транситионсенаблед</span><span class="sxs-lookup"><span data-stu-id="cb337-103">IAMTimeline::TransitionsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="cb337-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cb337-104">\[Deprecated.</span></span> <span data-ttu-id="cb337-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cb337-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cb337-106">Метод **транситионсенаблед** определяет, включены ли переходы.</span><span class="sxs-lookup"><span data-stu-id="cb337-106">The **TransitionsEnabled** method determines whether transitions are enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb337-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb337-107">Syntax</span></span>


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="cb337-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb337-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb337-109">*пфенаблед*</span><span class="sxs-lookup"><span data-stu-id="cb337-109">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="cb337-110">Получает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="cb337-110">Receives a Boolean value.</span></span> <span data-ttu-id="cb337-111">Если **значение равно true**, переходы включены.</span><span class="sxs-lookup"><span data-stu-id="cb337-111">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="cb337-112">В противном случае переходы отключены.</span><span class="sxs-lookup"><span data-stu-id="cb337-112">Otherwise, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb337-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb337-113">Return value</span></span>

<span data-ttu-id="cb337-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cb337-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb337-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb337-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb337-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb337-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cb337-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="cb337-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cb337-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cb337-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cb337-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cb337-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb337-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cb337-120">Requirements</span></span>



| <span data-ttu-id="cb337-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cb337-121">Requirement</span></span> | <span data-ttu-id="cb337-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cb337-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb337-123">Header</span><span class="sxs-lookup"><span data-stu-id="cb337-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cb337-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb337-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cb337-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb337-125">Library</span></span><br/> | <dl> <span data-ttu-id="cb337-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb337-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb337-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb337-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb337-128">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="cb337-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="cb337-129">**Иамтимелине:: Енаблетранситионс**</span><span class="sxs-lookup"><span data-stu-id="cb337-129">**IAMTimeline::EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)
</dt> <dt>

[<span data-ttu-id="cb337-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="cb337-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




