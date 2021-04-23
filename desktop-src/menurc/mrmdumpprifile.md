---
title: Функция Мрмдумпприфиле (Мрмресаурцеиндексер. h)
description: Выводит файл PRI (двоичный) в его эквивалент XML (в виде файла на диске), чтобы сделать его более удобным для чтения.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Меню функций Мрмдумпприфиле и другие ресурсы
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802519"
---
# <a name="mrmdumpprifile-function"></a><span data-ttu-id="48adf-104">Функция Мрмдумпприфиле</span><span class="sxs-lookup"><span data-stu-id="48adf-104">MrmDumpPriFile function</span></span>

<span data-ttu-id="48adf-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="48adf-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="48adf-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="48adf-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="48adf-107">Выводит файл PRI (двоичный) в его эквивалент XML (в виде файла на диске), чтобы сделать его более удобным для чтения.</span><span class="sxs-lookup"><span data-stu-id="48adf-107">Dumps a PRI file (which is binary) to its XML equivalent (as a file on disk), in order to make it more easily readable.</span></span> <span data-ttu-id="48adf-108">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="48adf-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="48adf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48adf-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="48adf-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="48adf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48adf-111">*индексфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48adf-111">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48adf-112">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="48adf-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="48adf-113">Полный путь к файлу PRI.</span><span class="sxs-lookup"><span data-stu-id="48adf-113">A full file path to a PRI file.</span></span> <span data-ttu-id="48adf-114">Это PRI-файл, который будет сохранен в XML.</span><span class="sxs-lookup"><span data-stu-id="48adf-114">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="48adf-115">*счемаприфиле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="48adf-115">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48adf-116">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="48adf-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="48adf-117">Необязательный полный путь к файлу схемы (или к PRI-файлу, представляющему схему; см. раздел Примечания).</span><span class="sxs-lookup"><span data-stu-id="48adf-117">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="48adf-118">*думптипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48adf-118">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48adf-119">Тип: **[ **мрмдумптипе**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="48adf-119">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="48adf-120">Указывает, насколько подробным должен быть дамп XML, или следует ли создавать дамп схемы.</span><span class="sxs-lookup"><span data-stu-id="48adf-120">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="48adf-121">*аутпутксмлфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48adf-121">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48adf-122">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="48adf-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="48adf-123">Путь к создаваемому XML-файлу.</span><span class="sxs-lookup"><span data-stu-id="48adf-123">The path of an XML file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48adf-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48adf-124">Return value</span></span>

<span data-ttu-id="48adf-125">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="48adf-125">Type: **HRESULT**</span></span>

<span data-ttu-id="48adf-126">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="48adf-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="48adf-127">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="48adf-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="48adf-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48adf-128">Remarks</span></span>

<span data-ttu-id="48adf-129">Пакет ресурсов без схемы — это тот, который был создан с помощью аргумента [**мрмпаккагингоптионсомитсчемафромресаурцепаккс**](mrmpackagingoptions.md) , переданного в [**мрмкреатересаурцефиле**](mrmcreateresourcefile.md) или [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md) (или с параметром *omitSchemaFromResourcePacks* в файле конфигурации PRI).</span><span class="sxs-lookup"><span data-stu-id="48adf-129">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="48adf-130">Чтобы создать дамп пакета ресурсов без схемы, передайте путь к основным данным пакета PRI в качестве аргумента для параметра *счемаприфиле* .</span><span class="sxs-lookup"><span data-stu-id="48adf-130">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="48adf-131">Требования</span><span class="sxs-lookup"><span data-stu-id="48adf-131">Requirements</span></span>



| <span data-ttu-id="48adf-132">Требование</span><span class="sxs-lookup"><span data-stu-id="48adf-132">Requirement</span></span> | <span data-ttu-id="48adf-133">Значение</span><span class="sxs-lookup"><span data-stu-id="48adf-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48adf-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48adf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="48adf-135">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="48adf-135">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="48adf-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48adf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="48adf-137">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="48adf-137">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="48adf-138">Header</span><span class="sxs-lookup"><span data-stu-id="48adf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="48adf-139"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="48adf-139"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="48adf-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="48adf-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="48adf-141"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48adf-141"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="48adf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="48adf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48adf-143"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48adf-143"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="48adf-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48adf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48adf-145">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="48adf-145">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

