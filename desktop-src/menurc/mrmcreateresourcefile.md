---
title: Функция Мрмкреатересаурцефиле (Мрмресаурцеиндексер. h)
description: Создает PRI-файл (с именем \ 0034; Resources. PRI \ 0034;) или файлы на диске в указанной папке. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Меню функций Мрмкреатересаурцефиле и другие ресурсы
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803448"
---
# <a name="mrmcreateresourcefile-function"></a><span data-ttu-id="bda89-105">Функция Мрмкреатересаурцефиле</span><span class="sxs-lookup"><span data-stu-id="bda89-105">MrmCreateResourceFile function</span></span>

<span data-ttu-id="bda89-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="bda89-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bda89-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="bda89-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bda89-108">Создает PRI-файл (с именем Resources. PRI) или файлы на диске в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="bda89-108">Creates a PRI file (named "resources.pri"), or files, on disk in the specified folder.</span></span> <span data-ttu-id="bda89-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="bda89-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="bda89-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bda89-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="bda89-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bda89-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda89-112">*индексатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bda89-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda89-113">Тип: **[ **мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="bda89-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="bda89-114">Маркер, идентифицирующий индексатор ресурсов, из которого создается PRI-файл.</span><span class="sxs-lookup"><span data-stu-id="bda89-114">A handle identifying the resource indexer from which to create the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="bda89-115">*паккагингмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bda89-115">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda89-116">Тип: **[ **мрмпаккагингмоде**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="bda89-116">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="bda89-117">Указывает, должен ли PRI-файл быть автономным, автоматически разделяться по квалификатору ресурса или быть пакетом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bda89-117">Specifies whether the PRI file should be standalone, be automatically split by resource qualifier, or be a resource pack.</span></span>

</dd> <dt>

<span data-ttu-id="bda89-118">*паккагингоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bda89-118">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda89-119">Тип: **[ **мрмпаккагингоптионс**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="bda89-119">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="bda89-120">Указывает дополнительные параметры для PRI файла.</span><span class="sxs-lookup"><span data-stu-id="bda89-120">Specifies additional options about the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="bda89-121">*outputDirectory*</span><span class="sxs-lookup"><span data-stu-id="bda89-121">*outputDirectory*</span></span> 
</dt> <dd>

<span data-ttu-id="bda89-122">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="bda89-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="bda89-123">Путь к папке, в которой будет сохранен PRI-файл.</span><span class="sxs-lookup"><span data-stu-id="bda89-123">A path to a folder in which to save the PRI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda89-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bda89-124">Return value</span></span>

<span data-ttu-id="bda89-125">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bda89-125">Type: **HRESULT**</span></span>

<span data-ttu-id="bda89-126">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="bda89-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="bda89-127">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="bda89-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda89-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bda89-128">Requirements</span></span>



| <span data-ttu-id="bda89-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bda89-129">Requirement</span></span> | <span data-ttu-id="bda89-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bda89-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda89-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bda89-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bda89-132">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="bda89-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bda89-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bda89-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bda89-134">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="bda89-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bda89-135">Header</span><span class="sxs-lookup"><span data-stu-id="bda89-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda89-136"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="bda89-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="bda89-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bda89-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="bda89-138"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bda89-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="bda89-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bda89-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bda89-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bda89-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bda89-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bda89-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda89-142">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="bda89-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

