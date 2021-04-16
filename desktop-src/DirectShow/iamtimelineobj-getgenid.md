---
description: Метод Жетженид извлекает созданный идентификатор объекта. Идентификатор является зарезервированным числом; приложения не должны его использовать.
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'Метод Иамтимелинеобж:: Жетженид (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3497777d25c9a81d4334f1979ce33f351111ed4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679667"
---
# <a name="iamtimelineobjgetgenid-method"></a><span data-ttu-id="c24b9-104">Метод Иамтимелинеобж:: Жетженид</span><span class="sxs-lookup"><span data-stu-id="c24b9-104">IAMTimelineObj::GetGenID method</span></span>

> [!Note]  
> <span data-ttu-id="c24b9-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c24b9-105">\[Deprecated.</span></span> <span data-ttu-id="c24b9-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c24b9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c24b9-107">`GetGenID`Метод получает созданный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="c24b9-107">The `GetGenID` method retrieves the object's generated identifier.</span></span> <span data-ttu-id="c24b9-108">Идентификатор является зарезервированным числом; приложения не должны его использовать.</span><span class="sxs-lookup"><span data-stu-id="c24b9-108">The identifier is a reserved number; applications should not use it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c24b9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c24b9-109">Syntax</span></span>


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c24b9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c24b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c24b9-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="c24b9-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="c24b9-112">Получает созданный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c24b9-112">Receives the generated identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c24b9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c24b9-113">Return value</span></span>

<span data-ttu-id="c24b9-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c24b9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c24b9-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c24b9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c24b9-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c24b9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c24b9-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c24b9-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c24b9-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c24b9-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c24b9-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c24b9-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c24b9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c24b9-120">Requirements</span></span>



| <span data-ttu-id="c24b9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c24b9-121">Requirement</span></span> | <span data-ttu-id="c24b9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c24b9-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c24b9-123">Header</span><span class="sxs-lookup"><span data-stu-id="c24b9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c24b9-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c24b9-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c24b9-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c24b9-125">Library</span></span><br/> | <dl> <span data-ttu-id="c24b9-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c24b9-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c24b9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c24b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c24b9-128">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="c24b9-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="c24b9-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="c24b9-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




