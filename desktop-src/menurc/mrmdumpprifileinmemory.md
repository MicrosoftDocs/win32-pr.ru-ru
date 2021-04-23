---
title: Функция Мрмдумпприфилеинмемори (Мрмресаурцеиндексер. h)
description: Выводит файл PRI (двоичный) в его эквивалент XML (как данные в памяти), чтобы сделать его более удобным для чтения.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Меню функций Мрмдумпприфилеинмемори и другие ресурсы
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661828"
---
# <a name="mrmdumpprifileinmemory-function"></a><span data-ttu-id="5f60a-104">Функция Мрмдумпприфилеинмемори</span><span class="sxs-lookup"><span data-stu-id="5f60a-104">MrmDumpPriFileInMemory function</span></span>

<span data-ttu-id="5f60a-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="5f60a-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5f60a-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="5f60a-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5f60a-107">Выводит файл PRI (двоичный) в его эквивалент XML (как данные в памяти), чтобы сделать его более удобным для чтения.</span><span class="sxs-lookup"><span data-stu-id="5f60a-107">Dumps a PRI file (which is binary) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="5f60a-108">Функция выделяет память и возвращает указатель на эту память в *аутпутксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="5f60a-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="5f60a-109">Вызовите [**мрмфримемори**](mrmfreememory.md) с тем же указателем, чтобы освободить эту память.</span><span class="sxs-lookup"><span data-stu-id="5f60a-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="5f60a-110">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="5f60a-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f60a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f60a-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="5f60a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f60a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f60a-113">*индексфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f60a-113">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f60a-114">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="5f60a-114">Type: **PCWSTR**</span></span>

<span data-ttu-id="5f60a-115">Полный путь к файлу PRI.</span><span class="sxs-lookup"><span data-stu-id="5f60a-115">A full file path to a PRI file.</span></span> <span data-ttu-id="5f60a-116">Это PRI-файл, который будет сохранен в XML.</span><span class="sxs-lookup"><span data-stu-id="5f60a-116">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="5f60a-117">*счемаприфиле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5f60a-117">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f60a-118">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="5f60a-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="5f60a-119">Необязательный полный путь к файлу схемы (или к PRI-файлу, представляющему схему; см. раздел Примечания).</span><span class="sxs-lookup"><span data-stu-id="5f60a-119">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="5f60a-120">*думптипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f60a-120">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f60a-121">Тип: **[ **мрмдумптипе**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="5f60a-121">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="5f60a-122">Указывает, насколько подробным должен быть дамп XML, или следует ли создавать дамп схемы.</span><span class="sxs-lookup"><span data-stu-id="5f60a-122">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="5f60a-123">*аутпутксмлдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5f60a-123">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f60a-124">Тип: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="5f60a-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="5f60a-125">Адрес указателя на байт.</span><span class="sxs-lookup"><span data-stu-id="5f60a-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="5f60a-126">Функция выделяет память и возвращает указатель на эту память в *аутпутксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="5f60a-126">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="5f60a-127">Вызовите [**мрмфримемори**](mrmfreememory.md) с помощью указателя на Byte, чтобы освободить эту память.</span><span class="sxs-lookup"><span data-stu-id="5f60a-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="5f60a-128">*аутпутксмлсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5f60a-128">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f60a-129">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="5f60a-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="5f60a-130">Адрес ULONG.</span><span class="sxs-lookup"><span data-stu-id="5f60a-130">The address of a ULONG.</span></span> <span data-ttu-id="5f60a-131">В _outputXmlSize \* функция возвращает размер выделенной памяти, на которую указывает *аутпутксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="5f60a-131">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f60a-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f60a-132">Return value</span></span>

<span data-ttu-id="5f60a-133">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5f60a-133">Type: **HRESULT**</span></span>

<span data-ttu-id="5f60a-134">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="5f60a-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="5f60a-135">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="5f60a-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f60a-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f60a-136">Remarks</span></span>

<span data-ttu-id="5f60a-137">Пакет ресурсов без схемы — это тот, который был создан с помощью аргумента [**мрмпаккагингоптионсомитсчемафромресаурцепаккс**](mrmpackagingoptions.md) , переданного в [**мрмкреатересаурцефиле**](mrmcreateresourcefile.md) или [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md) (или с параметром *omitSchemaFromResourcePacks* в файле конфигурации PRI).</span><span class="sxs-lookup"><span data-stu-id="5f60a-137">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="5f60a-138">Чтобы создать дамп пакета ресурсов без схемы, передайте путь к основным данным пакета PRI в качестве аргумента для параметра *счемаприфиле* .</span><span class="sxs-lookup"><span data-stu-id="5f60a-138">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f60a-139">Требования</span><span class="sxs-lookup"><span data-stu-id="5f60a-139">Requirements</span></span>



| <span data-ttu-id="5f60a-140">Требование</span><span class="sxs-lookup"><span data-stu-id="5f60a-140">Requirement</span></span> | <span data-ttu-id="5f60a-141">Значение</span><span class="sxs-lookup"><span data-stu-id="5f60a-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f60a-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f60a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5f60a-143">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="5f60a-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5f60a-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f60a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5f60a-145">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="5f60a-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5f60a-146">Header</span><span class="sxs-lookup"><span data-stu-id="5f60a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f60a-147"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f60a-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="5f60a-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5f60a-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f60a-149"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f60a-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="5f60a-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5f60a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f60a-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f60a-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5f60a-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f60a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f60a-153">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="5f60a-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

