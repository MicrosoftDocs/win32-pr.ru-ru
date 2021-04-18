---
description: Метод AddGroup добавляет группу на временную шкалу.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'Метод Иамтимелине:: AddGroup (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675293"
---
# <a name="iamtimelineaddgroup-method"></a><span data-ttu-id="9ca63-103">Метод Иамтимелине:: AddGroup</span><span class="sxs-lookup"><span data-stu-id="9ca63-103">IAMTimeline::AddGroup method</span></span>

> [!Note]  
> <span data-ttu-id="9ca63-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9ca63-104">\[Deprecated.</span></span> <span data-ttu-id="9ca63-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ca63-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ca63-106">`AddGroup`Метод добавляет группу на временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="9ca63-106">The `AddGroup` method adds a group to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca63-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ca63-107">Syntax</span></span>


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="9ca63-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ca63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ca63-109">*пграуп*</span><span class="sxs-lookup"><span data-stu-id="9ca63-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="9ca63-110">Указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) группы.</span><span class="sxs-lookup"><span data-stu-id="9ca63-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ca63-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ca63-111">Return value</span></span>

<span data-ttu-id="9ca63-112">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="9ca63-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="9ca63-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9ca63-113">Return code</span></span>                                                                                   | <span data-ttu-id="9ca63-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9ca63-114">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="9ca63-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9ca63-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9ca63-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="9ca63-116">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="9ca63-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9ca63-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9ca63-118">Превышено максимальное число групп.</span><span class="sxs-lookup"><span data-stu-id="9ca63-118">Maximum number of groups exceeded.</span></span><br/> |
| <dl> <span data-ttu-id="9ca63-119"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="9ca63-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="9ca63-120">Объект не является группой.</span><span class="sxs-lookup"><span data-stu-id="9ca63-120">The object is not a group.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="9ca63-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ca63-121">Remarks</span></span>

<span data-ttu-id="9ca63-122">Сейчас шкала времени поддерживает не более 32 групп.</span><span class="sxs-lookup"><span data-stu-id="9ca63-122">Currently, timelines support a maximum of 32 groups.</span></span>

> [!Note]  
> <span data-ttu-id="9ca63-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="9ca63-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9ca63-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ca63-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9ca63-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9ca63-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ca63-126">Требования</span><span class="sxs-lookup"><span data-stu-id="9ca63-126">Requirements</span></span>



| <span data-ttu-id="9ca63-127">Требование</span><span class="sxs-lookup"><span data-stu-id="9ca63-127">Requirement</span></span> | <span data-ttu-id="9ca63-128">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca63-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca63-129">Header</span><span class="sxs-lookup"><span data-stu-id="9ca63-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9ca63-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ca63-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9ca63-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9ca63-131">Library</span></span><br/> | <dl> <span data-ttu-id="9ca63-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ca63-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca63-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ca63-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca63-134">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="9ca63-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="9ca63-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="9ca63-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




