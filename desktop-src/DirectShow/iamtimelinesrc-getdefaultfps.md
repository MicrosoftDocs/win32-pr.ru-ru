---
description: Метод Жетдефаултфпс извлекает частоту кадров исходного объекта по умолчанию. Модуль подготовки отчетов использует это значение, если не может определить частоту кадров от исходного источника.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'Метод Иамтимелинесрк:: Жетдефаултфпс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685081"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a><span data-ttu-id="07d72-104">Метод Иамтимелинесрк:: Жетдефаултфпс</span><span class="sxs-lookup"><span data-stu-id="07d72-104">IAMTimelineSrc::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="07d72-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="07d72-105">\[Deprecated.</span></span> <span data-ttu-id="07d72-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="07d72-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="07d72-107">`GetDefaultFPS`Метод извлекает частоту кадров по умолчанию для исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="07d72-107">The `GetDefaultFPS` method retrieves the source object's default frame rate.</span></span> <span data-ttu-id="07d72-108">Модуль подготовки отчетов использует это значение, если не может определить частоту кадров от исходного источника.</span><span class="sxs-lookup"><span data-stu-id="07d72-108">The render engine uses this value if it cannot determine the frame rate from the original source.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d72-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07d72-109">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="07d72-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="07d72-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d72-111">*пфпс*</span><span class="sxs-lookup"><span data-stu-id="07d72-111">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="07d72-112">Получает частоту кадров по умолчанию в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="07d72-112">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d72-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07d72-113">Return value</span></span>

<span data-ttu-id="07d72-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="07d72-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07d72-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07d72-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="07d72-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07d72-116">Remarks</span></span>

<span data-ttu-id="07d72-117">Частота кадров по умолчанию не требуется, если формат файла задает частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="07d72-117">The default frame rate is not required if the file format specifies the frame rate.</span></span> <span data-ttu-id="07d72-118">Это так для форматов аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="07d72-118">This is the case for audio and video formats.</span></span>

<span data-ttu-id="07d72-119">Если источником является точечный рисунок или изображение JPEG, подсистема визуализации использует его в качестве первого изображения в последовательности DIB (не зависящей от устройства) с частотой кадров, равной частоте кадров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07d72-119">If the source is a bitmap or JPEG image, the render engine uses it as the first image in a device-independent bitmap (DIB) sequence, with a frame rate equal to the default frame rate.</span></span> <span data-ttu-id="07d72-120">Чтобы отобразить статическое изображение, а не последовательность DIB, задайте для параметра Частота кадров по умолчанию значение 0.</span><span class="sxs-lookup"><span data-stu-id="07d72-120">To render a static image, rather than a DIB sequence, set the default frame rate to 0.</span></span>

<span data-ttu-id="07d72-121">Если источником является GIF, не устанавливайте частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="07d72-121">If the source is a GIF, do not set the frame rate.</span></span> <span data-ttu-id="07d72-122">Для анимированных GIF-файлов в GIF-файле указывается задержка между изображениями.</span><span class="sxs-lookup"><span data-stu-id="07d72-122">For animated GIFs, the GIF file specifies the delay between each image.</span></span>

> [!Note]  
> <span data-ttu-id="07d72-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="07d72-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="07d72-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="07d72-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="07d72-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="07d72-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="07d72-126">Требования</span><span class="sxs-lookup"><span data-stu-id="07d72-126">Requirements</span></span>



| <span data-ttu-id="07d72-127">Требование</span><span class="sxs-lookup"><span data-stu-id="07d72-127">Requirement</span></span> | <span data-ttu-id="07d72-128">Значение</span><span class="sxs-lookup"><span data-stu-id="07d72-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07d72-129">Header</span><span class="sxs-lookup"><span data-stu-id="07d72-129">Header</span></span><br/>  | <dl> <span data-ttu-id="07d72-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d72-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="07d72-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07d72-131">Library</span></span><br/> | <dl> <span data-ttu-id="07d72-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07d72-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d72-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07d72-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d72-134">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="07d72-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="07d72-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="07d72-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




