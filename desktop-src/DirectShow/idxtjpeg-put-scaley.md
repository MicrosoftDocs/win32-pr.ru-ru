---
description: Метод вставки \_ масштаба задает величину, на которую производится растяжение очистки по вертикали.
ms.assetid: 1dd84540-b249-482c-9cb7-aab8c7dc4d25
title: 'Идкстжпег: метод ut_ScaleY:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65a8b736dc66ec9dad20b1e261ecd7b0c4556774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675233"
---
# <a name="idxtjpegput_scaley-method"></a><span data-ttu-id="e3c78-103">Идкстжпег: \_ метод масштабирования:p UT</span><span class="sxs-lookup"><span data-stu-id="e3c78-103">IDxtJpeg::put\_ScaleY method</span></span>

> [!Note]  
> <span data-ttu-id="e3c78-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e3c78-104">\[Deprecated.</span></span> <span data-ttu-id="e3c78-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3c78-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e3c78-106">`put_ScaleY`Метод задает величину, на которую производится растяжение очистки по вертикали.</span><span class="sxs-lookup"><span data-stu-id="e3c78-106">The `put_ScaleY` method specifies the amount by which the wipe is stretched vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c78-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3c78-107">Syntax</span></span>


```C++
HRESULT put_ScaleY(
  [in] double newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e3c78-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3c78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3c78-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3c78-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c78-110">Величина, на которую производится растяжение очистки по вертикали в процентах от исходного определения очистки.</span><span class="sxs-lookup"><span data-stu-id="e3c78-110">The amount by which the wipe is stretched vertically, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="e3c78-111">Например, значение 1,0 означает отсутствие растяжения, а 2,0 означает 200% растяжения.</span><span class="sxs-lookup"><span data-stu-id="e3c78-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3c78-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3c78-112">Return value</span></span>

<span data-ttu-id="e3c78-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e3c78-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3c78-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3c78-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c78-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3c78-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e3c78-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="e3c78-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e3c78-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3c78-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e3c78-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e3c78-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3c78-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e3c78-119">Requirements</span></span>



| <span data-ttu-id="e3c78-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e3c78-120">Requirement</span></span> | <span data-ttu-id="e3c78-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e3c78-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c78-122">Header</span><span class="sxs-lookup"><span data-stu-id="e3c78-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e3c78-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c78-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e3c78-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3c78-124">Library</span></span><br/> | <dl> <span data-ttu-id="e3c78-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3c78-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3c78-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3c78-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c78-127">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="e3c78-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




