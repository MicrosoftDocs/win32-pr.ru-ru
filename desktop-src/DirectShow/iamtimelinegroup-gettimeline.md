---
description: Метод метода Timeline извлекает временную шкалу, к которой принадлежит эта группа.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: Метод Иамтимелинеграуп::-Timeline (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675618"
---
# <a name="iamtimelinegroupgettimeline-method"></a><span data-ttu-id="f6a77-103">Метод Иамтимелинеграуп:: with Timeline</span><span class="sxs-lookup"><span data-stu-id="f6a77-103">IAMTimelineGroup::GetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="f6a77-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f6a77-104">\[Deprecated.</span></span> <span data-ttu-id="f6a77-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6a77-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f6a77-106">`GetTimeline`Метод извлекает временную шкалу, к которой принадлежит эта группа.</span><span class="sxs-lookup"><span data-stu-id="f6a77-106">The `GetTimeline` method retrieves the timeline to which this group belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a77-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6a77-107">Syntax</span></span>


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="f6a77-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6a77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a77-109">*пптимелине* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f6a77-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a77-110">Получает интерфейс [**иамтимелине**](iamtimeline.md) временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="f6a77-110">Receives the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="f6a77-111">Если группа не является частью временной шкалы, для нее устанавливается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f6a77-111">If the group is not part of a timeline, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a77-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6a77-112">Return value</span></span>

<span data-ttu-id="f6a77-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f6a77-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6a77-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6a77-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6a77-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6a77-115">Remarks</span></span>

<span data-ttu-id="f6a77-116">Если значение, возвращаемое в *пптимелине* , не равно **null**, то интерфейс **иамтимелине** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="f6a77-116">If the value returned in *ppTimeline* is not **NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="f6a77-117">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="f6a77-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="f6a77-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f6a77-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f6a77-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6a77-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f6a77-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f6a77-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f6a77-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f6a77-121">Requirements</span></span>



| <span data-ttu-id="f6a77-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f6a77-122">Requirement</span></span> | <span data-ttu-id="f6a77-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f6a77-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a77-124">Header</span><span class="sxs-lookup"><span data-stu-id="f6a77-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f6a77-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6a77-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f6a77-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6a77-126">Library</span></span><br/> | <dl> <span data-ttu-id="f6a77-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6a77-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6a77-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6a77-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6a77-129">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="f6a77-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="f6a77-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f6a77-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




