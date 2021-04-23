---
description: 'Метод Сетсубобжектгуидб указывает идентификатор GUID для подобъекта, связанного с этим объектом. Этот метод эквивалентен Иамтимелинеобж:: Сетсубобжектгуид, но принимает значение BSTR.'
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: 'Метод Иамтимелинеобж:: Сетсубобжектгуидб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8df74249f061321ccd710822b8c2e0b76d5c3582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675414"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a><span data-ttu-id="f2ed8-104">Метод Иамтимелинеобж:: Сетсубобжектгуидб</span><span class="sxs-lookup"><span data-stu-id="f2ed8-104">IAMTimelineObj::SetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="f2ed8-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f2ed8-105">\[Deprecated.</span></span> <span data-ttu-id="f2ed8-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f2ed8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f2ed8-107">`SetSubObjectGUIDB`Метод указывает идентификатор GUID подобъекта, связанного с этим объектом.</span><span class="sxs-lookup"><span data-stu-id="f2ed8-107">The `SetSubObjectGUIDB` method specifies the GUID of the subobject associated with this object.</span></span> <span data-ttu-id="f2ed8-108">Этот метод эквивалентен [**иамтимелинеобж:: сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md) , но принимает значение **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="f2ed8-108">This method is equivalent to [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) but takes a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ed8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2ed8-109">Syntax</span></span>


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f2ed8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2ed8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ed8-111">*неввал*</span><span class="sxs-lookup"><span data-stu-id="f2ed8-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f2ed8-112">**BSTR** , представляющий идентификатор GUID подобъекта.</span><span class="sxs-lookup"><span data-stu-id="f2ed8-112">**BSTR** representing the GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2ed8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2ed8-113">Return value</span></span>

<span data-ttu-id="f2ed8-114">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="f2ed8-114">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ed8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2ed8-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f2ed8-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f2ed8-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f2ed8-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f2ed8-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f2ed8-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f2ed8-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2ed8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f2ed8-119">Requirements</span></span>



| <span data-ttu-id="f2ed8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f2ed8-120">Requirement</span></span> | <span data-ttu-id="f2ed8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ed8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ed8-122">Header</span><span class="sxs-lookup"><span data-stu-id="f2ed8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f2ed8-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ed8-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f2ed8-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2ed8-124">Library</span></span><br/> | <dl> <span data-ttu-id="f2ed8-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2ed8-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ed8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2ed8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ed8-127">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="f2ed8-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f2ed8-128">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f2ed8-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




