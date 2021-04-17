---
description: Метод Жетнекствтракк извлекает следующую виртуальную запись после указанной виртуальной записи.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'Метод Иамтимелинекомп:: Жетнекствтракк (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679790"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a><span data-ttu-id="95c10-103">Метод Иамтимелинекомп:: Жетнекствтракк</span><span class="sxs-lookup"><span data-stu-id="95c10-103">IAMTimelineComp::GetNextVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="95c10-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="95c10-104">\[Deprecated.</span></span> <span data-ttu-id="95c10-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="95c10-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="95c10-106">`GetNextVTrack`Метод извлекает следующую виртуальную запись после указанной виртуальной записи.</span><span class="sxs-lookup"><span data-stu-id="95c10-106">The `GetNextVTrack` method retrieves the next virtual track after a specified virtual track.</span></span>

## <a name="syntax"></a><span data-ttu-id="95c10-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95c10-107">Syntax</span></span>


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a><span data-ttu-id="95c10-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95c10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c10-109">*пвиртуалтракк*</span><span class="sxs-lookup"><span data-stu-id="95c10-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="95c10-110">Указатель на предыдущую виртуальную дорожку или **значение NULL** , чтобы получить первую виртуальную дорожку в композиции.</span><span class="sxs-lookup"><span data-stu-id="95c10-110">Pointer to the previous virtual track, or **NULL** to retrieve the first virtual track in the composition.</span></span>

</dd> <dt>

<span data-ttu-id="95c10-111">*ппнекствиртуалтракк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95c10-111">*ppNextVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95c10-112">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) следующей виртуальной записи в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="95c10-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the next virtual track, in order of priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c10-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95c10-113">Return value</span></span>

<span data-ttu-id="95c10-114">Возвращает \_ значение ОК, если метод получает виртуальную дорожку, или \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="95c10-114">Returns S\_OK if the method retrieves a virtual track, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="95c10-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95c10-115">Remarks</span></span>

<span data-ttu-id="95c10-116">Если метод завершается успешно, интерфейс **иамтимелинеобж** , который он возвращает, имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="95c10-116">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="95c10-117">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="95c10-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="95c10-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="95c10-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="95c10-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="95c10-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="95c10-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="95c10-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95c10-121">Требования</span><span class="sxs-lookup"><span data-stu-id="95c10-121">Requirements</span></span>



| <span data-ttu-id="95c10-122">Требование</span><span class="sxs-lookup"><span data-stu-id="95c10-122">Requirement</span></span> | <span data-ttu-id="95c10-123">Значение</span><span class="sxs-lookup"><span data-stu-id="95c10-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95c10-124">Header</span><span class="sxs-lookup"><span data-stu-id="95c10-124">Header</span></span><br/>  | <dl> <span data-ttu-id="95c10-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="95c10-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="95c10-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95c10-126">Library</span></span><br/> | <dl> <span data-ttu-id="95c10-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95c10-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95c10-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95c10-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c10-129">**Интерфейс Иамтимелинекомп**</span><span class="sxs-lookup"><span data-stu-id="95c10-129">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="95c10-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="95c10-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




