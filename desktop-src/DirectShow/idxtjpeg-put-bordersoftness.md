---
description: Метод размещения \_ бордерсофтнесс задает ширину размытой области вокруг краев шаблона очистки.
ms.assetid: 9fdbda7f-c89b-4ed8-8035-054bc28f3231
title: 'Идкстжпег: метод ut_BorderSoftness:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c72f59798ca84d01be79110cd4792da0a77f408
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679801"
---
# <a name="idxtjpegput_bordersoftness-method"></a><span data-ttu-id="1d353-103">Идкстжпег::p UT \_ бордерсофтнесс метод</span><span class="sxs-lookup"><span data-stu-id="1d353-103">IDxtJpeg::put\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="1d353-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1d353-104">\[Deprecated.</span></span> <span data-ttu-id="1d353-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1d353-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1d353-106">`put_BorderSoftness`Метод задает ширину размытой области вокруг краев шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="1d353-106">The `put_BorderSoftness` method specifies the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d353-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d353-107">Syntax</span></span>


```C++
HRESULT put_BorderSoftness(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="1d353-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d353-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d353-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1d353-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d353-110">Ширина размытой области в пикселях.</span><span class="sxs-lookup"><span data-stu-id="1d353-110">The width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d353-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d353-111">Return value</span></span>

<span data-ttu-id="1d353-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d353-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d353-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d353-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d353-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d353-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d353-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="1d353-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1d353-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1d353-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1d353-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1d353-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d353-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1d353-118">Requirements</span></span>



| <span data-ttu-id="1d353-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1d353-119">Requirement</span></span> | <span data-ttu-id="1d353-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1d353-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d353-121">Header</span><span class="sxs-lookup"><span data-stu-id="1d353-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1d353-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d353-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1d353-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d353-123">Library</span></span><br/> | <dl> <span data-ttu-id="1d353-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d353-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d353-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d353-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d353-126">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="1d353-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




