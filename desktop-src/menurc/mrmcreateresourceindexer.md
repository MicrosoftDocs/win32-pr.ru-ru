---
title: Функция Мрмкреатересаурцеиндексер (Мрмресаурцеиндексер. h)
description: Создает индексатор ресурсов, используемый для создания файлов индекса ресурсов пакета (PRI) для приложения UWP. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Меню функций Мрмкреатересаурцеиндексер и другие ресурсы
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415997"
---
# <a name="mrmcreateresourceindexer-function"></a><span data-ttu-id="e7efc-105">Функция Мрмкреатересаурцеиндексер</span><span class="sxs-lookup"><span data-stu-id="e7efc-105">MrmCreateResourceIndexer function</span></span>

<span data-ttu-id="e7efc-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e7efc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e7efc-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e7efc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e7efc-108">Создает индексатор ресурсов, используемый для создания файлов индекса ресурсов пакета (PRI) для приложения UWP.</span><span class="sxs-lookup"><span data-stu-id="e7efc-108">Creates a resource indexer, used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="e7efc-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="e7efc-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7efc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7efc-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="e7efc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7efc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7efc-112">*паккажефамилинаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7efc-112">*packageFamilyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7efc-113">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="e7efc-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="e7efc-114">Имя семейства пакетов приложения UWP, для которого будут создаваться PRI файлы.</span><span class="sxs-lookup"><span data-stu-id="e7efc-114">The package family name of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="e7efc-115">Это значение будет использоваться в качестве имени схемы ресурса при последующем формировании PRI-файла из этого индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7efc-115">This value will be used as the resource map name when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="e7efc-116">*прожектрут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7efc-116">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7efc-117">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="e7efc-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="e7efc-118">Корневой каталог проекта приложения UWP, для которого будут создаваться файлы PRI.</span><span class="sxs-lookup"><span data-stu-id="e7efc-118">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="e7efc-119">Иными словами, это путь к файлам ресурсов этого приложения.</span><span class="sxs-lookup"><span data-stu-id="e7efc-119">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="e7efc-120">Это можно указать таким образом, чтобы можно было указать пути относительно корня в последующих вызовах API для того же индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7efc-120">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="e7efc-121">*платформверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7efc-121">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7efc-122">Тип: **[ **мрмплатформверсион**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="e7efc-122">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="e7efc-123">Версия целевой платформы для индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7efc-123">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="e7efc-124">*дефаулткуалифиерс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e7efc-124">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e7efc-125">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="e7efc-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="e7efc-126">Список квалификаторов ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7efc-126">A list of default resource qualifiers.</span></span> <span data-ttu-id="e7efc-127">Например, L "язык-EN-US \_ Scale-100 \_ контраст — Standard"</span><span class="sxs-lookup"><span data-stu-id="e7efc-127">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="e7efc-128">*индексатор* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e7efc-128">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7efc-129">Тип: \**[**мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="e7efc-129">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="e7efc-130">Указатель на обработчик индексатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="e7efc-130">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7efc-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7efc-131">Return value</span></span>

<span data-ttu-id="e7efc-132">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e7efc-132">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e7efc-133">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="e7efc-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="e7efc-134">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="e7efc-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7efc-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e7efc-135">Requirements</span></span>



| <span data-ttu-id="e7efc-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e7efc-136">Requirement</span></span> | <span data-ttu-id="e7efc-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e7efc-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7efc-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7efc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e7efc-139">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="e7efc-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e7efc-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7efc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e7efc-141">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="e7efc-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e7efc-142">Header</span><span class="sxs-lookup"><span data-stu-id="e7efc-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7efc-143"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7efc-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="e7efc-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e7efc-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7efc-145"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7efc-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="e7efc-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e7efc-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7efc-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7efc-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e7efc-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7efc-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7efc-149">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="e7efc-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

