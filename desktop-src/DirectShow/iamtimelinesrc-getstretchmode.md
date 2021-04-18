---
description: Метод Жетстретчмоде извлекает режим Stretch. Режим растяжения определяет способ подготовки источника видео, если его размер не соответствует выходным измерениям.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: 'Метод Иамтимелинесрк:: Жетстретчмоде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f10552ac67c50e8656f303fd524bdad2cd07823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679892"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a><span data-ttu-id="6f055-104">Метод Иамтимелинесрк:: Жетстретчмоде</span><span class="sxs-lookup"><span data-stu-id="6f055-104">IAMTimelineSrc::GetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="6f055-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6f055-105">\[Deprecated.</span></span> <span data-ttu-id="6f055-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6f055-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6f055-107">`GetStretchMode`Метод извлекает режим растяжения.</span><span class="sxs-lookup"><span data-stu-id="6f055-107">The `GetStretchMode` method retrieves the stretch mode.</span></span> <span data-ttu-id="6f055-108">Режим растяжения определяет способ подготовки источника видео, если его размер не соответствует выходным измерениям.</span><span class="sxs-lookup"><span data-stu-id="6f055-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f055-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f055-109">Syntax</span></span>


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="6f055-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f055-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f055-111">*пнстретчмоде*</span><span class="sxs-lookup"><span data-stu-id="6f055-111">*pnStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="6f055-112">Получает флаг, указывающий текущий режим Stretch.</span><span class="sxs-lookup"><span data-stu-id="6f055-112">Receives a flag indicating the current stretch mode.</span></span> <span data-ttu-id="6f055-113">Список возможных значений см. в разделе [**изменение размера флагов**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6f055-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f055-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f055-114">Return value</span></span>

<span data-ttu-id="6f055-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6f055-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f055-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f055-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f055-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f055-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6f055-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="6f055-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6f055-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6f055-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6f055-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6f055-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f055-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6f055-121">Requirements</span></span>



| <span data-ttu-id="6f055-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6f055-122">Requirement</span></span> | <span data-ttu-id="6f055-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6f055-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f055-124">Header</span><span class="sxs-lookup"><span data-stu-id="6f055-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6f055-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f055-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6f055-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f055-126">Library</span></span><br/> | <dl> <span data-ttu-id="6f055-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f055-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f055-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f055-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f055-129">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="6f055-129">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="6f055-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="6f055-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




