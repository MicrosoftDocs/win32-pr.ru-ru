---
title: Функция Мрминдексфилеаутокуалифиерс (Мрмресаурцеиндексер. h)
description: Индексирует файл ресурсов, принадлежащий приложению UWP. Выводит список квалификаторов ресурсов из параметра filePath. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Меню функций Мрминдексфилеаутокуалифиерс и другие ресурсы
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65254a8715073060e9b4fc1578b68d54ae987958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135226"
---
# <a name="mrmindexfileautoqualifiers-function"></a><span data-ttu-id="8289d-106">Функция Мрминдексфилеаутокуалифиерс</span><span class="sxs-lookup"><span data-stu-id="8289d-106">MrmIndexFileAutoQualifiers function</span></span>

<span data-ttu-id="8289d-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="8289d-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8289d-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="8289d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8289d-109">Индексирует файл ресурсов, принадлежащий приложению UWP.</span><span class="sxs-lookup"><span data-stu-id="8289d-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="8289d-110">Выводит список квалификаторов ресурсов из параметра *FilePath* .</span><span class="sxs-lookup"><span data-stu-id="8289d-110">Infers a list of resource qualifiers from the *filePath* parameter.</span></span> <span data-ttu-id="8289d-111">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="8289d-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="8289d-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8289d-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a><span data-ttu-id="8289d-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="8289d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8289d-114">*индексатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8289d-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8289d-115">Тип: **[ **мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="8289d-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="8289d-116">Маркер, идентифицирующий индексатор ресурсов, который будет индексировать файл ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8289d-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="8289d-117">*путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8289d-117">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8289d-118">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="8289d-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="8289d-119">Относительный путь к файлу, содержащему ресурс, который необходимо проиндексировать.</span><span class="sxs-lookup"><span data-stu-id="8289d-119">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="8289d-120">Этот путь указывается относительно корня проекта приложения UWP, для которого создаются PRI-файлы.</span><span class="sxs-lookup"><span data-stu-id="8289d-120">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="8289d-121">Корневой каталог проекта — это значение *прожектрут* , передаваемое в [**мрмкреатересаурцеиндексер**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="8289d-121">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8289d-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8289d-122">Return value</span></span>

<span data-ttu-id="8289d-123">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8289d-123">Type: **HRESULT**</span></span>

<span data-ttu-id="8289d-124">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="8289d-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="8289d-125">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="8289d-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8289d-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8289d-126">Remarks</span></span>

<span data-ttu-id="8289d-127">В качестве имени ресурса используется сегмент *FilePath* имени файла. Квалификаторы ресурсов и являются производными от их пути.</span><span class="sxs-lookup"><span data-stu-id="8289d-127">The file name segment of *filePath* is used as the resource name; and resource qualifiers are derived from its path.</span></span> <span data-ttu-id="8289d-128">Например, если передать L "Images \\ de-de \\ scale-100 \\background.png" в *FilePath* , то индексатор ресурсов добавит ресурс с именем "background.png" с квалификаторами ресурсов "Language-de-de" и "Scale-100".</span><span class="sxs-lookup"><span data-stu-id="8289d-128">For example, if you pass L"Images\\de-DE\\scale-100\\background.png" to *filePath* then the resource indexer adds a resource named "background.png" with resource qualifiers "language-de-DE" and "scale-100".</span></span>

<span data-ttu-id="8289d-129">L "Files" будет использоваться в качестве имени поддерева схемы ресурсов для этого ресурса при последующем создании PRI-файла из этого индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8289d-129">L"Files" will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8289d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="8289d-130">Requirements</span></span>



| <span data-ttu-id="8289d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="8289d-131">Requirement</span></span> | <span data-ttu-id="8289d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8289d-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8289d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8289d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8289d-134">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="8289d-134">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8289d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8289d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8289d-136">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="8289d-136">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8289d-137">Header</span><span class="sxs-lookup"><span data-stu-id="8289d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="8289d-138"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="8289d-138"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="8289d-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8289d-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="8289d-140"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8289d-140"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="8289d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8289d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8289d-142"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8289d-142"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="8289d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8289d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8289d-144">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="8289d-144">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

