---
title: Функция Мрминдексресаурцеконтаинераутокуалифиерс (Мрмресаурцеиндексер. h)
description: Индексирует строковые ресурсы, содержащиеся в файле ресурсов (. resw/. resjson), или. приинфо или. прифиле, относящиеся к приложению UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Меню функций Мрминдексресаурцеконтаинераутокуалифиерс и другие ресурсы
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710517"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a><span data-ttu-id="48eb5-104">Функция Мрминдексресаурцеконтаинераутокуалифиерс</span><span class="sxs-lookup"><span data-stu-id="48eb5-104">MrmIndexResourceContainerAutoQualifiers function</span></span>

<span data-ttu-id="48eb5-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="48eb5-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="48eb5-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="48eb5-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="48eb5-107">Индексирует строковые ресурсы, содержащиеся в файле ресурсов (. resw/. resjson), или. приинфо или. прифиле, относящиеся к приложению UWP.</span><span class="sxs-lookup"><span data-stu-id="48eb5-107">Indexes the string resources contained inside a Resources File (.resw/.resjson), or a .priinfo or .prifile, belonging to a UWP app.</span></span> <span data-ttu-id="48eb5-108">Выводит список квалификаторов ресурсов из параметра *контаинерпас* .</span><span class="sxs-lookup"><span data-stu-id="48eb5-108">Infers a list of resource qualifiers from the *containerPath* parameter.</span></span> <span data-ttu-id="48eb5-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="48eb5-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="48eb5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48eb5-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a><span data-ttu-id="48eb5-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="48eb5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48eb5-112">*индексатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48eb5-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48eb5-113">Тип: **[ **мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="48eb5-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="48eb5-114">Маркер, идентифицирующий индексатор ресурсов, который будет индексировать строковые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="48eb5-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="48eb5-115">*контаинерпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48eb5-115">*containerPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48eb5-116">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="48eb5-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="48eb5-117">Относительный путь к. resw,. resjson,. приинфо или. прифиле, содержащий строковые ресурсы, которые необходимо индексировать.</span><span class="sxs-lookup"><span data-stu-id="48eb5-117">A relative path to a .resw, .resjson, .priinfo, or .prifile containing string resources that you want to index.</span></span> <span data-ttu-id="48eb5-118">Этот путь указывается относительно корня проекта приложения UWP, для которого создаются PRI-файлы.</span><span class="sxs-lookup"><span data-stu-id="48eb5-118">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="48eb5-119">Корневой каталог проекта — это значение *прожектрут* , передаваемое в [**мрмкреатересаурцеиндексер**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="48eb5-119">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48eb5-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48eb5-120">Return value</span></span>

<span data-ttu-id="48eb5-121">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="48eb5-121">Type: **HRESULT**</span></span>

<span data-ttu-id="48eb5-122">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="48eb5-122">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="48eb5-123">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="48eb5-123">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="48eb5-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48eb5-124">Remarks</span></span>

<span data-ttu-id="48eb5-125">Квалификаторы ресурсов выводятся из *контаинерпас*.</span><span class="sxs-lookup"><span data-stu-id="48eb5-125">Resource qualifiers are inferred from *containerPath*.</span></span> <span data-ttu-id="48eb5-126">Например, значение L "en-US \\ \\ Resources. resw" добавляет строковые ресурсы с квалификатором "Language-en-US".</span><span class="sxs-lookup"><span data-stu-id="48eb5-126">For example, a value of L"en-US\\\\resources.resw" adds string resources with the qualifier "language-en-US".</span></span>

<span data-ttu-id="48eb5-127">Имя файла ресурсов будет использоваться в качестве имени поддерева схемы ресурса для этих ресурсов при последующем формировании PRI-файла из этого индексатора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48eb5-127">The name of the Resources File will be used as the resource map subtree name for these resources when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="48eb5-128">Требования</span><span class="sxs-lookup"><span data-stu-id="48eb5-128">Requirements</span></span>



| <span data-ttu-id="48eb5-129">Требование</span><span class="sxs-lookup"><span data-stu-id="48eb5-129">Requirement</span></span> | <span data-ttu-id="48eb5-130">Значение</span><span class="sxs-lookup"><span data-stu-id="48eb5-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48eb5-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48eb5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="48eb5-132">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="48eb5-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="48eb5-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48eb5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="48eb5-134">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="48eb5-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="48eb5-135">Header</span><span class="sxs-lookup"><span data-stu-id="48eb5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="48eb5-136"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="48eb5-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="48eb5-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="48eb5-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="48eb5-138"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48eb5-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="48eb5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="48eb5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48eb5-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48eb5-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="48eb5-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48eb5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48eb5-142">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="48eb5-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

