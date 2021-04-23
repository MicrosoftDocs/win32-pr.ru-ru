---
description: Метод «разместить \_ BorderColor» задает цвет границы вокруг краев шаблона очистки.
ms.assetid: d6a49956-8fc9-4ba2-8485-a49175da3cf7
title: 'Идкстжпег: метод ut_BorderColor:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: faacc76eaa120467aa6cfb6c318aac0d9baec334
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675116"
---
# <a name="idxtjpegput_bordercolor-method"></a><span data-ttu-id="cf62e-103">Идкстжпег::p \_ методу UT BorderColor</span><span class="sxs-lookup"><span data-stu-id="cf62e-103">IDxtJpeg::put\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="cf62e-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cf62e-104">\[Deprecated.</span></span> <span data-ttu-id="cf62e-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cf62e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cf62e-106">`put_BorderColor`Метод задает цвет границы вокруг границ шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="cf62e-106">The `put_BorderColor` method specifies the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf62e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf62e-107">Syntax</span></span>


```C++
HRESULT put_BorderColor(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="cf62e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf62e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf62e-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf62e-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf62e-110">Задает цвет в виде шестнадцатеричного числа в формате 0xRRGGBB, где RR — это красная величина, а параметр GG — зеленое значение, а BB — синий.</span><span class="sxs-lookup"><span data-stu-id="cf62e-110">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf62e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf62e-111">Return value</span></span>

<span data-ttu-id="cf62e-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cf62e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf62e-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf62e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf62e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf62e-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cf62e-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="cf62e-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cf62e-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf62e-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cf62e-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cf62e-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf62e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cf62e-118">Requirements</span></span>



| <span data-ttu-id="cf62e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cf62e-119">Requirement</span></span> | <span data-ttu-id="cf62e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cf62e-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf62e-121">Header</span><span class="sxs-lookup"><span data-stu-id="cf62e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cf62e-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf62e-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cf62e-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf62e-123">Library</span></span><br/> | <dl> <span data-ttu-id="cf62e-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf62e-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf62e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf62e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf62e-126">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="cf62e-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




