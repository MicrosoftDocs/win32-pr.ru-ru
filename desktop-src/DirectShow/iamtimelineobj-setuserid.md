---
description: Метод Сетусерид задает определяемый приложением идентификатор для объекта.
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: 'Метод Иамтимелинеобж:: Сетусерид (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 31a0c59c6c93535be1200b2cd7678d4c355b5bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689137"
---
# <a name="iamtimelineobjsetuserid-method"></a><span data-ttu-id="d6b7e-103">Метод Иамтимелинеобж:: Сетусерид</span><span class="sxs-lookup"><span data-stu-id="d6b7e-103">IAMTimelineObj::SetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="d6b7e-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-104">\[Deprecated.</span></span> <span data-ttu-id="d6b7e-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d6b7e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d6b7e-106">`SetUserID`Метод задает определяемый приложением идентификатор для объекта.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-106">The `SetUserID` method sets an application-defined identifier for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b7e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6b7e-107">Syntax</span></span>


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d6b7e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6b7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6b7e-109">*неввал*</span><span class="sxs-lookup"><span data-stu-id="d6b7e-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d6b7e-110">Значение, указывающее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-110">Value that specifies the identifier.</span></span> <span data-ttu-id="d6b7e-111">Этот идентификатор используется только приложением и может принимать любое значение.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-111">This identifier is used only by the application and can be any value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6b7e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6b7e-112">Return value</span></span>

<span data-ttu-id="d6b7e-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6b7e-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6b7e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6b7e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6b7e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6b7e-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d6b7e-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d6b7e-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6b7e-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d6b7e-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d6b7e-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d6b7e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d6b7e-119">Requirements</span></span>



| <span data-ttu-id="d6b7e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d6b7e-120">Requirement</span></span> | <span data-ttu-id="d6b7e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d6b7e-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b7e-122">Header</span><span class="sxs-lookup"><span data-stu-id="d6b7e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d6b7e-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6b7e-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d6b7e-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d6b7e-124">Library</span></span><br/> | <dl> <span data-ttu-id="d6b7e-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6b7e-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6b7e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6b7e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b7e-127">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="d6b7e-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="d6b7e-128">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="d6b7e-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




