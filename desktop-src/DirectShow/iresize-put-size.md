---
description: Метод помещения \_ размера задает размер выходных данных и режим Stretch.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'Иресизе: метод ut_Size:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675345"
---
# <a name="iresizeput_size-method"></a><span data-ttu-id="a6bab-103">Иресизе: метод:p UT \_ size</span><span class="sxs-lookup"><span data-stu-id="a6bab-103">IResize::put\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="a6bab-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a6bab-104">\[Deprecated.</span></span> <span data-ttu-id="a6bab-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a6bab-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a6bab-106">`put_Size`Метод задает размер выходных данных и режим Stretch.</span><span class="sxs-lookup"><span data-stu-id="a6bab-106">The `put_Size` method sets the output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6bab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6bab-107">Syntax</span></span>


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a><span data-ttu-id="a6bab-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6bab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6bab-109">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6bab-109">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bab-110">Высота видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a6bab-110">The video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a6bab-111">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6bab-111">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bab-112">Ширина видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a6bab-112">The video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a6bab-113">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6bab-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bab-114">Режим Stretch.</span><span class="sxs-lookup"><span data-stu-id="a6bab-114">The stretch mode.</span></span> <span data-ttu-id="a6bab-115">Возможные значения см. в разделе [**изменение размера флагов**](resize-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="a6bab-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6bab-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6bab-116">Return value</span></span>

<span data-ttu-id="a6bab-117">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6bab-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6bab-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6bab-118">Remarks</span></span>

<span data-ttu-id="a6bab-119">DES может вызывать этот метод до или после вызова метода **размещения \_ mediaType**.</span><span class="sxs-lookup"><span data-stu-id="a6bab-119">DES may call this method before or after calling **put\_MediaType**.</span></span> <span data-ttu-id="a6bab-120">Если DES вызывает этот метод перед вызовом метода OUTPUT **\_ mediaType**, фильтр должен выбрать значение по умолчанию для битовой глубины и использовать значения размера для создания выходного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="a6bab-120">If DES calls this method before calling **put\_MediaType**, the filter should select a default value for the bit depth and use the size values to construct an output media type.</span></span> <span data-ttu-id="a6bab-121">Если DES вызывает этот метод после вызова метода OUTPUT **\_ mediaType**, фильтр должен изменить его текущий тип вывода на новые размеры.</span><span class="sxs-lookup"><span data-stu-id="a6bab-121">If DES calls this method after calling **put\_MediaType**, the filter should modify its current output type with the new sizes.</span></span>

<span data-ttu-id="a6bab-122">DES может также вызывать этот метод после подключения выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="a6bab-122">DES may also call this method after the output pin is connected.</span></span> <span data-ttu-id="a6bab-123">В этом случае измените тип выходных данных и повторно подключите выходной ПИН-код к новому типу.</span><span class="sxs-lookup"><span data-stu-id="a6bab-123">In that case, modify the output type and reconnect the output pin with the new type.</span></span> <span data-ttu-id="a6bab-124">Дополнительные сведения см. в разделе [Повторное подключение ПИН](reconnecting-pins.md) -кодов.</span><span class="sxs-lookup"><span data-stu-id="a6bab-124">See [Reconnecting Pins](reconnecting-pins.md) for more information.</span></span>

<span data-ttu-id="a6bab-125">Параметр *flags* указывает, как фильтр должен выполнить операцию изменения размера.</span><span class="sxs-lookup"><span data-stu-id="a6bab-125">The *Flags* parameter specifies how the filter should perform the resizing operation.</span></span>

> [!Note]  
> <span data-ttu-id="a6bab-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="a6bab-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a6bab-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6bab-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a6bab-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a6bab-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6bab-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a6bab-129">Requirements</span></span>



| <span data-ttu-id="a6bab-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a6bab-130">Requirement</span></span> | <span data-ttu-id="a6bab-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a6bab-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bab-132">Версия</span><span class="sxs-lookup"><span data-stu-id="a6bab-132">Version</span></span><br/> | <span data-ttu-id="a6bab-133">DirectX 9,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a6bab-133">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="a6bab-134">Header</span><span class="sxs-lookup"><span data-stu-id="a6bab-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a6bab-135"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6bab-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a6bab-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a6bab-136">Library</span></span><br/> | <dl> <span data-ttu-id="a6bab-137"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6bab-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6bab-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6bab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6bab-139">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="a6bab-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="a6bab-140">**Интерфейс Иресизе**</span><span class="sxs-lookup"><span data-stu-id="a6bab-140">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




