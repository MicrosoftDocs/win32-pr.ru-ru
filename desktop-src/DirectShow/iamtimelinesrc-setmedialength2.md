---
description: 'Метод SetMediaLength2 задает длительность исходного файла. Этот метод эквивалентен Иамтимелинесрк:: Сетмедиаленгс, но принимает значение РЕФТИМЕ.'
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'Метод Иамтимелинесрк:: SetMediaLength2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675883"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a><span data-ttu-id="a8d45-104">Метод Иамтимелинесрк:: SetMediaLength2</span><span class="sxs-lookup"><span data-stu-id="a8d45-104">IAMTimelineSrc::SetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="a8d45-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a8d45-105">\[Deprecated.</span></span> <span data-ttu-id="a8d45-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a8d45-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a8d45-107">`SetMediaLength2`Метод задает длительность исходного файла.</span><span class="sxs-lookup"><span data-stu-id="a8d45-107">The `SetMediaLength2` method specifies the duration of the source file.</span></span> <span data-ttu-id="a8d45-108">Этот метод эквивалентен [**иамтимелинесрк:: сетмедиаленгс**](iamtimelinesrc-setmedialength.md), но принимает значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d45-108">This method is equivalent to [**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d45-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8d45-109">Syntax</span></span>


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="a8d45-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8d45-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d45-111">*Длина*</span><span class="sxs-lookup"><span data-stu-id="a8d45-111">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d45-112">Длина носителя в секундах.</span><span class="sxs-lookup"><span data-stu-id="a8d45-112">Media length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8d45-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8d45-113">Return value</span></span>

<span data-ttu-id="a8d45-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a8d45-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8d45-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8d45-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8d45-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8d45-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a8d45-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="a8d45-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a8d45-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a8d45-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a8d45-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a8d45-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a8d45-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a8d45-120">Requirements</span></span>



| <span data-ttu-id="a8d45-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a8d45-121">Requirement</span></span> | <span data-ttu-id="a8d45-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a8d45-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d45-123">Header</span><span class="sxs-lookup"><span data-stu-id="a8d45-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a8d45-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8d45-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a8d45-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a8d45-125">Library</span></span><br/> | <dl> <span data-ttu-id="a8d45-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8d45-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8d45-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8d45-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d45-128">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="a8d45-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="a8d45-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="a8d45-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




