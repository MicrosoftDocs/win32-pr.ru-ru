---
description: Метод Иснормалрате указывает, будет ли воспроизводиться воспроизведение клипа с нормальным темпом воспроизведения; то есть скорость воспроизведения исходного файла.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'Метод Иамтимелинесрк:: Иснормалрате (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689361"
---
# <a name="iamtimelinesrcisnormalrate-method"></a><span data-ttu-id="43c6c-103">Метод Иамтимелинесрк:: Иснормалрате</span><span class="sxs-lookup"><span data-stu-id="43c6c-103">IAMTimelineSrc::IsNormalRate method</span></span>

> [!Note]  
> <span data-ttu-id="43c6c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="43c6c-104">\[Deprecated.</span></span> <span data-ttu-id="43c6c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="43c6c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="43c6c-106">`IsNormalRate`Метод указывает, будет ли воспроизведение клипа воспроизводиться с нормальным темпом воспроизведения, то есть от скорости воспроизведения исходного файла.</span><span class="sxs-lookup"><span data-stu-id="43c6c-106">The `IsNormalRate` method indicates whether the clip will play at the normal playback rate; that is, the playback rate of the original file.</span></span>

## <a name="syntax"></a><span data-ttu-id="43c6c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43c6c-107">Syntax</span></span>


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="43c6c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="43c6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c6c-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="43c6c-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="43c6c-110">Получает логическое значение, указывающее, как будет отображаться клип.</span><span class="sxs-lookup"><span data-stu-id="43c6c-110">Receives a Boolean value indicating how the clip will render.</span></span> <span data-ttu-id="43c6c-111">Если значение равно **true**, клип будет воспроизводиться по нормальной ставке.</span><span class="sxs-lookup"><span data-stu-id="43c6c-111">If the value is **TRUE**, the clip will play at the normal rate.</span></span> <span data-ttu-id="43c6c-112">В противном случае он будет воспроизводиться быстрее или медленнее, чем обычная.</span><span class="sxs-lookup"><span data-stu-id="43c6c-112">Otherwise, it will play faster or slower than normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c6c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43c6c-113">Return value</span></span>

<span data-ttu-id="43c6c-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="43c6c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43c6c-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43c6c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43c6c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43c6c-116">Remarks</span></span>

<span data-ttu-id="43c6c-117">Скорость воспроизведения клипа определяется временем его начала и окончания, относительно времени его выполнения:</span><span class="sxs-lookup"><span data-stu-id="43c6c-117">A clip's playback rate is determined by its media start and stop times, relative to its timeline times:</span></span>


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



<span data-ttu-id="43c6c-118">Если это соотношение равно 1, клип воспроизводится с созданной скоростью.</span><span class="sxs-lookup"><span data-stu-id="43c6c-118">If this ratio is equal to 1, the clip plays at the authored speed.</span></span> <span data-ttu-id="43c6c-119">В противном случае он будет воспроизводиться быстрее или медленнее.</span><span class="sxs-lookup"><span data-stu-id="43c6c-119">Otherwise, it plays faster or slower.</span></span> <span data-ttu-id="43c6c-120">Дополнительные сведения см. [в разделе время в службах редактирования DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="43c6c-120">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="43c6c-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="43c6c-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="43c6c-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="43c6c-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="43c6c-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="43c6c-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43c6c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="43c6c-124">Requirements</span></span>



| <span data-ttu-id="43c6c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="43c6c-125">Requirement</span></span> | <span data-ttu-id="43c6c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="43c6c-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43c6c-127">Header</span><span class="sxs-lookup"><span data-stu-id="43c6c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="43c6c-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="43c6c-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="43c6c-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43c6c-129">Library</span></span><br/> | <dl> <span data-ttu-id="43c6c-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43c6c-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43c6c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43c6c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c6c-132">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="43c6c-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="43c6c-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="43c6c-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




