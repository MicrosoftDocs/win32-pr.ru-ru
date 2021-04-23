---
description: Метод GetObject извлекает определяемый приложением идентификатор.
ms.assetid: 68a20dfa-990e-47de-ae02-1d3182b7f13f
title: Метод Иамтимелинеобж::-UserID (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f5d6c07fd826f2045ddc9f54445bc96feb5a7c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685048"
---
# <a name="iamtimelineobjgetuserid-method"></a><span data-ttu-id="76e7f-103">Метод Иамтимелинеобж::</span><span class="sxs-lookup"><span data-stu-id="76e7f-103">IAMTimelineObj::GetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="76e7f-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="76e7f-104">\[Deprecated.</span></span> <span data-ttu-id="76e7f-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="76e7f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="76e7f-106">`GetUserID`Метод получает определяемый приложением идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="76e7f-106">The `GetUserID` method retrieves the object's application-defined identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="76e7f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76e7f-107">Syntax</span></span>


```C++
HRESULT GetUserID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="76e7f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="76e7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76e7f-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="76e7f-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="76e7f-110">Получает определяемый приложением идентификатор.</span><span class="sxs-lookup"><span data-stu-id="76e7f-110">Receives the application-defined identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76e7f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76e7f-111">Return value</span></span>

<span data-ttu-id="76e7f-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="76e7f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76e7f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76e7f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="76e7f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76e7f-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="76e7f-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="76e7f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="76e7f-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="76e7f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="76e7f-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="76e7f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="76e7f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="76e7f-118">Requirements</span></span>



| <span data-ttu-id="76e7f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="76e7f-119">Requirement</span></span> | <span data-ttu-id="76e7f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="76e7f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76e7f-121">Header</span><span class="sxs-lookup"><span data-stu-id="76e7f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="76e7f-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="76e7f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="76e7f-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="76e7f-123">Library</span></span><br/> | <dl> <span data-ttu-id="76e7f-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76e7f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76e7f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76e7f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76e7f-126">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="76e7f-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="76e7f-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="76e7f-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




