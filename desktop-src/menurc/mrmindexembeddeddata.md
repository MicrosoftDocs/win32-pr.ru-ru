---
title: Функция Мрминдексембеддеддата (Мрмресаурцеиндексер. h)
description: Индексирует один ресурс внедренный, принадлежащий приложению UWP.
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- Меню функций Мрминдексембеддеддата и другие ресурсы
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d08e0e125e7919ad3eb32e6cba2184356fce5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661827"
---
# <a name="mrmindexembeddeddata-function"></a><span data-ttu-id="1f943-104">Функция Мрминдексембеддеддата</span><span class="sxs-lookup"><span data-stu-id="1f943-104">MrmIndexEmbeddedData function</span></span>

<span data-ttu-id="1f943-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1f943-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1f943-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1f943-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1f943-107">Индексирует один ресурс **внедренный** , принадлежащий приложению UWP.</span><span class="sxs-lookup"><span data-stu-id="1f943-107">Indexes a single **embeddeddata** resource belonging to a UWP app.</span></span> <span data-ttu-id="1f943-108">Принимает явный (но необязательный) список квалификаторов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f943-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="1f943-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="1f943-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f943-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f943-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="1f943-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f943-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f943-112">*индексатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1f943-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f943-113">Тип: **[ **мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="1f943-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="1f943-114">Маркер, идентифицирующий индексатор ресурсов, который будет индексировать файл ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f943-114">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="1f943-115">*resourceUri* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1f943-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f943-116">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="1f943-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="1f943-117">URI ресурса, который необходимо назначить ресурсу.</span><span class="sxs-lookup"><span data-stu-id="1f943-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="1f943-118">Путь будет использоваться в качестве имени поддерева схемы ресурса для этого ресурса, если позднее вы создадите PRI-файл из этого индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f943-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="1f943-119">*внедренный* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1f943-119">*embeddedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f943-120">Тип: \**const байт \** _</span><span class="sxs-lookup"><span data-stu-id="1f943-120">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="1f943-121">Указатель на данные ресурса, который необходимо проиндексировать.</span><span class="sxs-lookup"><span data-stu-id="1f943-121">A pointer to the data of the resource that you want to index.</span></span>

</dd> <dt>

<span data-ttu-id="1f943-122">_embeddedDataSize \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="1f943-122">_embeddedDataSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f943-123">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="1f943-123">Type: **ULONG**</span></span>

<span data-ttu-id="1f943-124">Размер данных, на которые указывает *внедренный*.</span><span class="sxs-lookup"><span data-stu-id="1f943-124">The size of the data pointed to by *embeddedData*.</span></span>

</dd> <dt>

<span data-ttu-id="1f943-125">*Квалификаторы* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1f943-125">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f943-126">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="1f943-126">Type: **PCWSTR**</span></span>

<span data-ttu-id="1f943-127">Необязательный список квалификаторов ресурсов, например L "язык-EN-US \_ Scale-100 \_ контраст-Standard".</span><span class="sxs-lookup"><span data-stu-id="1f943-127">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="1f943-128">Пустая строка или **nullptr** обозначает нейтральный ресурс.</span><span class="sxs-lookup"><span data-stu-id="1f943-128">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="1f943-129">Квалификаторы ресурсов *не* выводятся из *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="1f943-129">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f943-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f943-130">Return value</span></span>

<span data-ttu-id="1f943-131">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1f943-131">Type: **HRESULT**</span></span>

<span data-ttu-id="1f943-132">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="1f943-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="1f943-133">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="1f943-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f943-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f943-134">Remarks</span></span>

<span data-ttu-id="1f943-135">Если необходимо указать квалификаторы ресурсов, передайте их в параметр *Квалификаторы* .</span><span class="sxs-lookup"><span data-stu-id="1f943-135">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="1f943-136">Квалификаторы ресурсов *не* выводятся из *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="1f943-136">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="1f943-137">В качестве имени ресурса используется сегмент имени файла *resourceUri* .</span><span class="sxs-lookup"><span data-stu-id="1f943-137">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f943-138">Требования</span><span class="sxs-lookup"><span data-stu-id="1f943-138">Requirements</span></span>



| <span data-ttu-id="1f943-139">Требование</span><span class="sxs-lookup"><span data-stu-id="1f943-139">Requirement</span></span> | <span data-ttu-id="1f943-140">Значение</span><span class="sxs-lookup"><span data-stu-id="1f943-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f943-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f943-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1f943-142">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="1f943-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1f943-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f943-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1f943-144">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="1f943-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1f943-145">Header</span><span class="sxs-lookup"><span data-stu-id="1f943-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f943-146"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f943-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="1f943-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1f943-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f943-148"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f943-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="1f943-149">DLL</span><span class="sxs-lookup"><span data-stu-id="1f943-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f943-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f943-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1f943-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f943-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f943-152">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="1f943-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

