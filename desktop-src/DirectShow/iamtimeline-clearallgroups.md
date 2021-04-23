---
description: Метод Клеараллграупс удаляет все группы из временной шкалы, а также все объекты, содержащиеся в этих группах.
ms.assetid: b0d2a463-bd18-4377-893c-ea4fdf77b1c8
title: 'Метод Иамтимелине:: Клеараллграупс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ClearAllGroups
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 05d847bdae9d6f5f5672d555a31505c2739af41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651792"
---
# <a name="iamtimelineclearallgroups-method"></a><span data-ttu-id="c276c-103">Метод Иамтимелине:: Клеараллграупс</span><span class="sxs-lookup"><span data-stu-id="c276c-103">IAMTimeline::ClearAllGroups method</span></span>

> [!Note]  
> <span data-ttu-id="c276c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c276c-104">\[Deprecated.</span></span> <span data-ttu-id="c276c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c276c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c276c-106">`ClearAllGroups`Метод удаляет все группы из временной шкалы, а также все объекты, содержащиеся в этих группах.</span><span class="sxs-lookup"><span data-stu-id="c276c-106">The `ClearAllGroups` method removes all groups from the timeline, along with all objects contained in those groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="c276c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c276c-107">Syntax</span></span>


```C++
HRESULT ClearAllGroups();
```



## <a name="parameters"></a><span data-ttu-id="c276c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c276c-108">Parameters</span></span>

<span data-ttu-id="c276c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c276c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c276c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c276c-110">Return value</span></span>

<span data-ttu-id="c276c-111">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c276c-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c276c-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c276c-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c276c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c276c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c276c-114">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c276c-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c276c-115">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c276c-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c276c-116">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c276c-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c276c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c276c-117">Requirements</span></span>



| <span data-ttu-id="c276c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c276c-118">Requirement</span></span> | <span data-ttu-id="c276c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c276c-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c276c-120">Header</span><span class="sxs-lookup"><span data-stu-id="c276c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c276c-121"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c276c-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c276c-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c276c-122">Library</span></span><br/> | <dl> <span data-ttu-id="c276c-123"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c276c-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c276c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c276c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c276c-125">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="c276c-125">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="c276c-126">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="c276c-126">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




