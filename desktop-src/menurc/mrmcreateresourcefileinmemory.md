---
title: Функция Мрмкреатересаурцефилеинмемори (Мрмресаурцеиндексер. h)
description: Создает сведения PRI в виде большого двоичного объекта в памяти, а не в виде файла на диске.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Меню функций Мрмкреатересаурцефилеинмемори и другие ресурсы
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492543"
---
# <a name="mrmcreateresourcefileinmemory-function"></a><span data-ttu-id="d7744-104">Функция Мрмкреатересаурцефилеинмемори</span><span class="sxs-lookup"><span data-stu-id="d7744-104">MrmCreateResourceFileInMemory function</span></span>

<span data-ttu-id="d7744-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="d7744-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d7744-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="d7744-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d7744-107">Создает сведения PRI в виде большого двоичного объекта в памяти, а не в виде файла на диске.</span><span class="sxs-lookup"><span data-stu-id="d7744-107">Creates PRI info as a blob in memory, not as a file on disk.</span></span> <span data-ttu-id="d7744-108">Функция выделяет память и возвращает указатель на эту память в *аутпутпридата*.</span><span class="sxs-lookup"><span data-stu-id="d7744-108">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="d7744-109">Вызовите [**мрмфримемори**](mrmfreememory.md) с тем же указателем, чтобы освободить эту память.</span><span class="sxs-lookup"><span data-stu-id="d7744-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="d7744-110">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="d7744-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7744-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7744-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a><span data-ttu-id="d7744-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7744-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7744-113">*индексатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7744-113">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7744-114">Тип: **[ **мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="d7744-114">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="d7744-115">Маркер, идентифицирующий индексатор ресурсов, из которого создаются сведения о PRI.</span><span class="sxs-lookup"><span data-stu-id="d7744-115">A handle identifying the resource indexer from which to create the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="d7744-116">*паккагингмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7744-116">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7744-117">Тип: **[ **мрмпаккагингмоде**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="d7744-117">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="d7744-118">Указывает, должны ли сведения PRI быть автономными или являться пакетами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7744-118">Specifies whether the PRI info should be standalone, or be a resource pack.</span></span> <span data-ttu-id="d7744-119">**Мрмпаккагингмодеаутосплит** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d7744-119">**MrmPackagingModeAutoSplit** is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d7744-120">*паккагингоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7744-120">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7744-121">Тип: **[ **мрмпаккагингоптионс**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="d7744-121">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="d7744-122">Задает дополнительные параметры сведений о PRI.</span><span class="sxs-lookup"><span data-stu-id="d7744-122">Specifies additional options about the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="d7744-123">*аутпутпридата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7744-123">*outputPriData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7744-124">Тип: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="d7744-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="d7744-125">Адрес указателя на байт.</span><span class="sxs-lookup"><span data-stu-id="d7744-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="d7744-126">Функция выделяет память и возвращает указатель на эту память в *аутпутпридата*.</span><span class="sxs-lookup"><span data-stu-id="d7744-126">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="d7744-127">Вызовите [**мрмфримемори**](mrmfreememory.md) с помощью указателя на Byte, чтобы освободить эту память.</span><span class="sxs-lookup"><span data-stu-id="d7744-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="d7744-128">*аутпутприсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7744-128">*outputPriSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7744-129">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="d7744-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="d7744-130">Адрес ULONG.</span><span class="sxs-lookup"><span data-stu-id="d7744-130">The address of a ULONG.</span></span> <span data-ttu-id="d7744-131">В _outputPriSize \* функция возвращает размер выделенной памяти, на которую указывает *аутпутпридата*.</span><span class="sxs-lookup"><span data-stu-id="d7744-131">In _outputPriSize\*, the function returns the size of the allocated memory pointed to by *outputPriData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7744-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7744-132">Return value</span></span>

<span data-ttu-id="d7744-133">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d7744-133">Type: **HRESULT**</span></span>

<span data-ttu-id="d7744-134">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="d7744-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="d7744-135">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="d7744-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7744-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7744-136">Remarks</span></span>

<span data-ttu-id="d7744-137">Если вы передадите *аутпутпридата* в [**мрмкреатересаурцеиндексерфромпревиауспридата**](mrmcreateresourceindexerfrompreviouspridata-.md), не освобождайте память до тех пор, пока не завершите использование индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7744-137">If you pass *outputPriData* to [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), then don't free the memory until after you've finished using the resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7744-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d7744-138">Requirements</span></span>



| <span data-ttu-id="d7744-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d7744-139">Requirement</span></span> | <span data-ttu-id="d7744-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d7744-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7744-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7744-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d7744-142">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="d7744-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d7744-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7744-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d7744-144">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="d7744-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d7744-145">Header</span><span class="sxs-lookup"><span data-stu-id="d7744-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7744-146"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7744-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="d7744-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d7744-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7744-148"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7744-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="d7744-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d7744-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7744-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7744-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d7744-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7744-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7744-152">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="d7744-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

