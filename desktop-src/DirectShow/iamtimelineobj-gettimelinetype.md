---
description: Метод Жеттимелинетипе Извлекает тип объекта.
ms.assetid: db46457f-25d0-4421-af73-426d65b720d3
title: 'Метод Иамтимелинеобж:: Жеттимелинетипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76b9c2a847cc0d0150b21062810290aaaab702cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685049"
---
# <a name="iamtimelineobjgettimelinetype-method"></a><span data-ttu-id="8a575-103">Метод Иамтимелинеобж:: Жеттимелинетипе</span><span class="sxs-lookup"><span data-stu-id="8a575-103">IAMTimelineObj::GetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="8a575-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8a575-104">\[Deprecated.</span></span> <span data-ttu-id="8a575-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8a575-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8a575-106">`GetTimelineType`Метод получает тип объекта.</span><span class="sxs-lookup"><span data-stu-id="8a575-106">The `GetTimelineType` method retrieves the object's type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a575-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a575-107">Syntax</span></span>


```C++
HRESULT GetTimelineType(
   TIMELINE_MAJOR_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8a575-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a575-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a575-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="8a575-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="8a575-110">Получает элемент типа "перечислимый тип [**временной шкалы \_ \_**](timeline-major-type.md) ", указывающий тип объекта.</span><span class="sxs-lookup"><span data-stu-id="8a575-110">Receives a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, indicating the type of object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a575-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a575-111">Return value</span></span>

<span data-ttu-id="8a575-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8a575-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a575-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a575-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a575-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a575-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8a575-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="8a575-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8a575-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a575-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8a575-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8a575-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a575-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8a575-118">Requirements</span></span>



| <span data-ttu-id="8a575-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8a575-119">Requirement</span></span> | <span data-ttu-id="8a575-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8a575-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a575-121">Header</span><span class="sxs-lookup"><span data-stu-id="8a575-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8a575-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a575-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8a575-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a575-123">Library</span></span><br/> | <dl> <span data-ttu-id="8a575-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a575-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a575-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a575-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a575-126">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="8a575-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="8a575-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="8a575-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




