---
description: Метод Сетмутед задает состояние отключения объекта. Отключенный объект не готовится к просмотру, но остается на временной шкале.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'Метод Иамтимелинеобж:: Сетмутед (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676040"
---
# <a name="iamtimelineobjsetmuted-method"></a><span data-ttu-id="be5fd-104">Метод Иамтимелинеобж:: Сетмутед</span><span class="sxs-lookup"><span data-stu-id="be5fd-104">IAMTimelineObj::SetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="be5fd-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="be5fd-105">\[Deprecated.</span></span> <span data-ttu-id="be5fd-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="be5fd-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="be5fd-107">`SetMuted`Метод задает состояние отключения объекта.</span><span class="sxs-lookup"><span data-stu-id="be5fd-107">The `SetMuted` method sets the object's muted state.</span></span> <span data-ttu-id="be5fd-108">Отключенный объект не готовится к просмотру, но остается на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="be5fd-108">A muted object is not rendered, but it remains in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="be5fd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be5fd-109">Syntax</span></span>


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="be5fd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="be5fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be5fd-111">*неввал*</span><span class="sxs-lookup"><span data-stu-id="be5fd-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="be5fd-112">Флаг, указывающий состояние отключения.</span><span class="sxs-lookup"><span data-stu-id="be5fd-112">Flag that specifies the muted state.</span></span> <span data-ttu-id="be5fd-113">Если **значение — true**, объект и все его дочерние элементы будут отключены.</span><span class="sxs-lookup"><span data-stu-id="be5fd-113">If **TRUE**, the object and all of its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be5fd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be5fd-114">Return value</span></span>

<span data-ttu-id="be5fd-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="be5fd-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be5fd-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be5fd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be5fd-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be5fd-117">Remarks</span></span>

<span data-ttu-id="be5fd-118">При отключении звука объект также выключает все дочерние элементы, содержащиеся в объекте.</span><span class="sxs-lookup"><span data-stu-id="be5fd-118">Muting an object also mutes any children contained in the object.</span></span> <span data-ttu-id="be5fd-119">Например, если выключить трассировку, то переходы, источники и эффекты в этой дорожке также будут отключены.</span><span class="sxs-lookup"><span data-stu-id="be5fd-119">For example, if you mute a track, the transitions, sources, and effects in that track are also muted.</span></span> <span data-ttu-id="be5fd-120">После того как объект больше не будет отключен, его дочерние элементы возвращаются к предыдущему состоянию, которое может быть отключено или отключено.</span><span class="sxs-lookup"><span data-stu-id="be5fd-120">Once the object is no longer muted, its children revert to their previous state, which might be muted or unmuted.</span></span>

> [!Note]  
> <span data-ttu-id="be5fd-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="be5fd-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="be5fd-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="be5fd-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="be5fd-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="be5fd-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="be5fd-124">Требования</span><span class="sxs-lookup"><span data-stu-id="be5fd-124">Requirements</span></span>



| <span data-ttu-id="be5fd-125">Требование</span><span class="sxs-lookup"><span data-stu-id="be5fd-125">Requirement</span></span> | <span data-ttu-id="be5fd-126">Значение</span><span class="sxs-lookup"><span data-stu-id="be5fd-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be5fd-127">Header</span><span class="sxs-lookup"><span data-stu-id="be5fd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="be5fd-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="be5fd-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="be5fd-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be5fd-129">Library</span></span><br/> | <dl> <span data-ttu-id="be5fd-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be5fd-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be5fd-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be5fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be5fd-132">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="be5fd-132">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="be5fd-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="be5fd-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




