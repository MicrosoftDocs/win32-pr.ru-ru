---
description: Метод Сетдефаултфпс задает частоту кадров исходного объекта по умолчанию.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'Метод Иамтимелинесрк:: Сетдефаултфпс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675885"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a><span data-ttu-id="93f7d-103">Метод Иамтимелинесрк:: Сетдефаултфпс</span><span class="sxs-lookup"><span data-stu-id="93f7d-103">IAMTimelineSrc::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="93f7d-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="93f7d-104">\[Deprecated.</span></span> <span data-ttu-id="93f7d-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="93f7d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="93f7d-106">`SetDefaultFPS`Метод задает частоту кадров исходного объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93f7d-106">The `SetDefaultFPS` method sets the source object's default frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f7d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93f7d-107">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="93f7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="93f7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93f7d-109">*Кадры в секунду*</span><span class="sxs-lookup"><span data-stu-id="93f7d-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="93f7d-110">Частота кадров по умолчанию в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="93f7d-110">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93f7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93f7d-111">Return value</span></span>

<span data-ttu-id="93f7d-112">Возвращает \_ ОК в случае успеха или E \_ INVALIDARG, если указанная частота кадров меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="93f7d-112">Returns S\_OK if successful, or E\_INVALIDARG if the specified frame rate is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="93f7d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93f7d-113">Remarks</span></span>

<span data-ttu-id="93f7d-114">Модуль подготовки отчетов использует это значение, если не может определить частоту кадров из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="93f7d-114">The render engine uses this value if it cannot determine the frame rate from the original source file.</span></span>

<span data-ttu-id="93f7d-115">Вызывайте этот метод только для исходных файлов без стандартной частоты кадров.</span><span class="sxs-lookup"><span data-stu-id="93f7d-115">Call this method only for source files without a predefined frame rate.</span></span> <span data-ttu-id="93f7d-116">Для растровых и JPEG-файлов частота кадров по умолчанию равна нулю, что приводит к отображению источника в виде изображения по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="93f7d-116">For bitmap and JPEG files, the default frame rate is zero, which causes the source to be rendered as a still image.</span></span> <span data-ttu-id="93f7d-117">Чтобы использовать изображение в качестве первого кадра в последовательности DIB, задайте для параметра Частота кадров значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="93f7d-117">To use the image as the first frame in a DIB sequence set the frame rate to a value greater than zero.</span></span> <span data-ttu-id="93f7d-118">Дополнительные сведения см. в разделе [Работа с источниками](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="93f7d-118">For more information, see [Working with Sources](working-with-sources.md).</span></span>

> [!Note]  
> <span data-ttu-id="93f7d-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="93f7d-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="93f7d-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="93f7d-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="93f7d-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="93f7d-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="93f7d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="93f7d-122">Requirements</span></span>



| <span data-ttu-id="93f7d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="93f7d-123">Requirement</span></span> | <span data-ttu-id="93f7d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="93f7d-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93f7d-125">Header</span><span class="sxs-lookup"><span data-stu-id="93f7d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="93f7d-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="93f7d-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="93f7d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="93f7d-127">Library</span></span><br/> | <dl> <span data-ttu-id="93f7d-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93f7d-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f7d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93f7d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f7d-130">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="93f7d-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="93f7d-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="93f7d-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




