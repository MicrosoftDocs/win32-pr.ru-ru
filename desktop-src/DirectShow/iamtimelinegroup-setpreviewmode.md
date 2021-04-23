---
description: Метод Сетпревиевмоде задает режим предварительного просмотра для группы.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: 'Метод Иамтимелинеграуп:: Сетпревиевмоде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe03e6be3572b6cc660e51c27551a316db990d80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689211"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a><span data-ttu-id="d923c-103">Метод Иамтимелинеграуп:: Сетпревиевмоде</span><span class="sxs-lookup"><span data-stu-id="d923c-103">IAMTimelineGroup::SetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="d923c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d923c-104">\[Deprecated.</span></span> <span data-ttu-id="d923c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d923c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d923c-106">Метод Сетпревиевмоде задает режим предварительного просмотра для группы.</span><span class="sxs-lookup"><span data-stu-id="d923c-106">The SetPreviewMode method sets the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d923c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d923c-107">Syntax</span></span>


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a><span data-ttu-id="d923c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d923c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d923c-109">*фпревиев*</span><span class="sxs-lookup"><span data-stu-id="d923c-109">*fPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="d923c-110">Режим предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="d923c-110">The preview mode.</span></span> <span data-ttu-id="d923c-111">Если **значение — true**, группа находится в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="d923c-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="d923c-112">Если задано **значение false**, группа находится в режиме разработки.</span><span class="sxs-lookup"><span data-stu-id="d923c-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d923c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d923c-113">Return value</span></span>

<span data-ttu-id="d923c-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d923c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d923c-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d923c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d923c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d923c-116">Remarks</span></span>

<span data-ttu-id="d923c-117">В режиме предварительного просмотра фреймы удаляются во время незначительного эффекта или переходов для синхронизации видео с аудио.</span><span class="sxs-lookup"><span data-stu-id="d923c-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="d923c-118">В результате видео может выглядеть прерывисто.</span><span class="sxs-lookup"><span data-stu-id="d923c-118">The video might look choppy as a result.</span></span> <span data-ttu-id="d923c-119">В режиме разработки отображается каждый кадр.</span><span class="sxs-lookup"><span data-stu-id="d923c-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="d923c-120">Режим разработки подходит для записи файлов. При предварительном просмотре видео может быть не синхронизировано с звуковым экраном.</span><span class="sxs-lookup"><span data-stu-id="d923c-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might be out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="d923c-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d923c-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d923c-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d923c-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d923c-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d923c-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d923c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d923c-124">Requirements</span></span>



| <span data-ttu-id="d923c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d923c-125">Requirement</span></span> | <span data-ttu-id="d923c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d923c-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d923c-127">Header</span><span class="sxs-lookup"><span data-stu-id="d923c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d923c-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d923c-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d923c-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d923c-129">Library</span></span><br/> | <dl> <span data-ttu-id="d923c-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d923c-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d923c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d923c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d923c-132">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="d923c-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="d923c-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="d923c-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




