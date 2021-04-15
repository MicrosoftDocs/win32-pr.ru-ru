---
description: Метод Втраккжеткаунт Извлекает число виртуальных дорожек, содержащихся в композиции.
ms.assetid: a8117b06-4f42-45da-9b93-f547cb70aa5d
title: 'Метод Иамтимелинекомп:: Втраккжеткаунт (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 36800381ce50ea60d5252841d9731b2657fc22cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689260"
---
# <a name="iamtimelinecompvtrackgetcount-method"></a><span data-ttu-id="e5df7-103">Метод Иамтимелинекомп:: Втраккжеткаунт</span><span class="sxs-lookup"><span data-stu-id="e5df7-103">IAMTimelineComp::VTrackGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="e5df7-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e5df7-104">\[Deprecated.</span></span> <span data-ttu-id="e5df7-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e5df7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e5df7-106">`VTrackGetCount`Метод извлекает число виртуальных дорожек, содержащихся в композиции.</span><span class="sxs-lookup"><span data-stu-id="e5df7-106">The `VTrackGetCount` method retrieves the number of virtual tracks contained in the composition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5df7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5df7-107">Syntax</span></span>


```C++
HRESULT VTrackGetCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e5df7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5df7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5df7-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="e5df7-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e5df7-110">Получает число виртуальных дорожек.</span><span class="sxs-lookup"><span data-stu-id="e5df7-110">Receives the number of virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5df7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5df7-111">Return value</span></span>

<span data-ttu-id="e5df7-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e5df7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e5df7-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e5df7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5df7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5df7-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e5df7-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="e5df7-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e5df7-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e5df7-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e5df7-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e5df7-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5df7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e5df7-118">Requirements</span></span>



| <span data-ttu-id="e5df7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e5df7-119">Requirement</span></span> | <span data-ttu-id="e5df7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e5df7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5df7-121">Header</span><span class="sxs-lookup"><span data-stu-id="e5df7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e5df7-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5df7-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e5df7-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5df7-123">Library</span></span><br/> | <dl> <span data-ttu-id="e5df7-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5df7-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5df7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5df7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5df7-126">**Интерфейс Иамтимелинекомп**</span><span class="sxs-lookup"><span data-stu-id="e5df7-126">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="e5df7-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="e5df7-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




