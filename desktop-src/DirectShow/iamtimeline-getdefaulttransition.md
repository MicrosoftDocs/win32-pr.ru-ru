---
description: Метод Жетдефаулттранситион извлекает переход по умолчанию. Если механизм визуализации не может визуализировать переход, он подставляет переход по умолчанию.
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: 'Метод Иамтимелине:: Жетдефаулттранситион (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652121"
---
# <a name="iamtimelinegetdefaulttransition-method"></a><span data-ttu-id="992e7-104">Метод Иамтимелине:: Жетдефаулттранситион</span><span class="sxs-lookup"><span data-stu-id="992e7-104">IAMTimeline::GetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="992e7-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="992e7-105">\[Deprecated.</span></span> <span data-ttu-id="992e7-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="992e7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="992e7-107">`GetDefaultTransition`Метод получает переход по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="992e7-107">The `GetDefaultTransition` method retrieves the default transition.</span></span> <span data-ttu-id="992e7-108">Если механизм визуализации не может визуализировать переход, он подставляет переход по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="992e7-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="992e7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="992e7-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="992e7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="992e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="992e7-111">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="992e7-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="992e7-112">Получает идентификатор GUID перехода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="992e7-112">Receives the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="992e7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="992e7-113">Return value</span></span>

<span data-ttu-id="992e7-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="992e7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="992e7-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="992e7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="992e7-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="992e7-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="992e7-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="992e7-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="992e7-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="992e7-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="992e7-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="992e7-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="992e7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="992e7-120">Requirements</span></span>



| <span data-ttu-id="992e7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="992e7-121">Requirement</span></span> | <span data-ttu-id="992e7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="992e7-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="992e7-123">Header</span><span class="sxs-lookup"><span data-stu-id="992e7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="992e7-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="992e7-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="992e7-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="992e7-125">Library</span></span><br/> | <dl> <span data-ttu-id="992e7-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="992e7-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992e7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="992e7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992e7-128">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="992e7-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="992e7-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="992e7-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




