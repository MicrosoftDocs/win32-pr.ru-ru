---
description: Метод размещения \_ сркоффсети задает вертикальное смещение исходного прямоугольника.
ms.assetid: abdc520f-8de6-4a4f-aa8f-facedaa8fce1
title: 'Идксткомпоситор: метод ut_SrcOffsetY:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcOffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ad574939ce9f3d694944d39af76787dd19a22735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675141"
---
# <a name="idxtcompositorput_srcoffsety-method"></a><span data-ttu-id="18446-103">Идксткомпоситор::p UT \_ сркоффсети метод</span><span class="sxs-lookup"><span data-stu-id="18446-103">IDxtCompositor::put\_SrcOffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="18446-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="18446-104">\[Deprecated.</span></span> <span data-ttu-id="18446-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="18446-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="18446-106">`put_SrcOffsetY`Метод задает вертикальное смещение исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="18446-106">The `put_SrcOffsetY` method specifies the vertical offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="18446-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18446-107">Syntax</span></span>


```C++
HRESULT put_SrcOffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="18446-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="18446-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18446-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18446-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18446-110">Вертикальное смещение исходного прямоугольника в пикселях.</span><span class="sxs-lookup"><span data-stu-id="18446-110">The vertical offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18446-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18446-111">Return value</span></span>

<span data-ttu-id="18446-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="18446-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18446-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18446-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18446-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18446-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="18446-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="18446-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="18446-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="18446-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="18446-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="18446-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18446-118">Требования</span><span class="sxs-lookup"><span data-stu-id="18446-118">Requirements</span></span>



| <span data-ttu-id="18446-119">Требование</span><span class="sxs-lookup"><span data-stu-id="18446-119">Requirement</span></span> | <span data-ttu-id="18446-120">Значение</span><span class="sxs-lookup"><span data-stu-id="18446-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18446-121">Header</span><span class="sxs-lookup"><span data-stu-id="18446-121">Header</span></span><br/>  | <dl> <span data-ttu-id="18446-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="18446-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="18446-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="18446-123">Library</span></span><br/> | <dl> <span data-ttu-id="18446-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18446-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18446-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18446-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18446-126">**Интерфейс Идксткомпоситор**</span><span class="sxs-lookup"><span data-stu-id="18446-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




