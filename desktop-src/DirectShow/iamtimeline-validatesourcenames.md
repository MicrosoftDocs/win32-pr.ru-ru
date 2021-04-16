---
description: Метод Валидатесаурценамес проверяет имена источников на временной шкале с помощью указателя мультимедиа. При необходимости этот метод также обновляет любой исходный объект, для которого он находит файл.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'Метод Иамтимелине:: Валидатесаурценамес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689037"
---
# <a name="iamtimelinevalidatesourcenames-method"></a><span data-ttu-id="46527-104">Метод Иамтимелине:: Валидатесаурценамес</span><span class="sxs-lookup"><span data-stu-id="46527-104">IAMTimeline::ValidateSourceNames method</span></span>

> [!Note]  
> <span data-ttu-id="46527-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="46527-105">\[Deprecated.</span></span> <span data-ttu-id="46527-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46527-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="46527-107">`ValidateSourceNames`Метод проверяет имена источников на временной шкале с помощью указателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="46527-107">The `ValidateSourceNames` method validates source names in the timeline, using the media locator.</span></span> <span data-ttu-id="46527-108">При необходимости этот метод также обновляет любой исходный объект, для которого он находит файл.</span><span class="sxs-lookup"><span data-stu-id="46527-108">Optionally, this method also updates any source object for which it locates a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="46527-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46527-109">Syntax</span></span>


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a><span data-ttu-id="46527-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="46527-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46527-111">*валидатефлагс*</span><span class="sxs-lookup"><span data-stu-id="46527-111">*ValidateFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="46527-112">Побитовое сочетание [**флагов проверки имени файла**](file-name-validation-flags.md) , определяющее поведение указателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="46527-112">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="46527-113">\_ \_ \_ Должны присутствовать флаги проверки СФН валидатеф Replace и СФН валидатеф \_ , или метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="46527-113">The SFN\_VALIDATEF\_REPLACE and SFN\_VALIDATEF\_CHECK flags must be present, or the method returns E\_INVALIDARG.</span></span>

</dd> <dt>

<span data-ttu-id="46527-114">*поверриде*</span><span class="sxs-lookup"><span data-stu-id="46527-114">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="46527-115">Необязательный указатель на интерфейс [**имедиалокатор**](imedialocator.md) указателя мультимедиа, используемый вместо значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46527-115">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="46527-116">Чтобы использовать указатель носителя по умолчанию, установите для этого параметра значение **null**.</span><span class="sxs-lookup"><span data-stu-id="46527-116">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="46527-117">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="46527-117">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="46527-118">*нотифевенсандле*</span><span class="sxs-lookup"><span data-stu-id="46527-118">*NotifyEventHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="46527-119">Дескриптор события.</span><span class="sxs-lookup"><span data-stu-id="46527-119">Handle to an event.</span></span> <span data-ttu-id="46527-120">Метод сигнализирует о событии после завершения проверки.</span><span class="sxs-lookup"><span data-stu-id="46527-120">The method signals the event after it has completed the validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46527-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46527-121">Return value</span></span>

<span data-ttu-id="46527-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="46527-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46527-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46527-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46527-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46527-124">Remarks</span></span>

<span data-ttu-id="46527-125">С помощью параметра *поверриде* можно предоставить собственную пользовательскую реализацию интерфейса [**имедиалокатор**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="46527-125">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="46527-126">Например, указатель мультимедиа по умолчанию не будет уведомлять приложение о найденных файлах (или не может найти их).</span><span class="sxs-lookup"><span data-stu-id="46527-126">For example, the default media locator will not notify your application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="46527-127">Чтобы обойти это ограничение, можно реализовать пользовательский указатель мультимедиа, сделав его оболочкой для версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46527-127">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="46527-128">В пользовательской версии передайте [**имедиалокатор:: финдмедиафиле**](imedialocator-findmediafile.md) напрямую вызовет версию по умолчанию и изучите возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="46527-128">In your custom version, pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version, and examine the return value.</span></span>

> [!Note]  
> <span data-ttu-id="46527-129">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="46527-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="46527-130">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="46527-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="46527-131">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="46527-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46527-132">Требования</span><span class="sxs-lookup"><span data-stu-id="46527-132">Requirements</span></span>



| <span data-ttu-id="46527-133">Требование</span><span class="sxs-lookup"><span data-stu-id="46527-133">Requirement</span></span> | <span data-ttu-id="46527-134">Значение</span><span class="sxs-lookup"><span data-stu-id="46527-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46527-135">Header</span><span class="sxs-lookup"><span data-stu-id="46527-135">Header</span></span><br/>  | <dl> <span data-ttu-id="46527-136"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="46527-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="46527-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46527-137">Library</span></span><br/> | <dl> <span data-ttu-id="46527-138"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46527-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46527-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46527-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46527-140">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="46527-140">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="46527-141">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="46527-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




