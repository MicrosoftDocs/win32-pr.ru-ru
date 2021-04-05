---
title: Функция Мрмкреатересаурцеиндексерфромпревиауссчемафиле (Мрмресаурцеиндексер. h)
description: Создает индексатор ресурсов из файла схемы, созданного с помощью предыдущего вызова метода Мрмдумпприфиле. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- Меню функций Мрмкреатересаурцеиндексерфромпревиауссчемафиле и другие ресурсы
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 304e0aebe75ac416623cb1ec1053a7b6ae504194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803442"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a><span data-ttu-id="0f138-105">Функция Мрмкреатересаурцеиндексерфромпревиауссчемафиле</span><span class="sxs-lookup"><span data-stu-id="0f138-105">MrmCreateResourceIndexerFromPreviousSchemaFile function</span></span>

<span data-ttu-id="0f138-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="0f138-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0f138-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="0f138-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0f138-108">Создает индексатор ресурсов из файла схемы, созданного с помощью предыдущего вызова метода [**мрмдумпприфиле**](mrmdumpprifile.md).</span><span class="sxs-lookup"><span data-stu-id="0f138-108">Creates a resource indexer from a schema file created with a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span> <span data-ttu-id="0f138-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="0f138-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f138-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f138-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="0f138-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f138-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f138-112">*прожектрут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f138-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f138-113">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="0f138-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="0f138-114">Корневой каталог проекта приложения UWP, для которого будут создаваться файлы PRI.</span><span class="sxs-lookup"><span data-stu-id="0f138-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="0f138-115">Иными словами, это путь к файлам ресурсов этого приложения.</span><span class="sxs-lookup"><span data-stu-id="0f138-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="0f138-116">Это можно указать таким образом, чтобы можно было указать пути относительно корня в последующих вызовах API для того же индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f138-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="0f138-117">*платформверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f138-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f138-118">Тип: **[ **мрмплатформверсион**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="0f138-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="0f138-119">Версия целевой платформы для индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f138-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="0f138-120">*дефаулткуалифиерс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0f138-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f138-121">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="0f138-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="0f138-122">Список квалификаторов ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f138-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="0f138-123">Например, L "язык-EN-US \_ Scale-100 \_ контраст — Standard"</span><span class="sxs-lookup"><span data-stu-id="0f138-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="0f138-124">*счемафиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f138-124">*schemaFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f138-125">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="0f138-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="0f138-126">Полный путь к файлу схемы, созданному при предыдущем вызове [**мрмдумпприфиле**](mrmdumpprifile.md).</span><span class="sxs-lookup"><span data-stu-id="0f138-126">A full file path to a schema file created by a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f138-127">*индексатор* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0f138-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f138-128">Тип: \**[**мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="0f138-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="0f138-129">Указатель на обработчик индексатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f138-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f138-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f138-130">Return value</span></span>

<span data-ttu-id="0f138-131">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0f138-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0f138-132">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="0f138-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="0f138-133">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="0f138-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f138-134">Требования</span><span class="sxs-lookup"><span data-stu-id="0f138-134">Requirements</span></span>



| <span data-ttu-id="0f138-135">Требование</span><span class="sxs-lookup"><span data-stu-id="0f138-135">Requirement</span></span> | <span data-ttu-id="0f138-136">Значение</span><span class="sxs-lookup"><span data-stu-id="0f138-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f138-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f138-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0f138-138">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="0f138-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0f138-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f138-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0f138-140">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="0f138-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0f138-141">Header</span><span class="sxs-lookup"><span data-stu-id="0f138-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f138-142"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f138-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="0f138-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f138-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f138-144"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f138-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="0f138-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0f138-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f138-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f138-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0f138-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f138-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f138-148">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="0f138-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

