---
description: Метод предшествовал извлекает приоритет группы.
ms.assetid: d698317f-ace6-40ed-b125-7e2427fb683b
title: 'Метод Иамтимелинеграуп:: предшествовал (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eef0c4e0c2db439a7c593841d3aed44ab7654db7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675621"
---
# <a name="iamtimelinegroupgetpriority-method"></a><span data-ttu-id="fd570-103">Метод Иамтимелинеграуп:: предшествовал</span><span class="sxs-lookup"><span data-stu-id="fd570-103">IAMTimelineGroup::GetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="fd570-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="fd570-104">\[Deprecated.</span></span> <span data-ttu-id="fd570-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fd570-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fd570-106">`GetPriority`Метод получает приоритет группы.</span><span class="sxs-lookup"><span data-stu-id="fd570-106">The `GetPriority` method retrieves the group's priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd570-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd570-107">Syntax</span></span>


```C++
HRESULT GetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="fd570-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd570-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd570-109">*пприорити*</span><span class="sxs-lookup"><span data-stu-id="fd570-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="fd570-110">Получает приоритет группы.</span><span class="sxs-lookup"><span data-stu-id="fd570-110">Receives the group's priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd570-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd570-111">Return value</span></span>

<span data-ttu-id="fd570-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd570-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fd570-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd570-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd570-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd570-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd570-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="fd570-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fd570-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fd570-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fd570-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fd570-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd570-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fd570-118">Requirements</span></span>



| <span data-ttu-id="fd570-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fd570-119">Requirement</span></span> | <span data-ttu-id="fd570-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fd570-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd570-121">Header</span><span class="sxs-lookup"><span data-stu-id="fd570-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fd570-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd570-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fd570-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd570-123">Library</span></span><br/> | <dl> <span data-ttu-id="fd570-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd570-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd570-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd570-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd570-126">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="fd570-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="fd570-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="fd570-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




