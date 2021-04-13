---
title: Функция Мрминдексфиле (Мрмресаурцеиндексер. h)
description: Индексирует файл ресурсов, принадлежащий приложению UWP. Принимает явный (но необязательный) список квалификаторов ресурсов. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Меню функций Мрминдексфиле и другие ресурсы
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492537"
---
# <a name="mrmindexfile-function"></a><span data-ttu-id="875cd-106">Функция Мрминдексфиле</span><span class="sxs-lookup"><span data-stu-id="875cd-106">MrmIndexFile function</span></span>

<span data-ttu-id="875cd-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="875cd-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="875cd-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="875cd-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="875cd-109">Индексирует файл ресурсов, принадлежащий приложению UWP.</span><span class="sxs-lookup"><span data-stu-id="875cd-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="875cd-110">Принимает явный (но необязательный) список квалификаторов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="875cd-110">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="875cd-111">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="875cd-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="875cd-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="875cd-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="875cd-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="875cd-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="875cd-114">*индексатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="875cd-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="875cd-115">Тип: **[ **мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="875cd-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="875cd-116">Маркер, идентифицирующий индексатор ресурсов, который будет индексировать файл ресурсов.</span><span class="sxs-lookup"><span data-stu-id="875cd-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="875cd-117">*resourceUri* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="875cd-117">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="875cd-118">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="875cd-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="875cd-119">URI ресурса, который необходимо назначить ресурсу.</span><span class="sxs-lookup"><span data-stu-id="875cd-119">The resource URI to assign to the resource.</span></span> <span data-ttu-id="875cd-120">Путь будет использоваться в качестве имени поддерева схемы ресурса для этого ресурса, если позднее вы создадите PRI-файл из этого индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="875cd-120">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="875cd-121">*путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="875cd-121">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="875cd-122">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="875cd-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="875cd-123">Относительный путь к файлу, содержащему ресурс, который необходимо проиндексировать.</span><span class="sxs-lookup"><span data-stu-id="875cd-123">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="875cd-124">Этот путь указывается относительно корня проекта приложения UWP, для которого создаются PRI-файлы.</span><span class="sxs-lookup"><span data-stu-id="875cd-124">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="875cd-125">Корневой каталог проекта — это значение *прожектрут* , передаваемое в [**мрмкреатересаурцеиндексер**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="875cd-125">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> <dt>

<span data-ttu-id="875cd-126">*Квалификаторы* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="875cd-126">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="875cd-127">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="875cd-127">Type: **PCWSTR**</span></span>

<span data-ttu-id="875cd-128">Необязательный список квалификаторов ресурсов, например L "язык-EN-US \_ Scale-100 \_ контраст-Standard".</span><span class="sxs-lookup"><span data-stu-id="875cd-128">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="875cd-129">Пустая строка или **nullptr** обозначает нейтральный ресурс.</span><span class="sxs-lookup"><span data-stu-id="875cd-129">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="875cd-130">Квалификаторы ресурсов *не* выводятся из *ResourceUri* и из *контаинерпас*.</span><span class="sxs-lookup"><span data-stu-id="875cd-130">Resource qualifiers are *not* inferred from *resourceUri* nor from *containerPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="875cd-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="875cd-131">Return value</span></span>

<span data-ttu-id="875cd-132">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="875cd-132">Type: **HRESULT**</span></span>

<span data-ttu-id="875cd-133">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="875cd-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="875cd-134">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="875cd-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="875cd-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="875cd-135">Remarks</span></span>

<span data-ttu-id="875cd-136">Если необходимо указать квалификаторы ресурсов, передайте их в параметр *Квалификаторы* .</span><span class="sxs-lookup"><span data-stu-id="875cd-136">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="875cd-137">Квалификаторы ресурсов *не* выводятся из *ResourceUri* и с *FilePath*.</span><span class="sxs-lookup"><span data-stu-id="875cd-137">Resource qualifiers are *not* inferred from *resourceUri* nor from *filePath*.</span></span>

<span data-ttu-id="875cd-138">В качестве имени ресурса используется сегмент имени файла *resourceUri* (не *FilePath*).</span><span class="sxs-lookup"><span data-stu-id="875cd-138">The file name segment of *resourceUri* (not *filePath*) is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="875cd-139">Требования</span><span class="sxs-lookup"><span data-stu-id="875cd-139">Requirements</span></span>



| <span data-ttu-id="875cd-140">Требование</span><span class="sxs-lookup"><span data-stu-id="875cd-140">Requirement</span></span> | <span data-ttu-id="875cd-141">Значение</span><span class="sxs-lookup"><span data-stu-id="875cd-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="875cd-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="875cd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="875cd-143">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="875cd-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="875cd-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="875cd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="875cd-145">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="875cd-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="875cd-146">Header</span><span class="sxs-lookup"><span data-stu-id="875cd-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="875cd-147"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="875cd-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="875cd-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="875cd-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="875cd-149"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="875cd-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="875cd-150">DLL</span><span class="sxs-lookup"><span data-stu-id="875cd-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="875cd-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="875cd-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="875cd-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="875cd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="875cd-153">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="875cd-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

