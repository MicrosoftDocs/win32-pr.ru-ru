---
description: Метод размещения \_ срчеигхт задает высоту исходного прямоугольника.
ms.assetid: 80c8cf92-36e2-4e57-8ce7-6a114bc8bab4
title: 'Идксткомпоситор: метод ut_SrcHeight:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcHeight
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 80697a3c4a159256389f48273e66ca86547478fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675731"
---
# <a name="idxtcompositorput_srcheight-method"></a><span data-ttu-id="9c0b4-103">Идксткомпоситор::p UT \_ срчеигхт метод</span><span class="sxs-lookup"><span data-stu-id="9c0b4-103">IDxtCompositor::put\_SrcHeight method</span></span>

> [!Note]  
> <span data-ttu-id="9c0b4-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9c0b4-104">\[Deprecated.</span></span> <span data-ttu-id="9c0b4-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9c0b4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9c0b4-106">`put_SrcHeight`Метод задает высоту исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="9c0b4-106">The `put_SrcHeight` method specifies the height of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c0b4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c0b4-107">Syntax</span></span>


```C++
HRESULT put_SrcHeight(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="9c0b4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c0b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c0b4-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c0b4-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0b4-110">Высота исходного прямоугольника (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="9c0b4-110">The height of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c0b4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c0b4-111">Return value</span></span>

<span data-ttu-id="9c0b4-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9c0b4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9c0b4-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9c0b4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c0b4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c0b4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9c0b4-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="9c0b4-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9c0b4-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9c0b4-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9c0b4-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9c0b4-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c0b4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9c0b4-118">Requirements</span></span>



| <span data-ttu-id="9c0b4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9c0b4-119">Requirement</span></span> | <span data-ttu-id="9c0b4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9c0b4-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0b4-121">Header</span><span class="sxs-lookup"><span data-stu-id="9c0b4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9c0b4-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c0b4-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9c0b4-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9c0b4-123">Library</span></span><br/> | <dl> <span data-ttu-id="9c0b4-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c0b4-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c0b4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c0b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c0b4-126">**Интерфейс Идксткомпоситор**</span><span class="sxs-lookup"><span data-stu-id="9c0b4-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




