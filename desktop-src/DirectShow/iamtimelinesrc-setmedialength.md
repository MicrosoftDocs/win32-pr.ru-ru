---
description: Метод Сетмедиаленгс задает длительность исходного файла.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'Метод Иамтимелинесрк:: Сетмедиаленгс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689359"
---
# <a name="iamtimelinesrcsetmedialength-method"></a><span data-ttu-id="3e870-103">Метод Иамтимелинесрк:: Сетмедиаленгс</span><span class="sxs-lookup"><span data-stu-id="3e870-103">IAMTimelineSrc::SetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="3e870-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3e870-104">\[Deprecated.</span></span> <span data-ttu-id="3e870-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3e870-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3e870-106">`SetMediaLength`Метод задает длительность исходного файла.</span><span class="sxs-lookup"><span data-stu-id="3e870-106">The `SetMediaLength` method specifies the duration of the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e870-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e870-107">Syntax</span></span>


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="3e870-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e870-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e870-109">*Длина*</span><span class="sxs-lookup"><span data-stu-id="3e870-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="3e870-110">Длина носителя (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="3e870-110">Media length, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e870-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e870-111">Return value</span></span>

<span data-ttu-id="3e870-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3e870-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3e870-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3e870-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e870-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e870-114">Remarks</span></span>

<span data-ttu-id="3e870-115">Можно избежать потенциальных ошибок отрисовки, установив длину носителя до того, как будет задано время окончания носителя.</span><span class="sxs-lookup"><span data-stu-id="3e870-115">You can avoid potential rendering errors by setting the media length before you set the media stop time.</span></span> <span data-ttu-id="3e870-116">При задании времени окончания передачи данных DES проверяет его на соответствие длине носителя.</span><span class="sxs-lookup"><span data-stu-id="3e870-116">When you set the media stop time, DES checks it against the media length.</span></span>

<span data-ttu-id="3e870-117">Этот метод не проверяет параметр *длины* , но значение должно равняться фактической длительности исходного файла.</span><span class="sxs-lookup"><span data-stu-id="3e870-117">This method does not validate the *Length* parameter, but the value must equal the actual duration of the source file.</span></span> <span data-ttu-id="3e870-118">Получите длительность исходного файла, вызвав [**имедиадет:: Get \_ стреамленгс**](imediadet-get-streamlength.md).</span><span class="sxs-lookup"><span data-stu-id="3e870-118">Obtain the source file duration by calling [**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md).</span></span>

> [!Note]  
> <span data-ttu-id="3e870-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="3e870-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3e870-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3e870-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3e870-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3e870-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e870-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3e870-122">Requirements</span></span>



| <span data-ttu-id="3e870-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3e870-123">Requirement</span></span> | <span data-ttu-id="3e870-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3e870-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e870-125">Header</span><span class="sxs-lookup"><span data-stu-id="3e870-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3e870-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e870-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3e870-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e870-127">Library</span></span><br/> | <dl> <span data-ttu-id="3e870-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e870-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e870-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e870-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e870-130">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="3e870-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="3e870-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="3e870-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




