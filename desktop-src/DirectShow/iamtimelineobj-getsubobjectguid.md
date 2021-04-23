---
description: Метод Жетсубобжектгуид извлекает идентификатор GUID для подобъекта, связанного с этим объектом временной шкалы.
ms.assetid: c2787e6b-ed72-4a6c-9e1e-c79c00020585
title: 'Метод Иамтимелинеобж:: Жетсубобжектгуид (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1c787bdbca8bbd255ccc78c3756fd0071d22f30d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688838"
---
# <a name="iamtimelineobjgetsubobjectguid-method"></a><span data-ttu-id="af449-103">Метод Иамтимелинеобж:: Жетсубобжектгуид</span><span class="sxs-lookup"><span data-stu-id="af449-103">IAMTimelineObj::GetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="af449-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="af449-104">\[Deprecated.</span></span> <span data-ttu-id="af449-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af449-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="af449-106">`GetSubObjectGUID`Метод получает идентификатор GUID подобъекта, связанного с этим объектом временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="af449-106">The `GetSubObjectGUID` method retrieves the GUID of the subobject associated with this timeline object.</span></span>

## <a name="syntax"></a><span data-ttu-id="af449-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af449-107">Syntax</span></span>


```C++
HRESULT GetSubObjectGUID(
   GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="af449-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="af449-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af449-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="af449-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="af449-110">Получает идентификатор GUID для подобъекта или GUID \_ null, если у объекта нет подобъекта.</span><span class="sxs-lookup"><span data-stu-id="af449-110">Receives the GUID of the subobject, or GUID\_NULL if the object does not have a subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af449-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af449-111">Return value</span></span>

<span data-ttu-id="af449-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="af449-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af449-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af449-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="af449-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af449-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="af449-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="af449-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="af449-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="af449-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="af449-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="af449-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="af449-118">Требования</span><span class="sxs-lookup"><span data-stu-id="af449-118">Requirements</span></span>



| <span data-ttu-id="af449-119">Требование</span><span class="sxs-lookup"><span data-stu-id="af449-119">Requirement</span></span> | <span data-ttu-id="af449-120">Значение</span><span class="sxs-lookup"><span data-stu-id="af449-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af449-121">Header</span><span class="sxs-lookup"><span data-stu-id="af449-121">Header</span></span><br/>  | <dl> <span data-ttu-id="af449-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="af449-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="af449-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="af449-123">Library</span></span><br/> | <dl> <span data-ttu-id="af449-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af449-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af449-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af449-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af449-126">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="af449-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="af449-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="af449-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




