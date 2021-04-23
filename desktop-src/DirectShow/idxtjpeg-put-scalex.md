---
description: Метод Where \_ ScaleX задает величину, на которую производится растяжение очистки по горизонтали.
ms.assetid: d57af5dc-41e0-45a7-8f11-55ef3bc62549
title: 'Идкстжпег: метод ut_ScaleX:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fff0583ce3163ebf5626cfdbb82edf5c927bdc9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675234"
---
# <a name="idxtjpegput_scalex-method"></a><span data-ttu-id="d61eb-103">Идкстжпег: метод:p UT \_ ScaleX</span><span class="sxs-lookup"><span data-stu-id="d61eb-103">IDxtJpeg::put\_ScaleX method</span></span>

> [!Note]  
> <span data-ttu-id="d61eb-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d61eb-104">\[Deprecated.</span></span> <span data-ttu-id="d61eb-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d61eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d61eb-106">`put_ScaleX`Метод задает величину, на которую производится растяжение очистки по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d61eb-106">The `put_ScaleX` method specifies the amount by which the wipe is stretched horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="d61eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d61eb-107">Syntax</span></span>


```C++
HRESULT put_ScaleX(
  [in] double newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d61eb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d61eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d61eb-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d61eb-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d61eb-110">Величина, на которую производится растяжение очистки по горизонтали в процентах от исходного определения очистки.</span><span class="sxs-lookup"><span data-stu-id="d61eb-110">The amount by which the wipe is stretched horizontally, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="d61eb-111">Например, значение 1,0 означает отсутствие растяжения, а 2,0 означает 200% растяжения.</span><span class="sxs-lookup"><span data-stu-id="d61eb-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d61eb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d61eb-112">Return value</span></span>

<span data-ttu-id="d61eb-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d61eb-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d61eb-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d61eb-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d61eb-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d61eb-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d61eb-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d61eb-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d61eb-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d61eb-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d61eb-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d61eb-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d61eb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d61eb-119">Requirements</span></span>



| <span data-ttu-id="d61eb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d61eb-120">Requirement</span></span> | <span data-ttu-id="d61eb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d61eb-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d61eb-122">Header</span><span class="sxs-lookup"><span data-stu-id="d61eb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d61eb-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d61eb-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d61eb-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d61eb-124">Library</span></span><br/> | <dl> <span data-ttu-id="d61eb-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d61eb-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d61eb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d61eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d61eb-127">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="d61eb-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




