---
title: Функция Мрминдексстринг (Мрмресаурцеиндексер. h)
description: Индексирует один строковый ресурс, принадлежащий приложению UWP.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Меню функций Мрминдексстринг и другие ресурсы
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135223"
---
# <a name="mrmindexstring-function"></a><span data-ttu-id="fd16a-104">Функция Мрминдексстринг</span><span class="sxs-lookup"><span data-stu-id="fd16a-104">MrmIndexString function</span></span>

<span data-ttu-id="fd16a-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="fd16a-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fd16a-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="fd16a-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fd16a-107">Индексирует один строковый ресурс, принадлежащий приложению UWP.</span><span class="sxs-lookup"><span data-stu-id="fd16a-107">Indexes a single string resource belonging to a UWP app.</span></span> <span data-ttu-id="fd16a-108">Принимает явный (но необязательный) список квалификаторов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd16a-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="fd16a-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="fd16a-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd16a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd16a-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="fd16a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd16a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd16a-112">*индексатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd16a-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd16a-113">Тип: **[ **мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="fd16a-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="fd16a-114">Маркер, идентифицирующий индексатор ресурсов, который будет индексировать строковые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="fd16a-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="fd16a-115">*resourceUri* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd16a-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd16a-116">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="fd16a-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="fd16a-117">URI ресурса, который необходимо назначить ресурсу.</span><span class="sxs-lookup"><span data-stu-id="fd16a-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="fd16a-118">Путь будет использоваться в качестве имени поддерева схемы ресурса для этого ресурса, если позднее вы создадите PRI-файл из этого индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd16a-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="fd16a-119">*ресаурцестринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd16a-119">*resourceString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd16a-120">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="fd16a-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="fd16a-121">Значение строкового ресурса.</span><span class="sxs-lookup"><span data-stu-id="fd16a-121">The value of the string resource.</span></span>

</dd> <dt>

<span data-ttu-id="fd16a-122">*Квалификаторы* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fd16a-122">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fd16a-123">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="fd16a-123">Type: **PCWSTR**</span></span>

<span data-ttu-id="fd16a-124">Необязательный список квалификаторов ресурсов, например L "язык-EN-US \_ Scale-100 \_ контраст-Standard".</span><span class="sxs-lookup"><span data-stu-id="fd16a-124">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="fd16a-125">Пустая строка или **nullptr** обозначает нейтральный ресурс.</span><span class="sxs-lookup"><span data-stu-id="fd16a-125">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="fd16a-126">Квалификаторы ресурсов *не* выводятся из *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="fd16a-126">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd16a-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd16a-127">Return value</span></span>

<span data-ttu-id="fd16a-128">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fd16a-128">Type: **HRESULT**</span></span>

<span data-ttu-id="fd16a-129">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="fd16a-129">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="fd16a-130">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="fd16a-130">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd16a-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd16a-131">Remarks</span></span>

<span data-ttu-id="fd16a-132">Если необходимо указать квалификаторы ресурсов, передайте их в параметр *Квалификаторы* .</span><span class="sxs-lookup"><span data-stu-id="fd16a-132">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="fd16a-133">Квалификаторы ресурсов *не* выводятся из *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="fd16a-133">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="fd16a-134">В качестве имени ресурса используется сегмент имени файла *resourceUri* .</span><span class="sxs-lookup"><span data-stu-id="fd16a-134">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd16a-135">Требования</span><span class="sxs-lookup"><span data-stu-id="fd16a-135">Requirements</span></span>



| <span data-ttu-id="fd16a-136">Требование</span><span class="sxs-lookup"><span data-stu-id="fd16a-136">Requirement</span></span> | <span data-ttu-id="fd16a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="fd16a-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd16a-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd16a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fd16a-139">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="fd16a-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fd16a-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd16a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fd16a-141">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="fd16a-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fd16a-142">Header</span><span class="sxs-lookup"><span data-stu-id="fd16a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd16a-143"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd16a-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="fd16a-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd16a-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd16a-145"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd16a-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="fd16a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fd16a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd16a-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd16a-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="fd16a-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd16a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd16a-149">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="fd16a-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

