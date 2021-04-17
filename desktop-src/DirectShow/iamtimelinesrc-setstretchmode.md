---
description: Метод Сетстретчмоде задает режим Stretch. Режим растяжения определяет способ подготовки источника видео, если его размер не соответствует выходным измерениям.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'Метод Иамтимелинесрк:: Сетстретчмоде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685196"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a><span data-ttu-id="42271-104">Метод Иамтимелинесрк:: Сетстретчмоде</span><span class="sxs-lookup"><span data-stu-id="42271-104">IAMTimelineSrc::SetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="42271-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="42271-105">\[Deprecated.</span></span> <span data-ttu-id="42271-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="42271-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="42271-107">`SetStretchMode`Метод задает режим Stretch.</span><span class="sxs-lookup"><span data-stu-id="42271-107">The `SetStretchMode` method sets the stretch mode.</span></span> <span data-ttu-id="42271-108">Режим растяжения определяет способ подготовки источника видео, если его размер не соответствует выходным измерениям.</span><span class="sxs-lookup"><span data-stu-id="42271-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="42271-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42271-109">Syntax</span></span>


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="42271-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="42271-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42271-111">*нстретчмоде*</span><span class="sxs-lookup"><span data-stu-id="42271-111">*nStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="42271-112">Флаг, указывающий текущий режим Stretch.</span><span class="sxs-lookup"><span data-stu-id="42271-112">Flag indicating the current stretch mode.</span></span> <span data-ttu-id="42271-113">Список возможных значений см. в разделе [**изменение размера флагов**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="42271-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42271-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42271-114">Return value</span></span>

<span data-ttu-id="42271-115">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="42271-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="42271-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42271-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="42271-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="42271-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="42271-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="42271-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="42271-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="42271-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42271-120">Требования</span><span class="sxs-lookup"><span data-stu-id="42271-120">Requirements</span></span>



| <span data-ttu-id="42271-121">Требование</span><span class="sxs-lookup"><span data-stu-id="42271-121">Requirement</span></span> | <span data-ttu-id="42271-122">Значение</span><span class="sxs-lookup"><span data-stu-id="42271-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42271-123">Header</span><span class="sxs-lookup"><span data-stu-id="42271-123">Header</span></span><br/>  | <dl> <span data-ttu-id="42271-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="42271-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="42271-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42271-125">Library</span></span><br/> | <dl> <span data-ttu-id="42271-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42271-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42271-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42271-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42271-128">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="42271-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="42271-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="42271-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




