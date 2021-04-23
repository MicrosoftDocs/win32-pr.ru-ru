---
description: ICE42 проверяет, что внутренние серверы не связаны с EXE – файлами в таблице классов. Также проверяется, что только классы Локалсервер и LocalServer32 имеют аргументы и значения Дефинпрок.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650926"
---
# <a name="ice42"></a><span data-ttu-id="bf299-104">ICE42</span><span class="sxs-lookup"><span data-stu-id="bf299-104">ICE42</span></span>

<span data-ttu-id="bf299-105">ICE42 проверяет, что внутренние серверы не связаны с EXE – файлами в [таблице классов](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="bf299-105">ICE42 validates that InProc servers are not linked to EXE files in the [Class table](class-table.md).</span></span> <span data-ttu-id="bf299-106">Также проверяется, что только классы Локалсервер и LocalServer32 имеют аргументы и значения Дефинпрок.</span><span class="sxs-lookup"><span data-stu-id="bf299-106">It also validates that only LocalServer and LocalServer32 classes have arguments and DefInProc values.</span></span>

## <a name="result"></a><span data-ttu-id="bf299-107">Результат</span><span class="sxs-lookup"><span data-stu-id="bf299-107">Result</span></span>

<span data-ttu-id="bf299-108">ICE42 отправляет сообщение об ошибке, если в таблице классов есть внутренние серверы, связанные с ИСПОЛНЯЕМыми файлами.</span><span class="sxs-lookup"><span data-stu-id="bf299-108">ICE42 posts an error if there are InProc servers linked to EXE files in the Class table.</span></span>

## <a name="example"></a><span data-ttu-id="bf299-109">Пример</span><span class="sxs-lookup"><span data-stu-id="bf299-109">Example</span></span>

<span data-ttu-id="bf299-110">ICE42 сообщит о следующих ошибках в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="bf299-110">ICE42 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="bf299-111">ICE42, ошибка</span><span class="sxs-lookup"><span data-stu-id="bf299-111">ICE42 error</span></span>                                                                                                                             | <span data-ttu-id="bf299-112">Описание</span><span class="sxs-lookup"><span data-stu-id="bf299-112">Description</span></span>                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf299-113">CLSID "{GUID1}" является сервером InProc, но реализующий компонент "Component1" содержит EXE-файл ("test.exe") в качестве ключа.</span><span class="sxs-lookup"><span data-stu-id="bf299-113">CLSID '{GUID1}' is an InProc server, but the implementing component 'Component1' has an EXE ('test.exe') as its KeyFile.</span></span>                | <span data-ttu-id="bf299-114">В качестве сервера INPROC указан исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="bf299-114">There is an executable file specified as an InProc server.</span></span> <span data-ttu-id="bf299-115">Файлы EXE не могут быть серверами INPROC.</span><span class="sxs-lookup"><span data-stu-id="bf299-115">EXE files cannot be InProc servers.</span></span>                                                                                                                            |
| <span data-ttu-id="bf299-116">CLSID "{GUID1}" в контексте "InProcServer32" содержит аргумент.</span><span class="sxs-lookup"><span data-stu-id="bf299-116">CLSID '{GUID1}' in context 'InProcServer32' has an argument.</span></span> <span data-ttu-id="bf299-117">Аргументы могут иметь только контексты Локалсервер.</span><span class="sxs-lookup"><span data-stu-id="bf299-117">Only LocalServer contexts can have arguments.</span></span>                              | <span data-ttu-id="bf299-118">Чтобы устранить эту ошибку, удалите аргумент.</span><span class="sxs-lookup"><span data-stu-id="bf299-118">To fix this error, remove the argument.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="bf299-119">CLSID "{GUID1}" в контексте "InProcServer32" указывает значение InProc по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bf299-119">CLSID '{GUID1}' in context 'InProcServer32' specifies a default InProc value.</span></span> <span data-ttu-id="bf299-120">Только контексты Локалсервер могут иметь значения INPROC по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bf299-120">Only LocalServer contexts can have default InProc values.</span></span> | <span data-ttu-id="bf299-121">Существует объект со значением INPROC по умолчанию, которое не является объектом, работающим в контекстах Локалсервер или LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="bf299-121">There is an object with a default InProc value that is not an object operating in the LocalServer or LocalServer32 contexts.</span></span> <span data-ttu-id="bf299-122">Чтобы устранить эту ошибку, удалите значение Дефлнпрок или измените контекст класса.</span><span class="sxs-lookup"><span data-stu-id="bf299-122">To fix this error, remove the DeflnProc value or change the context of the class.</span></span><br/> |



 

<span data-ttu-id="bf299-123">[Таблица классов](class-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="bf299-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="bf299-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="bf299-124">CLSID</span></span>   | <span data-ttu-id="bf299-125">Контекст</span><span class="sxs-lookup"><span data-stu-id="bf299-125">Context</span></span>        | <span data-ttu-id="bf299-126">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="bf299-126">Component\_</span></span> | <span data-ttu-id="bf299-127">дефинпрочандлер</span><span class="sxs-lookup"><span data-stu-id="bf299-127">DefInProcHandler</span></span> | <span data-ttu-id="bf299-128">Аргумент</span><span class="sxs-lookup"><span data-stu-id="bf299-128">Argument</span></span> |
|---------|----------------|-------------|------------------|----------|
| <span data-ttu-id="bf299-129">GUID1</span><span class="sxs-lookup"><span data-stu-id="bf299-129">{GUID1}</span></span> | <span data-ttu-id="bf299-130">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="bf299-130">InProcServer32</span></span> | <span data-ttu-id="bf299-131">Component1</span><span class="sxs-lookup"><span data-stu-id="bf299-131">Component1</span></span>  | <span data-ttu-id="bf299-132">инпроксервер</span><span class="sxs-lookup"><span data-stu-id="bf299-132">InProcServer</span></span>     | <span data-ttu-id="bf299-133">АРГ</span><span class="sxs-lookup"><span data-stu-id="bf299-133">Arg</span></span>      |



 

<span data-ttu-id="bf299-134">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="bf299-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="bf299-135">Компонент</span><span class="sxs-lookup"><span data-stu-id="bf299-135">Component</span></span>  | <span data-ttu-id="bf299-136">Путь</span><span class="sxs-lookup"><span data-stu-id="bf299-136">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="bf299-137">Component1</span><span class="sxs-lookup"><span data-stu-id="bf299-137">Component1</span></span> | <span data-ttu-id="bf299-138">Файл1</span><span class="sxs-lookup"><span data-stu-id="bf299-138">File1</span></span>   |



 

<span data-ttu-id="bf299-139">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="bf299-139">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="bf299-140">Файл</span><span class="sxs-lookup"><span data-stu-id="bf299-140">File</span></span>  | <span data-ttu-id="bf299-141">Имя файла</span><span class="sxs-lookup"><span data-stu-id="bf299-141">Filename</span></span> |
|-------|----------|
| <span data-ttu-id="bf299-142">Файл1</span><span class="sxs-lookup"><span data-stu-id="bf299-142">File1</span></span> | <span data-ttu-id="bf299-143">test.exe</span><span class="sxs-lookup"><span data-stu-id="bf299-143">test.exe</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bf299-144">См. также</span><span class="sxs-lookup"><span data-stu-id="bf299-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf299-145">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="bf299-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




