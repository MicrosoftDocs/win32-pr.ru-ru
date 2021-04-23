---
description: Метод Сетдефаулттранситион задает переход по умолчанию. Если механизм визуализации не может визуализировать переход, он подставляет переход по умолчанию.
ms.assetid: 5ee84a12-402f-4f1c-9f08-206431c7ecdb
title: 'Метод Иамтимелине:: Сетдефаулттранситион (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeea5563ca9a2548507d3b4333d857d7cc156dd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689370"
---
# <a name="iamtimelinesetdefaulttransition-method"></a><span data-ttu-id="eb648-104">Метод Иамтимелине:: Сетдефаулттранситион</span><span class="sxs-lookup"><span data-stu-id="eb648-104">IAMTimeline::SetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="eb648-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="eb648-105">\[Deprecated.</span></span> <span data-ttu-id="eb648-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb648-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eb648-107">`SetDefaultTransition`Метод задает переход по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb648-107">The `SetDefaultTransition` method sets the default transition.</span></span> <span data-ttu-id="eb648-108">Если механизм визуализации не может визуализировать переход, он подставляет переход по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb648-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb648-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb648-109">Syntax</span></span>


```C++
HRESULT SetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="eb648-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb648-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb648-111">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="eb648-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="eb648-112">Указатель на переменную, содержащую идентификатор GUID перехода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb648-112">Pointer to a variable that contains the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb648-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb648-113">Return value</span></span>

<span data-ttu-id="eb648-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="eb648-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb648-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb648-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb648-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb648-116">Remarks</span></span>

<span data-ttu-id="eb648-117">Если вы не настроили переход по умолчанию или если переход, указанный в качестве значения по умолчанию, вызывает ошибку, DES использует собственный переход по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb648-117">If you do not set a default transition, or if the transition that you specify as a default causes an error, DES uses its own default transition.</span></span>

> [!Note]  
> <span data-ttu-id="eb648-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="eb648-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eb648-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="eb648-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eb648-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="eb648-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb648-121">Требования</span><span class="sxs-lookup"><span data-stu-id="eb648-121">Requirements</span></span>



| <span data-ttu-id="eb648-122">Требование</span><span class="sxs-lookup"><span data-stu-id="eb648-122">Requirement</span></span> | <span data-ttu-id="eb648-123">Значение</span><span class="sxs-lookup"><span data-stu-id="eb648-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb648-124">Header</span><span class="sxs-lookup"><span data-stu-id="eb648-124">Header</span></span><br/>  | <dl> <span data-ttu-id="eb648-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb648-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eb648-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb648-126">Library</span></span><br/> | <dl> <span data-ttu-id="eb648-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb648-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb648-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb648-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb648-129">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="eb648-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="eb648-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="eb648-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




