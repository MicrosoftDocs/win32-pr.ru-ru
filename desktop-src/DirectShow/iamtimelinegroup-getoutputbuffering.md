---
description: Метод Жетаутпутбуфферинг Извлекает число кадров, отображаемых заранее во время просмотра.
ms.assetid: 93cb8d18-f1b7-48f9-af41-97f010304b05
title: 'Метод Иамтимелинеграуп:: Жетаутпутбуфферинг (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8213be882ca445775137a946d9064487b25f48af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689497"
---
# <a name="iamtimelinegroupgetoutputbuffering-method"></a><span data-ttu-id="f550f-103">Метод Иамтимелинеграуп:: Жетаутпутбуфферинг</span><span class="sxs-lookup"><span data-stu-id="f550f-103">IAMTimelineGroup::GetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="f550f-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f550f-104">\[Deprecated.</span></span> <span data-ttu-id="f550f-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f550f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f550f-106">`GetOutputBuffering`Метод получает число кадров, отображаемых заранее во время просмотра.</span><span class="sxs-lookup"><span data-stu-id="f550f-106">The `GetOutputBuffering` method retrieves the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="f550f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f550f-107">Syntax</span></span>


```C++
HRESULT GetOutputBuffering(
  [out] int *pnBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="f550f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f550f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f550f-109">*пнбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f550f-109">*pnBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f550f-110">Получает число кадров в буфере.</span><span class="sxs-lookup"><span data-stu-id="f550f-110">Receives the number of buffered frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f550f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f550f-111">Return value</span></span>

<span data-ttu-id="f550f-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f550f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f550f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f550f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f550f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f550f-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f550f-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f550f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f550f-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f550f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f550f-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f550f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f550f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f550f-118">Requirements</span></span>



| <span data-ttu-id="f550f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f550f-119">Requirement</span></span> | <span data-ttu-id="f550f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f550f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f550f-121">Header</span><span class="sxs-lookup"><span data-stu-id="f550f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f550f-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f550f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f550f-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f550f-123">Library</span></span><br/> | <dl> <span data-ttu-id="f550f-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f550f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f550f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f550f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f550f-126">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="f550f-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="f550f-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f550f-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




