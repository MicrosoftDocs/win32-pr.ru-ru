---
description: Метод Сетбуфферсамплес указывает, следует ли копировать демонстрационные данные в буфер, так как он проходит через фильтр.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'Метод Исамплеграббер:: Сетбуфферсамплес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675953"
---
# <a name="isamplegrabbersetbuffersamples-method"></a><span data-ttu-id="ea295-103">Метод Исамплеграббер:: Сетбуфферсамплес</span><span class="sxs-lookup"><span data-stu-id="ea295-103">ISampleGrabber::SetBufferSamples method</span></span>

> [!Note]  
> <span data-ttu-id="ea295-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ea295-104">\[Deprecated.</span></span> <span data-ttu-id="ea295-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ea295-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ea295-106">Метод **сетбуфферсамплес** указывает, следует ли копировать демонстрационные данные в буфер, так как он проходит через фильтр.</span><span class="sxs-lookup"><span data-stu-id="ea295-106">The **SetBufferSamples** method specifies whether to copy sample data into a buffer as it goes through the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea295-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea295-107">Syntax</span></span>


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a><span data-ttu-id="ea295-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea295-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea295-109">*буфферсем*</span><span class="sxs-lookup"><span data-stu-id="ea295-109">*BufferThem*</span></span> 
</dt> <dd>

<span data-ttu-id="ea295-110">Логическое значение, указывающее, следует ли заменять образец данных в буфер.</span><span class="sxs-lookup"><span data-stu-id="ea295-110">Boolean value specifying whether to buffer sample data.</span></span> <span data-ttu-id="ea295-111">Если **значение — true**, фильтр копирует демонстрационные данные во внутренний буфер.</span><span class="sxs-lookup"><span data-stu-id="ea295-111">If **TRUE**, the filter copies sample data into an internal buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea295-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea295-112">Return value</span></span>

<span data-ttu-id="ea295-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ea295-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea295-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea295-114">Remarks</span></span>

<span data-ttu-id="ea295-115">Чтобы получить скопированный буфер, вызовите метод [**исамплеграббер:: жеткуррентбуффер**](isamplegrabber-getcurrentbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ea295-115">To get the copied buffer, call [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="ea295-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ea295-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ea295-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ea295-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ea295-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ea295-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea295-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ea295-119">Requirements</span></span>



| <span data-ttu-id="ea295-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ea295-120">Requirement</span></span> | <span data-ttu-id="ea295-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ea295-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea295-122">Header</span><span class="sxs-lookup"><span data-stu-id="ea295-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ea295-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea295-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ea295-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ea295-124">Library</span></span><br/> | <dl> <span data-ttu-id="ea295-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea295-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea295-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea295-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea295-127">Использование образца захвата</span><span class="sxs-lookup"><span data-stu-id="ea295-127">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="ea295-128">**Интерфейс Исамплеграббер**</span><span class="sxs-lookup"><span data-stu-id="ea295-128">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




