---
description: Метод RemoveAll окончательно удаляет этот объект из временной шкалы, включая подобъекты и дочерние объекты.
ms.assetid: 9596cf47-63fe-4839-a6d5-3685fc91a935
title: 'Метод Иамтимелинеобж:: RemoveAll (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.RemoveAll
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1888b89773253285036c89e20332d92555b6db2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676043"
---
# <a name="iamtimelineobjremoveall-method"></a><span data-ttu-id="5fff0-103">Метод Иамтимелинеобж:: RemoveAll</span><span class="sxs-lookup"><span data-stu-id="5fff0-103">IAMTimelineObj::RemoveAll method</span></span>

> [!Note]  
> <span data-ttu-id="5fff0-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5fff0-104">\[Deprecated.</span></span> <span data-ttu-id="5fff0-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5fff0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5fff0-106">`RemoveAll`Метод окончательно удаляет этот объект из временной шкалы, включая подобъекты и дочерние объекты.</span><span class="sxs-lookup"><span data-stu-id="5fff0-106">The `RemoveAll` method permanently removes this object from the timeline, including subobjects and children.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fff0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fff0-107">Syntax</span></span>


```C++
HRESULT RemoveAll();
```



## <a name="parameters"></a><span data-ttu-id="5fff0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fff0-108">Parameters</span></span>

<span data-ttu-id="5fff0-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5fff0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5fff0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fff0-110">Return value</span></span>

<span data-ttu-id="5fff0-111">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5fff0-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5fff0-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5fff0-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fff0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fff0-113">Remarks</span></span>

<span data-ttu-id="5fff0-114">Чтобы удалить объект с целью его повторного добавления в другое место на временной шкале, вызовите метод [**иамтимелинеобж:: reinsert**](iamtimelineobj-remove.md).</span><span class="sxs-lookup"><span data-stu-id="5fff0-114">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md).</span></span>

> [!Note]  
> <span data-ttu-id="5fff0-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="5fff0-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5fff0-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5fff0-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5fff0-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5fff0-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5fff0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5fff0-118">Requirements</span></span>



| <span data-ttu-id="5fff0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5fff0-119">Requirement</span></span> | <span data-ttu-id="5fff0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5fff0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fff0-121">Header</span><span class="sxs-lookup"><span data-stu-id="5fff0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5fff0-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fff0-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5fff0-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5fff0-123">Library</span></span><br/> | <dl> <span data-ttu-id="5fff0-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fff0-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fff0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fff0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fff0-126">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="5fff0-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="5fff0-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="5fff0-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




