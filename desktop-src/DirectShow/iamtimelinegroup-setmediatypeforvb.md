---
description: Метод Сетмедиатипефорвб задает тип носителя группы для клиентов автоматизации.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'Метод Иамтимелинеграуп:: Сетмедиатипефорвб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1371b1d6c906666ca30e5df2d26dbe20eddf1745
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689214"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a><span data-ttu-id="0e89f-103">Метод Иамтимелинеграуп:: Сетмедиатипефорвб</span><span class="sxs-lookup"><span data-stu-id="0e89f-103">IAMTimelineGroup::SetMediaTypeForVB method</span></span>

> [!Note]  
> <span data-ttu-id="0e89f-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0e89f-104">\[Deprecated.</span></span> <span data-ttu-id="0e89f-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0e89f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0e89f-106">`SetMediaTypeForVB`Метод задает тип носителя группы для клиентов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="0e89f-106">The `SetMediaTypeForVB` method specifies the group media type, for Automation clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e89f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e89f-107">Syntax</span></span>


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a><span data-ttu-id="0e89f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e89f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e89f-109">*Val* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e89f-109">*Val* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e89f-110">Значение, указывающее тип носителя.</span><span class="sxs-lookup"><span data-stu-id="0e89f-110">Value that specifies the media type.</span></span> <span data-ttu-id="0e89f-111">Установите значение 0 для параметра видео или 1 для звукового сигнала.</span><span class="sxs-lookup"><span data-stu-id="0e89f-111">Set the value to 0 for video, or 1 for audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e89f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e89f-112">Return value</span></span>

<span data-ttu-id="0e89f-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0e89f-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e89f-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0e89f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e89f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e89f-115">Remarks</span></span>

<span data-ttu-id="0e89f-116">Этот метод предназначен для клиентов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="0e89f-116">This method is intended for Automation clients.</span></span> <span data-ttu-id="0e89f-117">Для приложений C++ используйте метод [**иамтимелинеграуп:: сетмедиатипе**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="0e89f-117">For C++ applications, use the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="0e89f-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="0e89f-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e89f-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0e89f-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0e89f-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0e89f-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e89f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0e89f-121">Requirements</span></span>



| <span data-ttu-id="0e89f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0e89f-122">Requirement</span></span> | <span data-ttu-id="0e89f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0e89f-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e89f-124">Header</span><span class="sxs-lookup"><span data-stu-id="0e89f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0e89f-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e89f-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0e89f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e89f-126">Library</span></span><br/> | <dl> <span data-ttu-id="0e89f-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e89f-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e89f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e89f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e89f-129">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="0e89f-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="0e89f-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="0e89f-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




