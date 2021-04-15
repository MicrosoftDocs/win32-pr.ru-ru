---
description: Не поддерживается.
ms.assetid: 7f97b1c4-0508-45a5-a6fd-5dae17f0fa60
title: 'Метод Иамтимелинеобж:: Жетдиртиранже (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4f82b34c70cafd49bf21d662cf8b397b8d6316d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689482"
---
# <a name="iamtimelineobjgetdirtyrange-method"></a><span data-ttu-id="4f8df-103">Метод Иамтимелинеобж:: Жетдиртиранже</span><span class="sxs-lookup"><span data-stu-id="4f8df-103">IAMTimelineObj::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="4f8df-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4f8df-104">\[Deprecated.</span></span> <span data-ttu-id="4f8df-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4f8df-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4f8df-106">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4f8df-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f8df-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f8df-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="4f8df-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f8df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f8df-109">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="4f8df-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="4f8df-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4f8df-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4f8df-111">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="4f8df-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="4f8df-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4f8df-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f8df-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f8df-113">Return value</span></span>

<span data-ttu-id="4f8df-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4f8df-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f8df-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f8df-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f8df-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f8df-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f8df-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="4f8df-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4f8df-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f8df-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4f8df-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4f8df-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f8df-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4f8df-120">Requirements</span></span>



| <span data-ttu-id="4f8df-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4f8df-121">Requirement</span></span> | <span data-ttu-id="4f8df-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4f8df-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8df-123">Header</span><span class="sxs-lookup"><span data-stu-id="4f8df-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4f8df-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f8df-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4f8df-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4f8df-125">Library</span></span><br/> | <dl> <span data-ttu-id="4f8df-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f8df-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f8df-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f8df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f8df-128">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="4f8df-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




