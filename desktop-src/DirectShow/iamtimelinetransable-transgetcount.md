---
description: Метод Трансжеткаунт извлекает количество переходов для этого объекта.
ms.assetid: f7fb4a99-c841-4680-b7f1-e4d887f12707
title: 'Метод Иамтимелинетрансабле:: Трансжеткаунт (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 81b5fc6301b319b8716a6db25fce2b1e5c2d4961
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689412"
---
# <a name="iamtimelinetransabletransgetcount-method"></a><span data-ttu-id="1b348-103">Метод Иамтимелинетрансабле:: Трансжеткаунт</span><span class="sxs-lookup"><span data-stu-id="1b348-103">IAMTimelineTransable::TransGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="1b348-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1b348-104">\[Deprecated.</span></span> <span data-ttu-id="1b348-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1b348-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1b348-106">`TransGetCount`Метод получает количество переходов для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="1b348-106">The `TransGetCount` method retrieves the number of transitions on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b348-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b348-107">Syntax</span></span>


```C++
HRESULT TransGetCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="1b348-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b348-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b348-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="1b348-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="1b348-110">Получает число переходов.</span><span class="sxs-lookup"><span data-stu-id="1b348-110">Receives the number of transitions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b348-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b348-111">Return value</span></span>

<span data-ttu-id="1b348-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1b348-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b348-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b348-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b348-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b348-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1b348-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="1b348-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1b348-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1b348-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1b348-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1b348-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1b348-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1b348-118">Requirements</span></span>



| <span data-ttu-id="1b348-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1b348-119">Requirement</span></span> | <span data-ttu-id="1b348-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1b348-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b348-121">Header</span><span class="sxs-lookup"><span data-stu-id="1b348-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1b348-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b348-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1b348-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1b348-123">Library</span></span><br/> | <dl> <span data-ttu-id="1b348-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b348-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b348-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b348-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b348-126">**Интерфейс Иамтимелинетрансабле**</span><span class="sxs-lookup"><span data-stu-id="1b348-126">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="1b348-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="1b348-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




