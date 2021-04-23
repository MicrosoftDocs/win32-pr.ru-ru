---
description: Метод LogError записывает ошибку в журнал. Приложениям не требуется вызывать этот метод. Он вызывается внутренним образом в ответ на ошибки отрисовки.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'Метод Иамеррорлог:: LogError (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651798"
---
# <a name="iamerrorloglogerror-method"></a><span data-ttu-id="fedf0-105">Метод Иамеррорлог:: LogError</span><span class="sxs-lookup"><span data-stu-id="fedf0-105">IAMErrorLog::LogError method</span></span>

> [!Note]  
> <span data-ttu-id="fedf0-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="fedf0-106">\[Deprecated.</span></span> <span data-ttu-id="fedf0-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fedf0-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fedf0-108">Метод **LogError** записывает ошибку в журнал.</span><span class="sxs-lookup"><span data-stu-id="fedf0-108">The **LogError** method logs an error.</span></span> <span data-ttu-id="fedf0-109">Приложениям не требуется вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="fedf0-109">Applications do not need to call this method.</span></span> <span data-ttu-id="fedf0-110">Он вызывается внутренним образом в ответ на ошибки отрисовки.</span><span class="sxs-lookup"><span data-stu-id="fedf0-110">It is called internally in response to rendering errors.</span></span>

## <a name="syntax"></a><span data-ttu-id="fedf0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fedf0-111">Syntax</span></span>


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a><span data-ttu-id="fedf0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fedf0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fedf0-113">*Уровень серьезности*</span><span class="sxs-lookup"><span data-stu-id="fedf0-113">*Severity*</span></span> 
</dt> <dd>

<span data-ttu-id="fedf0-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="fedf0-114">Reserved.</span></span> <span data-ttu-id="fedf0-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fedf0-115">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="fedf0-116">*ErrorString*</span><span class="sxs-lookup"><span data-stu-id="fedf0-116">*ErrorString*</span></span> 
</dt> <dd>

<span data-ttu-id="fedf0-117">Строковое значение, содержащее текст ошибки.</span><span class="sxs-lookup"><span data-stu-id="fedf0-117">String value containing the text of the error.</span></span>

</dd> <dt>

<span data-ttu-id="fedf0-118">*ErrorCode*</span><span class="sxs-lookup"><span data-stu-id="fedf0-118">*ErrorCode*</span></span> 
</dt> <dd>

<span data-ttu-id="fedf0-119">Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="fedf0-119">Error code.</span></span>

</dd> <dt>

<span data-ttu-id="fedf0-120">*состав*</span><span class="sxs-lookup"><span data-stu-id="fedf0-120">*hresult*</span></span> 
</dt> <dd>

<span data-ttu-id="fedf0-121">Значение HRESULT, возвращенное вызовом метода, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="fedf0-121">The HRESULT value that was returned by the method call that caused the error.</span></span>

</dd> <dt>

<span data-ttu-id="fedf0-122">*пекстраинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fedf0-122">*pExtraInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fedf0-123">Указатель на вариант, содержащий любые дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="fedf0-123">Pointer to a VARIANT that contains any additional information about the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fedf0-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fedf0-124">Return value</span></span>

<span data-ttu-id="fedf0-125">Возвращает значение параметра *HRESULT* .</span><span class="sxs-lookup"><span data-stu-id="fedf0-125">Return the value of the *hresult* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="fedf0-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fedf0-126">Remarks</span></span>

<span data-ttu-id="fedf0-127">В этом методе не следует освобождать **вариант** , на который указывает *пекстраинфо*.</span><span class="sxs-lookup"><span data-stu-id="fedf0-127">Within this method, do not free the **VARIANT** pointed to by *pExtraInfo*.</span></span> <span data-ttu-id="fedf0-128">Кроме того, **вариант** станет недопустимым после возврата метода, поэтому не пытайтесь ссылаться на него позже.</span><span class="sxs-lookup"><span data-stu-id="fedf0-128">Also, the **VARIANT** becomes invalid after the method returns, so do not try to reference it later.</span></span>

<span data-ttu-id="fedf0-129">Реализуйте этот метод, чтобы возвращать как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="fedf0-129">Implement this method to return as quickly as possible.</span></span> <span data-ttu-id="fedf0-130">Не делайте вызовы функций внутри этого метода, которые могут препятствовать выполнению программы.</span><span class="sxs-lookup"><span data-stu-id="fedf0-130">Do not make function calls from inside this method that might block program execution.</span></span> <span data-ttu-id="fedf0-131">Например, не вызывайте функции, которые отправляют сообщения в окне, блокируют события или иным образом могут блокировать выполнение.</span><span class="sxs-lookup"><span data-stu-id="fedf0-131">For example, do not call functions that send window messages, block on events, or otherwise might block execution.</span></span> <span data-ttu-id="fedf0-132">Это может привести к тому, что компьютер перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="fedf0-132">Doing so could cause the computer to stop responding.</span></span>

<span data-ttu-id="fedf0-133">Список ошибок, определенных DES, а также значение и тип данных **варианта** , на который указывает *пекстраинфо*, см. в разделе [ошибки отрисовки](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="fedf0-133">For a list of errors defined by DES, along with the meaning and data type of the **VARIANT** pointed to by *pExtraInfo*, see [Rendering Errors](rendering-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="fedf0-134">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="fedf0-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fedf0-135">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fedf0-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fedf0-136">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fedf0-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fedf0-137">Требования</span><span class="sxs-lookup"><span data-stu-id="fedf0-137">Requirements</span></span>



| <span data-ttu-id="fedf0-138">Требование</span><span class="sxs-lookup"><span data-stu-id="fedf0-138">Requirement</span></span> | <span data-ttu-id="fedf0-139">Значение</span><span class="sxs-lookup"><span data-stu-id="fedf0-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fedf0-140">Header</span><span class="sxs-lookup"><span data-stu-id="fedf0-140">Header</span></span><br/>  | <dl> <span data-ttu-id="fedf0-141"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="fedf0-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fedf0-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fedf0-142">Library</span></span><br/> | <dl> <span data-ttu-id="fedf0-143"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fedf0-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fedf0-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fedf0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fedf0-145">**Интерфейс Иамеррорлог**</span><span class="sxs-lookup"><span data-stu-id="fedf0-145">**IAMErrorLog Interface**</span></span>](iamerrorlog.md)
</dt> <dt>

[<span data-ttu-id="fedf0-146">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="fedf0-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




