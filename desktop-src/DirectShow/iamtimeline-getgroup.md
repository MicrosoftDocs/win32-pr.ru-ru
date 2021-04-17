---
description: Метод-Group извлекает указанную группу.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: Метод Иамтимелине::-Group (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1241a125698cf78c1138d9264ecd8c73ff78056c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675066"
---
# <a name="iamtimelinegetgroup-method"></a><span data-ttu-id="7c03a-103">Метод Иамтимелине:: Group</span><span class="sxs-lookup"><span data-stu-id="7c03a-103">IAMTimeline::GetGroup method</span></span>

> [!Note]  
> <span data-ttu-id="7c03a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7c03a-104">\[Deprecated.</span></span> <span data-ttu-id="7c03a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c03a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7c03a-106">`GetGroup`Метод извлекает указанную группу.</span><span class="sxs-lookup"><span data-stu-id="7c03a-106">The `GetGroup` method retrieves a specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c03a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c03a-107">Syntax</span></span>


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a><span data-ttu-id="7c03a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c03a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c03a-109">*ппграуп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7c03a-109">*ppGroup* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c03a-110">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) группы.</span><span class="sxs-lookup"><span data-stu-id="7c03a-110">Receives a pointer to the group's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7c03a-111">*вхичграуп*</span><span class="sxs-lookup"><span data-stu-id="7c03a-111">*WhichGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="7c03a-112">Индекс извлекаемой группы в зависимости от порядка добавления групп на временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="7c03a-112">Index of the group to retrieve, based on the order in which the groups were added to the timeline.</span></span> <span data-ttu-id="7c03a-113">Первая группа, добавленная на временную шкалу, имеет индекс 0.</span><span class="sxs-lookup"><span data-stu-id="7c03a-113">The first group added to the timeline has an index of 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c03a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c03a-114">Return value</span></span>

<span data-ttu-id="7c03a-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7c03a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7c03a-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7c03a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c03a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c03a-117">Remarks</span></span>

<span data-ttu-id="7c03a-118">Если метод завершается успешно, интерфейс **иамтимелинеобж** , который он возвращает, имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="7c03a-118">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="7c03a-119">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="7c03a-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="7c03a-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="7c03a-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7c03a-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c03a-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7c03a-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7c03a-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7c03a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7c03a-123">Requirements</span></span>



| <span data-ttu-id="7c03a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7c03a-124">Requirement</span></span> | <span data-ttu-id="7c03a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7c03a-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c03a-126">Header</span><span class="sxs-lookup"><span data-stu-id="7c03a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7c03a-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c03a-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7c03a-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c03a-128">Library</span></span><br/> | <dl> <span data-ttu-id="7c03a-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c03a-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c03a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c03a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c03a-131">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="7c03a-131">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="7c03a-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="7c03a-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




