---
title: Функция Мрмкреатересаурцеиндексерфромпревиауссчемадата (Мрмресаурцеиндексер. h)
description: Создает индексатор ресурсов из данных схемы в памяти, созданных с помощью предыдущего вызова либо Мрмдумпприфилеинмемори, либо Мрмдумппридатаинмемори.
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- Меню функций Мрмкреатересаурцеиндексерфромпревиауссчемадата и другие ресурсы
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491046"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a><span data-ttu-id="13c5b-104">Функция Мрмкреатересаурцеиндексерфромпревиауссчемадата</span><span class="sxs-lookup"><span data-stu-id="13c5b-104">MrmCreateResourceIndexerFromPreviousSchemaData function</span></span>

<span data-ttu-id="13c5b-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="13c5b-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="13c5b-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="13c5b-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="13c5b-107">Создает индексатор ресурсов из данных схемы в памяти, созданных с помощью предыдущего вызова либо [**мрмдумпприфилеинмемори**](mrmdumpprifileinmemory.md) , либо [**мрмдумппридатаинмемори**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="13c5b-107">Creates a resource indexer from in-memory schema data created with a previous call to either [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="13c5b-108">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="13c5b-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="13c5b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13c5b-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="13c5b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="13c5b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c5b-111">*прожектрут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13c5b-111">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c5b-112">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="13c5b-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="13c5b-113">Корневой каталог проекта приложения UWP, для которого будут создаваться файлы PRI.</span><span class="sxs-lookup"><span data-stu-id="13c5b-113">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="13c5b-114">Иными словами, это путь к файлам ресурсов этого приложения.</span><span class="sxs-lookup"><span data-stu-id="13c5b-114">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="13c5b-115">Это можно указать таким образом, чтобы можно было указать пути относительно корня в последующих вызовах API для того же индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13c5b-115">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="13c5b-116">*платформверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13c5b-116">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c5b-117">Тип: **[ **мрмплатформверсион**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="13c5b-117">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="13c5b-118">Версия целевой платформы для индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13c5b-118">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="13c5b-119">*дефаулткуалифиерс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="13c5b-119">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13c5b-120">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="13c5b-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="13c5b-121">Список квалификаторов ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13c5b-121">A list of default resource qualifiers.</span></span> <span data-ttu-id="13c5b-122">Например, L "язык-EN-US \_ Scale-100 \_ контраст — Standard"</span><span class="sxs-lookup"><span data-stu-id="13c5b-122">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="13c5b-123">*счемаксмлдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13c5b-123">*schemaXmlData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c5b-124">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="13c5b-124">Type: \**BYTE\** _</span></span>

<span data-ttu-id="13c5b-125">Указатель на данные схемы, созданные предыдущим вызовом в значение [_ *мрмдумпприфилеинмемори* \*](mrmdumpprifileinmemory.md) или [**мрмдумппридатаинмемори**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="13c5b-125">A pointer to schema data created by a previous call to either [_ *MrmDumpPriFileInMemory*\*](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="13c5b-126">Не освобождайте *счемаксмлдата* до тех пор, пока не завершите использование индексатора ресурсов, созданного этой функцией.</span><span class="sxs-lookup"><span data-stu-id="13c5b-126">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="13c5b-127">*счемаксмлсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13c5b-127">*schemaXmlSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c5b-128">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="13c5b-128">Type: **ULONG**</span></span>

<span data-ttu-id="13c5b-129">Размер данных, на которые указывает *счемаксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="13c5b-129">The size of the data pointed to by *schemaXmlData*.</span></span>

</dd> <dt>

<span data-ttu-id="13c5b-130">*индексатор* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="13c5b-130">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13c5b-131">Тип: \**[**мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="13c5b-131">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="13c5b-132">Указатель на обработчик индексатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="13c5b-132">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13c5b-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13c5b-133">Return value</span></span>

<span data-ttu-id="13c5b-134">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="13c5b-134">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="13c5b-135">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="13c5b-135">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="13c5b-136">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="13c5b-136">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="13c5b-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13c5b-137">Remarks</span></span>

<span data-ttu-id="13c5b-138">Не освобождайте *счемаксмлдата* до тех пор, пока не завершите использование индексатора ресурсов, созданного этой функцией.</span><span class="sxs-lookup"><span data-stu-id="13c5b-138">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c5b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="13c5b-139">Requirements</span></span>



| <span data-ttu-id="13c5b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="13c5b-140">Requirement</span></span> | <span data-ttu-id="13c5b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="13c5b-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c5b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13c5b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="13c5b-143">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="13c5b-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="13c5b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13c5b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="13c5b-145">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="13c5b-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="13c5b-146">Header</span><span class="sxs-lookup"><span data-stu-id="13c5b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="13c5b-147"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="13c5b-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="13c5b-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13c5b-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="13c5b-149"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13c5b-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="13c5b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="13c5b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13c5b-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13c5b-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="13c5b-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13c5b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c5b-153">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="13c5b-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

