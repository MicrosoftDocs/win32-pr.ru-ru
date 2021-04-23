---
description: Метод размещения \_ маскнум указывает код очистки SMPTE.
ms.assetid: d2d2382c-d920-49e7-b9b7-6897356a78de
title: 'Идкстжпег: метод ut_MaskNum:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f814fab2654a5585567273301dab285c32a1019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675363"
---
# <a name="idxtjpegput_masknum-method"></a><span data-ttu-id="3278c-103">Идкстжпег::p UT \_ маскнум метод</span><span class="sxs-lookup"><span data-stu-id="3278c-103">IDxtJpeg::put\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="3278c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3278c-104">\[Deprecated.</span></span> <span data-ttu-id="3278c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3278c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3278c-106">`put_MaskNum`Метод указывает код очистки SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3278c-106">The `put_MaskNum` method specifies the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="3278c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3278c-107">Syntax</span></span>


```C++
HRESULT put_MaskNum(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="3278c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3278c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3278c-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3278c-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3278c-110">Указывает код очистки SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3278c-110">Specifies the SMPTE wipe code.</span></span> <span data-ttu-id="3278c-111">Список поддерживаемых SMPTE очистки см. в разделе Переход на [SMPTE очистки](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="3278c-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3278c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3278c-112">Return value</span></span>

<span data-ttu-id="3278c-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3278c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3278c-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3278c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3278c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3278c-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3278c-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="3278c-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3278c-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3278c-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3278c-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3278c-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3278c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3278c-119">Requirements</span></span>



| <span data-ttu-id="3278c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3278c-120">Requirement</span></span> | <span data-ttu-id="3278c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3278c-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3278c-122">Header</span><span class="sxs-lookup"><span data-stu-id="3278c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3278c-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="3278c-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3278c-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3278c-124">Library</span></span><br/> | <dl> <span data-ttu-id="3278c-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3278c-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3278c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3278c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3278c-127">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="3278c-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




