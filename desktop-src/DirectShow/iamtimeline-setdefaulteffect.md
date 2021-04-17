---
description: Метод Сетдефаултеффект задает результат по умолчанию. Если механизм визуализации не может обработать результат, он подставляет результат по умолчанию.
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: 'Метод Иамтимелине:: Сетдефаултеффект (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 33e23070a7bb10dd040d08c145bfe1e0111026d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685369"
---
# <a name="iamtimelinesetdefaulteffect-method"></a><span data-ttu-id="b1b6f-104">Метод Иамтимелине:: Сетдефаултеффект</span><span class="sxs-lookup"><span data-stu-id="b1b6f-104">IAMTimeline::SetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="b1b6f-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-105">\[Deprecated.</span></span> <span data-ttu-id="b1b6f-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b1b6f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1b6f-107">`SetDefaultEffect`Метод задает результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-107">The `SetDefaultEffect` method sets the default effect.</span></span> <span data-ttu-id="b1b6f-108">Если механизм визуализации не может обработать результат, он подставляет результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b6f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1b6f-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="b1b6f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1b6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1b6f-111">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="b1b6f-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="b1b6f-112">Указатель на идентификатор GUID для действия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-112">Pointer to the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1b6f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1b6f-113">Return value</span></span>

<span data-ttu-id="b1b6f-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1b6f-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b1b6f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1b6f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1b6f-116">Remarks</span></span>

<span data-ttu-id="b1b6f-117">Если не задать действие по умолчанию или если результат, указанный в качестве значения по умолчанию, вызывает ошибку, то DES будет использовать свой собственный результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-117">If you do not set a default effect, or if the effect that you specify as a default causes an error, DES uses its own default effect.</span></span>

> [!Note]  
> <span data-ttu-id="b1b6f-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b1b6f-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1b6f-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b1b6f-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b1b6f-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1b6f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b1b6f-121">Requirements</span></span>



| <span data-ttu-id="b1b6f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b1b6f-122">Requirement</span></span> | <span data-ttu-id="b1b6f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b1b6f-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b6f-124">Header</span><span class="sxs-lookup"><span data-stu-id="b1b6f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b1b6f-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6f-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b1b6f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b1b6f-126">Library</span></span><br/> | <dl> <span data-ttu-id="b1b6f-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6f-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1b6f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1b6f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b6f-129">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="b1b6f-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="b1b6f-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="b1b6f-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




