---
description: Метод Жетсвапинпутс извлекает значение, указывающее, меняются ли входные данные перехода.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'Метод Иамтимелинетранс:: Жетсвапинпутс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689446"
---
# <a name="iamtimelinetransgetswapinputs-method"></a><span data-ttu-id="044d5-103">Метод Иамтимелинетранс:: Жетсвапинпутс</span><span class="sxs-lookup"><span data-stu-id="044d5-103">IAMTimelineTrans::GetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="044d5-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="044d5-104">\[Deprecated.</span></span> <span data-ttu-id="044d5-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="044d5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="044d5-106">`GetSwapInputs`Метод получает значение, указывающее, меняются ли входные данные перехода.</span><span class="sxs-lookup"><span data-stu-id="044d5-106">The `GetSwapInputs` method retrieves a value that indicates whether the transition inputs are swapped.</span></span>

<span data-ttu-id="044d5-107">По умолчанию переход проходит от состава всех слоев с низким приоритетом до слоя, в котором находится переход.</span><span class="sxs-lookup"><span data-stu-id="044d5-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="044d5-108">Эту прогрессию можно отменить, чтобы переход выполнялся с слоя, где он находится в составе слоев с более низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="044d5-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span>

## <a name="syntax"></a><span data-ttu-id="044d5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="044d5-109">Syntax</span></span>


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="044d5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="044d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044d5-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="044d5-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="044d5-112">Получает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="044d5-112">Receives a Boolean value.</span></span> <span data-ttu-id="044d5-113">Если значение равно **false**, переход проходит от составного набора всех уровней с низким приоритетом до слоя перехода.</span><span class="sxs-lookup"><span data-stu-id="044d5-113">If the value is **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="044d5-114">Если значение равно **true**, переход проходит в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="044d5-114">If the value is **TRUE**, the transition goes in the opposite direction.</span></span> <span data-ttu-id="044d5-115">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="044d5-115">The default value is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="044d5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="044d5-116">Return value</span></span>

<span data-ttu-id="044d5-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="044d5-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="044d5-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="044d5-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="044d5-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="044d5-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="044d5-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="044d5-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="044d5-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="044d5-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="044d5-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="044d5-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="044d5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="044d5-123">Requirements</span></span>



| <span data-ttu-id="044d5-124">Требование</span><span class="sxs-lookup"><span data-stu-id="044d5-124">Requirement</span></span> | <span data-ttu-id="044d5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="044d5-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="044d5-126">Header</span><span class="sxs-lookup"><span data-stu-id="044d5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="044d5-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="044d5-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="044d5-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="044d5-128">Library</span></span><br/> | <dl> <span data-ttu-id="044d5-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="044d5-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="044d5-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="044d5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044d5-131">**Интерфейс Иамтимелинетранс**</span><span class="sxs-lookup"><span data-stu-id="044d5-131">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="044d5-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="044d5-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




