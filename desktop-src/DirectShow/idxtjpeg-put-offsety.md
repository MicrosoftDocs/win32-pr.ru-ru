---
description: '\_Метод сдвига размещения задает вертикальное смещение источника очистки.'
ms.assetid: 1dfd18cf-06ae-46eb-80d7-078efc243bb1
title: 'Идкстжпег: метод ut_OffsetY:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f68a18d01acf519032bce31c28515bc7ac81c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679761"
---
# <a name="idxtjpegput_offsety-method"></a><span data-ttu-id="f8fa5-103">Идкстжпег: \_ метод смещения:p UT</span><span class="sxs-lookup"><span data-stu-id="f8fa5-103">IDxtJpeg::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="f8fa5-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f8fa5-104">\[Deprecated.</span></span> <span data-ttu-id="f8fa5-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f8fa5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f8fa5-106">`put_OffsetY`Метод задает вертикальное смещение источника очистки.</span><span class="sxs-lookup"><span data-stu-id="f8fa5-106">The `put_OffsetY` method specifies the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8fa5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8fa5-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f8fa5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8fa5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8fa5-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8fa5-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fa5-110">Вертикальное смещение начала очистки (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="f8fa5-110">The vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="f8fa5-111">Центр очистки смещается на этот объем.</span><span class="sxs-lookup"><span data-stu-id="f8fa5-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8fa5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8fa5-112">Return value</span></span>

<span data-ttu-id="f8fa5-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f8fa5-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8fa5-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8fa5-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8fa5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8fa5-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8fa5-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f8fa5-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f8fa5-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f8fa5-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f8fa5-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f8fa5-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8fa5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f8fa5-119">Requirements</span></span>



| <span data-ttu-id="f8fa5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f8fa5-120">Requirement</span></span> | <span data-ttu-id="f8fa5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f8fa5-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8fa5-122">Header</span><span class="sxs-lookup"><span data-stu-id="f8fa5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f8fa5-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8fa5-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f8fa5-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8fa5-124">Library</span></span><br/> | <dl> <span data-ttu-id="f8fa5-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8fa5-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8fa5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8fa5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8fa5-127">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="f8fa5-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




