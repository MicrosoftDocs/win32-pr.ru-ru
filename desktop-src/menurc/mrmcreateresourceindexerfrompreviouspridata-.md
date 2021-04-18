---
title: Функция Мрмкреатересаурцеиндексерфромпревиауспридата (Мрмресаурцеиндексер. h)
description: Создает индексатор ресурсов из данных PRI, созданных при предыдущем вызове метода Мрмкреатересаурцефилеинмемори. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: 945ED98C-8D73-404F-ACE3-7DD314FB405A
keywords:
- Меню функций Мрмкреатересаурцеиндексерфромпревиауспридата и другие ресурсы
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152ded28e6158fb80d8157c751026091afb51f65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341010"
---
# <a name="mrmcreateresourceindexerfrompreviouspridata-function"></a><span data-ttu-id="a52eb-105">Функция Мрмкреатересаурцеиндексерфромпревиауспридата</span><span class="sxs-lookup"><span data-stu-id="a52eb-105">MrmCreateResourceIndexerFromPreviousPriData function</span></span>

<span data-ttu-id="a52eb-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="a52eb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a52eb-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="a52eb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a52eb-108">Создает индексатор ресурсов из данных PRI, созданных при предыдущем вызове метода [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="a52eb-108">Creates a resource indexer from PRI data created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="a52eb-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="a52eb-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="a52eb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a52eb-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriData (
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *priData,
  _In_     ULONG                    priSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="a52eb-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a52eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a52eb-112">*прожектрут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a52eb-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52eb-113">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="a52eb-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="a52eb-114">Корневой каталог проекта приложения UWP, для которого будут создаваться файлы PRI.</span><span class="sxs-lookup"><span data-stu-id="a52eb-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="a52eb-115">Иными словами, это путь к файлам ресурсов этого приложения.</span><span class="sxs-lookup"><span data-stu-id="a52eb-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="a52eb-116">Это можно указать таким образом, чтобы можно было указать пути относительно корня в последующих вызовах API для того же индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a52eb-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="a52eb-117">*платформверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a52eb-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52eb-118">Тип: **[ **мрмплатформверсион**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="a52eb-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="a52eb-119">Версия целевой платформы для индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a52eb-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="a52eb-120">*дефаулткуалифиерс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a52eb-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a52eb-121">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="a52eb-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="a52eb-122">Список квалификаторов ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a52eb-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="a52eb-123">Например, L "язык-EN-US \_ Scale-100 \_ контраст — Standard"</span><span class="sxs-lookup"><span data-stu-id="a52eb-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="a52eb-124">*придата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a52eb-124">*priData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52eb-125">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="a52eb-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="a52eb-126">Указатель на данные PRI, созданные при предыдущем вызове к [_ *мрмкреатересаурцефилеинмемори* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="a52eb-126">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="a52eb-127">Не освобождайте *придата* до тех пор, пока не завершите использование индексатора ресурсов, созданного этой функцией.</span><span class="sxs-lookup"><span data-stu-id="a52eb-127">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="a52eb-128">*присизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a52eb-128">*priSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52eb-129">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="a52eb-129">Type: **ULONG**</span></span>

<span data-ttu-id="a52eb-130">Размер данных, на которые указывает *придата*.</span><span class="sxs-lookup"><span data-stu-id="a52eb-130">The size of the data pointed to by *priData*.</span></span>

</dd> <dt>

<span data-ttu-id="a52eb-131">*индексатор* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a52eb-131">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a52eb-132">Тип: \**[**мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="a52eb-132">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="a52eb-133">Указатель на обработчик индексатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="a52eb-133">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a52eb-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a52eb-134">Return value</span></span>

<span data-ttu-id="a52eb-135">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a52eb-135">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a52eb-136">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="a52eb-136">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="a52eb-137">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="a52eb-137">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a52eb-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a52eb-138">Remarks</span></span>

<span data-ttu-id="a52eb-139">Не освобождайте *придата* до тех пор, пока не завершите использование индексатора ресурсов, созданного этой функцией.</span><span class="sxs-lookup"><span data-stu-id="a52eb-139">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a52eb-140">Требования</span><span class="sxs-lookup"><span data-stu-id="a52eb-140">Requirements</span></span>



| <span data-ttu-id="a52eb-141">Требование</span><span class="sxs-lookup"><span data-stu-id="a52eb-141">Requirement</span></span> | <span data-ttu-id="a52eb-142">Значение</span><span class="sxs-lookup"><span data-stu-id="a52eb-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a52eb-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a52eb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a52eb-144">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="a52eb-144">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a52eb-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a52eb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a52eb-146">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="a52eb-146">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a52eb-147">Header</span><span class="sxs-lookup"><span data-stu-id="a52eb-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a52eb-148"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="a52eb-148"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="a52eb-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a52eb-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="a52eb-150"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a52eb-150"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="a52eb-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a52eb-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a52eb-152"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a52eb-152"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a52eb-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a52eb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a52eb-154">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="a52eb-154">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

