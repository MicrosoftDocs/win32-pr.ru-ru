---
title: Функция Мрмдумппридатаинмемори (Мрмресаурцеиндексер. h)
description: Выводит сведения о PRI (в виде большого двоичного объекта в памяти, созданном предыдущим вызовом Мрмкреатересаурцефилеинмемори) к его эквиваленту в формате XML (как данные в памяти), чтобы сделать его более удобным для чтения.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Меню функций Мрмдумппридатаинмемори и другие ресурсы
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661960"
---
# <a name="mrmdumppridatainmemory-function"></a><span data-ttu-id="6bca9-104">Функция Мрмдумппридатаинмемори</span><span class="sxs-lookup"><span data-stu-id="6bca9-104">MrmDumpPriDataInMemory function</span></span>

<span data-ttu-id="6bca9-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="6bca9-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6bca9-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6bca9-107">Выводит сведения о PRI (в виде большого двоичного объекта в памяти, созданном предыдущим вызовом [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md)) к его эквиваленту в формате XML (как данные в памяти), чтобы сделать его более удобным для чтения.</span><span class="sxs-lookup"><span data-stu-id="6bca9-107">Dumps PRI info (as a blob in memory, created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="6bca9-108">Функция выделяет память и возвращает указатель на эту память в *аутпутксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="6bca9-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="6bca9-109">Вызовите [**мрмфримемори**](mrmfreememory.md) с тем же указателем, чтобы освободить эту память.</span><span class="sxs-lookup"><span data-stu-id="6bca9-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="6bca9-110">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="6bca9-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="6bca9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bca9-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="6bca9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bca9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bca9-113">*инпутпридата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-113">*inputPriData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bca9-114">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="6bca9-114">Type: \**BYTE\** _</span></span>

<span data-ttu-id="6bca9-115">Указатель на данные PRI, созданные при предыдущем вызове к [_ *мрмкреатересаурцефилеинмемори* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="6bca9-115">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bca9-116">*инпутприсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-116">*inputPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bca9-117">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="6bca9-117">Type: **ULONG**</span></span>

<span data-ttu-id="6bca9-118">Размер данных, на которые указывает *инпутпридата*.</span><span class="sxs-lookup"><span data-stu-id="6bca9-118">The size of the data pointed to by *inputPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="6bca9-119">*счемапридата* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-119">*schemaPriData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6bca9-120">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="6bca9-120">Type: \**BYTE\** _</span></span>

<span data-ttu-id="6bca9-121">Необязательный указатель на сведения о PRI (в виде большого двоичного объекта в памяти), представляющий данные схемы, созданные предыдущим вызовом к [_ *мрмкреатересаурцефилеинмемори* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="6bca9-121">An optional pointer to PRI info (as a blob in memory) representing schema data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="6bca9-122">Не освобождайте *счемапридата* до тех пор, пока не завершите использование индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bca9-122">Don't free *schemaPriData* until after you've finished using the resource indexer.</span></span> <span data-ttu-id="6bca9-123">См. также примечания.</span><span class="sxs-lookup"><span data-stu-id="6bca9-123">Also see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6bca9-124">*счемаприсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-124">*schemaPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bca9-125">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="6bca9-125">Type: **ULONG**</span></span>

<span data-ttu-id="6bca9-126">Размер данных, на которые указывает *счемапридата*.</span><span class="sxs-lookup"><span data-stu-id="6bca9-126">The size of the data pointed to by *schemaPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="6bca9-127">*думптипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-127">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bca9-128">Тип: **[ **мрмдумптипе**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="6bca9-128">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="6bca9-129">Указывает, насколько подробным должен быть дамп XML, или следует ли создавать дамп схемы.</span><span class="sxs-lookup"><span data-stu-id="6bca9-129">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="6bca9-130">*аутпутксмлдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-130">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bca9-131">Тип: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="6bca9-131">Type: **BYTE\*\***</span></span>

<span data-ttu-id="6bca9-132">Адрес указателя на байт.</span><span class="sxs-lookup"><span data-stu-id="6bca9-132">The address of a pointer to BYTE.</span></span> <span data-ttu-id="6bca9-133">Функция выделяет память и возвращает указатель на эту память в *аутпутксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="6bca9-133">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="6bca9-134">Вызовите [**мрмфримемори**](mrmfreememory.md) с помощью указателя на Byte, чтобы освободить эту память.</span><span class="sxs-lookup"><span data-stu-id="6bca9-134">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="6bca9-135">*аутпутксмлсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-135">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bca9-136">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="6bca9-136">Type: \**ULONG\** _</span></span>

<span data-ttu-id="6bca9-137">Адрес ULONG.</span><span class="sxs-lookup"><span data-stu-id="6bca9-137">The address of a ULONG.</span></span> <span data-ttu-id="6bca9-138">В _outputXmlSize \* функция возвращает размер выделенной памяти, на которую указывает *аутпутксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="6bca9-138">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bca9-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bca9-139">Return value</span></span>

<span data-ttu-id="6bca9-140">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6bca9-140">Type: **HRESULT**</span></span>

<span data-ttu-id="6bca9-141">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="6bca9-141">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="6bca9-142">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="6bca9-142">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bca9-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bca9-143">Remarks</span></span>

<span data-ttu-id="6bca9-144">Пакет ресурсов без схемы — это тот, который был создан с помощью аргумента [**мрмпаккагингоптионсомитсчемафромресаурцепаккс**](mrmpackagingoptions.md) , переданного в [**мрмкреатересаурцефиле**](mrmcreateresourcefile.md) или [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md) (или с параметром *omitSchemaFromResourcePacks* в файле конфигурации PRI).</span><span class="sxs-lookup"><span data-stu-id="6bca9-144">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="6bca9-145">Чтобы создать дамп пакета ресурсов без схемы, передайте путь к основным данным пакета PRI в качестве аргумента для параметра *счемапридата* .</span><span class="sxs-lookup"><span data-stu-id="6bca9-145">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriData* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bca9-146">Требования</span><span class="sxs-lookup"><span data-stu-id="6bca9-146">Requirements</span></span>



| <span data-ttu-id="6bca9-147">Требование</span><span class="sxs-lookup"><span data-stu-id="6bca9-147">Requirement</span></span> | <span data-ttu-id="6bca9-148">Значение</span><span class="sxs-lookup"><span data-stu-id="6bca9-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bca9-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6bca9-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6bca9-150">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-150">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6bca9-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6bca9-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6bca9-152">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="6bca9-152">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6bca9-153">Header</span><span class="sxs-lookup"><span data-stu-id="6bca9-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bca9-154"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bca9-154"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="6bca9-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6bca9-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bca9-156"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bca9-156"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="6bca9-157">DLL</span><span class="sxs-lookup"><span data-stu-id="6bca9-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bca9-158"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bca9-158"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6bca9-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bca9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bca9-160">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="6bca9-160">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

