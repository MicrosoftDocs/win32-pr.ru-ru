---
description: Метод Сетсубобжектгуид указывает идентификатор GUID для подобъекта, связанного с этим объектом.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'Метод Иамтимелинеобж:: Сетсубобжектгуид (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689139"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a><span data-ttu-id="51e44-103">Метод Иамтимелинеобж:: Сетсубобжектгуид</span><span class="sxs-lookup"><span data-stu-id="51e44-103">IAMTimelineObj::SetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="51e44-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="51e44-104">\[Deprecated.</span></span> <span data-ttu-id="51e44-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51e44-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="51e44-106">`SetSubObjectGUID`Метод указывает идентификатор GUID подобъекта, связанного с этим объектом.</span><span class="sxs-lookup"><span data-stu-id="51e44-106">The `SetSubObjectGUID` method specifies the GUID of the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e44-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51e44-107">Syntax</span></span>


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a><span data-ttu-id="51e44-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="51e44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e44-109">*неввал*</span><span class="sxs-lookup"><span data-stu-id="51e44-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="51e44-110">Идентификатор GUID подобъекта.</span><span class="sxs-lookup"><span data-stu-id="51e44-110">GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e44-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51e44-111">Return value</span></span>

<span data-ttu-id="51e44-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="51e44-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51e44-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51e44-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e44-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51e44-114">Remarks</span></span>

<span data-ttu-id="51e44-115">Подсистема визуализации создает экземпляр подобъекта по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="51e44-115">The render engine creates an instance of the subobject as needed.</span></span>

> [!Note]  
> <span data-ttu-id="51e44-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="51e44-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="51e44-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="51e44-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="51e44-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="51e44-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51e44-119">Требования</span><span class="sxs-lookup"><span data-stu-id="51e44-119">Requirements</span></span>



| <span data-ttu-id="51e44-120">Требование</span><span class="sxs-lookup"><span data-stu-id="51e44-120">Requirement</span></span> | <span data-ttu-id="51e44-121">Значение</span><span class="sxs-lookup"><span data-stu-id="51e44-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51e44-122">Header</span><span class="sxs-lookup"><span data-stu-id="51e44-122">Header</span></span><br/>  | <dl> <span data-ttu-id="51e44-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="51e44-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="51e44-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="51e44-124">Library</span></span><br/> | <dl> <span data-ttu-id="51e44-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51e44-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e44-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51e44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e44-127">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="51e44-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="51e44-128">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="51e44-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




