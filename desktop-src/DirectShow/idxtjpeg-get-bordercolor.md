---
description: Метод Get \_ BorderColor извлекает цвет границы вокруг границ шаблона очистки.
ms.assetid: 9d36cc49-c174-4b93-a030-ca8d2890c624
title: 'Метод Идкстжпег:: get_BorderColor (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f37c37865caf76839733ada376ec637747977ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679713"
---
# <a name="idxtjpegget_bordercolor-method"></a><span data-ttu-id="7f2a2-103">Метод Идкстжпег:: Get \_ BorderColor</span><span class="sxs-lookup"><span data-stu-id="7f2a2-103">IDxtJpeg::get\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="7f2a2-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7f2a2-104">\[Deprecated.</span></span> <span data-ttu-id="7f2a2-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7f2a2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7f2a2-106">`get_BorderColor`Метод получает цвет границы вокруг границ шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="7f2a2-106">The `get_BorderColor` method retrieves the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f2a2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f2a2-107">Syntax</span></span>


```C++
HRESULT get_BorderColor(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="7f2a2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f2a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f2a2-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7f2a2-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2a2-110">Получает цвет.</span><span class="sxs-lookup"><span data-stu-id="7f2a2-110">Receives the color.</span></span> <span data-ttu-id="7f2a2-111">Возвращаемое значение представляет собой шестнадцатеричное число в формате 0xRRGGBB, где RR — это значение красного цвета, а параметр GG — зеленое значение, а BB — синий.</span><span class="sxs-lookup"><span data-stu-id="7f2a2-111">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f2a2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f2a2-112">Return value</span></span>

<span data-ttu-id="7f2a2-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7f2a2-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f2a2-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f2a2-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f2a2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f2a2-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7f2a2-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="7f2a2-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7f2a2-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7f2a2-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7f2a2-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7f2a2-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7f2a2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7f2a2-119">Requirements</span></span>



| <span data-ttu-id="7f2a2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7f2a2-120">Requirement</span></span> | <span data-ttu-id="7f2a2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7f2a2-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2a2-122">Header</span><span class="sxs-lookup"><span data-stu-id="7f2a2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7f2a2-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f2a2-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7f2a2-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f2a2-124">Library</span></span><br/> | <dl> <span data-ttu-id="7f2a2-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f2a2-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f2a2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f2a2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f2a2-127">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="7f2a2-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




