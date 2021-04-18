---
description: Метод Сетсаурценамевалидатион указывает, как подсистема подготовки отчетов проверяет имена файлов.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'Метод Ирендеренгине:: Сетсаурценамевалидатион (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676022"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a><span data-ttu-id="7c1af-103">Метод Ирендеренгине:: Сетсаурценамевалидатион</span><span class="sxs-lookup"><span data-stu-id="7c1af-103">IRenderEngine::SetSourceNameValidation method</span></span>

> [!Note]  
> <span data-ttu-id="7c1af-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7c1af-104">\[Deprecated.</span></span> <span data-ttu-id="7c1af-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c1af-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7c1af-106">`SetSourceNameValidation`Метод указывает, как подсистема подготовки отчетов проверяет имена файлов.</span><span class="sxs-lookup"><span data-stu-id="7c1af-106">The `SetSourceNameValidation` method specifies how the render engine validates file names.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c1af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c1af-107">Syntax</span></span>


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a><span data-ttu-id="7c1af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c1af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c1af-109">*филтерстринг*</span><span class="sxs-lookup"><span data-stu-id="7c1af-109">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="7c1af-110">Значение **BSTR** , содержащее пары строк фильтра, в формате, обязательном для элемента **лпстрфилтер** структуры [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="7c1af-110">**BSTR** value containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="7c1af-111">Указатель мультимедиа использует этот фильтр, если он представляет собой диалоговое окно открытия файла для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7c1af-111">The media locator uses this filter if it presents an Open File dialog box to the end user.</span></span>

</dd> <dt>

<span data-ttu-id="7c1af-112">*поверриде*</span><span class="sxs-lookup"><span data-stu-id="7c1af-112">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="7c1af-113">Необязательный указатель на интерфейс [**имедиалокатор**](imedialocator.md) указателя мультимедиа, используемый вместо значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c1af-113">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="7c1af-114">Чтобы использовать указатель носителя по умолчанию, установите для этого параметра значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7c1af-114">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="7c1af-115">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="7c1af-115">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="7c1af-116">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="7c1af-116">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="7c1af-117">Побитовое сочетание [**флагов проверки имени файла**](file-name-validation-flags.md) , определяющее поведение указателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7c1af-117">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="7c1af-118">\_ \_ Должен присутствовать флаг проверки СФН валидатеф.</span><span class="sxs-lookup"><span data-stu-id="7c1af-118">The SFN\_VALIDATEF\_CHECK flag must be present.</span></span> <span data-ttu-id="7c1af-119">Флаг СФН \_ валидатеф \_ хлинкмутед не влияет на этот метод.</span><span class="sxs-lookup"><span data-stu-id="7c1af-119">The SFN\_VALIDATEF\_hlinkMUTED flag has no effect with this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c1af-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c1af-120">Return value</span></span>

<span data-ttu-id="7c1af-121">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="7c1af-121">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="7c1af-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7c1af-122">Return code</span></span>                                                                                            | <span data-ttu-id="7c1af-123">Описание</span><span class="sxs-lookup"><span data-stu-id="7c1af-123">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7c1af-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7c1af-124"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="7c1af-125">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7c1af-125">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="7c1af-126"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="7c1af-126"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="7c1af-127">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="7c1af-127">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c1af-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c1af-128">Remarks</span></span>

<span data-ttu-id="7c1af-129">С помощью параметра *поверриде* можно предоставить собственную пользовательскую реализацию интерфейса [**имедиалокатор**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1af-129">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="7c1af-130">Например, указатель мультимедиа по умолчанию не уведомляет приложение о найденных файлах (или не может его найти).</span><span class="sxs-lookup"><span data-stu-id="7c1af-130">For example, the default media locator does not notify an application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="7c1af-131">Чтобы обойти это ограничение, можно реализовать пользовательский указатель мультимедиа, сделав его оболочкой для версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c1af-131">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="7c1af-132">Затем передайте [**имедиалокатор:: финдмедиафиле**](imedialocator-findmediafile.md) напрямую вызовет версию по умолчанию и изучите возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="7c1af-132">Then pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version and examine the return value.</span></span>

<span data-ttu-id="7c1af-133">В настоящее время этот метод не проверяет динамически загружаемые источники.</span><span class="sxs-lookup"><span data-stu-id="7c1af-133">Currently, this method does not validate dynamically loaded sources.</span></span> <span data-ttu-id="7c1af-134">См. раздел [**ирендеренгине:: сетдинамикреконнектлевел**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="7c1af-134">See [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="7c1af-135">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="7c1af-135">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7c1af-136">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c1af-136">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7c1af-137">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7c1af-137">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7c1af-138">Требования</span><span class="sxs-lookup"><span data-stu-id="7c1af-138">Requirements</span></span>



| <span data-ttu-id="7c1af-139">Требование</span><span class="sxs-lookup"><span data-stu-id="7c1af-139">Requirement</span></span> | <span data-ttu-id="7c1af-140">Значение</span><span class="sxs-lookup"><span data-stu-id="7c1af-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1af-141">Header</span><span class="sxs-lookup"><span data-stu-id="7c1af-141">Header</span></span><br/>  | <dl> <span data-ttu-id="7c1af-142"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c1af-142"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7c1af-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c1af-143">Library</span></span><br/> | <dl> <span data-ttu-id="7c1af-144"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c1af-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c1af-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c1af-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c1af-146">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="7c1af-146">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="7c1af-147">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="7c1af-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
