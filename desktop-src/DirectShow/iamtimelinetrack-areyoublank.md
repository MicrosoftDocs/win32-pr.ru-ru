---
description: Метод Арэйаубланк определяет, пуста ли запись (не содержит исходных объектов).
ms.assetid: 05d02753-6e40-4307-9445-c3cbc835f75e
title: 'Метод Иамтимелинетракк:: Арэйаубланк (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.AreYouBlank
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 289fac360f989504d3eb5108f8c2388ac4a06b09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685193"
---
# <a name="iamtimelinetrackareyoublank-method"></a><span data-ttu-id="04d4c-103">Метод Иамтимелинетракк:: Арэйаубланк</span><span class="sxs-lookup"><span data-stu-id="04d4c-103">IAMTimelineTrack::AreYouBlank method</span></span>

> [!Note]  
> <span data-ttu-id="04d4c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="04d4c-104">\[Deprecated.</span></span> <span data-ttu-id="04d4c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04d4c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="04d4c-106">`AreYouBlank`Метод определяет, пуста ли данная запись (не содержит исходных объектов).</span><span class="sxs-lookup"><span data-stu-id="04d4c-106">The `AreYouBlank` method determines whether the track is blank (contains no source objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="04d4c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04d4c-107">Syntax</span></span>


```C++
HRESULT AreYouBlank(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="04d4c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="04d4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d4c-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="04d4c-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="04d4c-110">Получает логическое значение, указывающее, пуста ли запись.</span><span class="sxs-lookup"><span data-stu-id="04d4c-110">Receives a Boolean value specifying whether the track is blank.</span></span> <span data-ttu-id="04d4c-111">Если значение равно **true**, то эта запись пуста и не содержит исходных объектов.</span><span class="sxs-lookup"><span data-stu-id="04d4c-111">If the value is **TRUE**, the track is blank and contains no source objects.</span></span> <span data-ttu-id="04d4c-112">**Значение false** указывает, что запись не пуста.</span><span class="sxs-lookup"><span data-stu-id="04d4c-112">If **FALSE**, the track is not blank.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d4c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04d4c-113">Return value</span></span>

<span data-ttu-id="04d4c-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="04d4c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04d4c-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04d4c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04d4c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04d4c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="04d4c-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="04d4c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="04d4c-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="04d4c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="04d4c-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="04d4c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04d4c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="04d4c-120">Requirements</span></span>



| <span data-ttu-id="04d4c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="04d4c-121">Requirement</span></span> | <span data-ttu-id="04d4c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="04d4c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04d4c-123">Header</span><span class="sxs-lookup"><span data-stu-id="04d4c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="04d4c-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="04d4c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="04d4c-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="04d4c-125">Library</span></span><br/> | <dl> <span data-ttu-id="04d4c-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04d4c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d4c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04d4c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d4c-128">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="04d4c-128">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="04d4c-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="04d4c-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




