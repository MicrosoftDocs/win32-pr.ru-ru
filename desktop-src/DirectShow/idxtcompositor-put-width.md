---
description: Метод размещения \_ ширины задает ширину целевого прямоугольника.
ms.assetid: 16a2d860-6f5d-4f36-ba54-1be2d3fef705
title: 'Идксткомпоситор: метод ut_Width:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_Width
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 55cc3f2f97be2176f13ce3655d3844ef94043409
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679582"
---
# <a name="idxtcompositorput_width-method"></a><span data-ttu-id="86982-103">Идксткомпоситор: метод:p UT \_ Width</span><span class="sxs-lookup"><span data-stu-id="86982-103">IDxtCompositor::put\_Width method</span></span>

> [!Note]  
> <span data-ttu-id="86982-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="86982-104">\[Deprecated.</span></span> <span data-ttu-id="86982-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="86982-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="86982-106">`put_Width`Метод задает ширину целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="86982-106">The `put_Width` method specifies the width of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="86982-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86982-107">Syntax</span></span>


```C++
HRESULT put_Width(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="86982-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="86982-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86982-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86982-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86982-110">Ширина целевого прямоугольника в пикселях.</span><span class="sxs-lookup"><span data-stu-id="86982-110">The width of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86982-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86982-111">Return value</span></span>

<span data-ttu-id="86982-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="86982-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86982-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86982-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="86982-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86982-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="86982-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="86982-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="86982-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="86982-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="86982-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="86982-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86982-118">Требования</span><span class="sxs-lookup"><span data-stu-id="86982-118">Requirements</span></span>



| <span data-ttu-id="86982-119">Требование</span><span class="sxs-lookup"><span data-stu-id="86982-119">Requirement</span></span> | <span data-ttu-id="86982-120">Значение</span><span class="sxs-lookup"><span data-stu-id="86982-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86982-121">Header</span><span class="sxs-lookup"><span data-stu-id="86982-121">Header</span></span><br/>  | <dl> <span data-ttu-id="86982-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="86982-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="86982-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86982-123">Library</span></span><br/> | <dl> <span data-ttu-id="86982-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86982-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86982-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86982-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86982-126">**Интерфейс Идксткомпоситор**</span><span class="sxs-lookup"><span data-stu-id="86982-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




