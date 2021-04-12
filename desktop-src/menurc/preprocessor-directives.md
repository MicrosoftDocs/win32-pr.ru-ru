---
title: Директивы препроцессора (меню и другие ресурсы)
description: При необходимости в скрипте ресурсов можно использовать директивы, описанные в следующей таблице. Они указывают RC на выполнение действий или присвоение значений именам.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- Компилятор ресурсов, директивы препроцессора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340240"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a><span data-ttu-id="609d2-105">Директивы препроцессора (меню и другие ресурсы)</span><span class="sxs-lookup"><span data-stu-id="609d2-105">Preprocessor Directives (Menus and Other Resources)</span></span>

<span data-ttu-id="609d2-106">При необходимости в скрипте ресурсов можно использовать директивы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="609d2-106">You can use the directives described in the following table as needed in your resource script.</span></span> <span data-ttu-id="609d2-107">Они указывают RC на выполнение действий или присвоение значений именам.</span><span class="sxs-lookup"><span data-stu-id="609d2-107">They instruct RC to perform actions or to assign values to names.</span></span>



| <span data-ttu-id="609d2-108">Директива</span><span class="sxs-lookup"><span data-stu-id="609d2-108">Directive</span></span>                     | <span data-ttu-id="609d2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="609d2-109">Description</span></span>                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="609d2-110">**\#определенно**</span><span class="sxs-lookup"><span data-stu-id="609d2-110">**\#define**</span></span>](-define.md)   | <span data-ttu-id="609d2-111">Определяет указанное имя, присваивая ему заданное значение.</span><span class="sxs-lookup"><span data-stu-id="609d2-111">Defines a specified name by assigning it a given value.</span></span>               |
| [<span data-ttu-id="609d2-112">**\##elif**</span><span class="sxs-lookup"><span data-stu-id="609d2-112">**\#elif**</span></span>](-elif.md)       | <span data-ttu-id="609d2-113">Помечает необязательное предложение блока условной компиляции.</span><span class="sxs-lookup"><span data-stu-id="609d2-113">Marks an optional clause of a conditional-compilation block.</span></span>          |
| [<span data-ttu-id="609d2-114">**\#else**</span><span class="sxs-lookup"><span data-stu-id="609d2-114">**\#else**</span></span>](-else.md)       | <span data-ttu-id="609d2-115">Помечает Последнее необязательное предложение блока условной компиляции.</span><span class="sxs-lookup"><span data-stu-id="609d2-115">Marks the last optional clause of a conditional-compilation block.</span></span>    |
| [<span data-ttu-id="609d2-116">**\#endif**</span><span class="sxs-lookup"><span data-stu-id="609d2-116">**\#endif**</span></span>](-endif.md)     | <span data-ttu-id="609d2-117">Помечает конец блока условной компиляции.</span><span class="sxs-lookup"><span data-stu-id="609d2-117">Marks the end of a conditional-compilation block.</span></span>                     |
| [<span data-ttu-id="609d2-118">**\#if**</span><span class="sxs-lookup"><span data-stu-id="609d2-118">**\#if**</span></span>](-if.md)           | <span data-ttu-id="609d2-119">Условно компилирует скрипт, если указанное выражение имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="609d2-119">Conditionally compiles the script if a specified expression is true.</span></span>  |
| [<span data-ttu-id="609d2-120">**\#ifdef**</span><span class="sxs-lookup"><span data-stu-id="609d2-120">**\#ifdef**</span></span>](-ifdef.md)     | <span data-ttu-id="609d2-121">Условно компилирует скрипт, если указанное имя определено.</span><span class="sxs-lookup"><span data-stu-id="609d2-121">Conditionally compiles the script if a specified name is defined.</span></span>     |
| [<span data-ttu-id="609d2-122">**\#ifndef**</span><span class="sxs-lookup"><span data-stu-id="609d2-122">**\#ifndef**</span></span>](-ifndef.md)   | <span data-ttu-id="609d2-123">Условно компилирует скрипт, если указанное имя не определено.</span><span class="sxs-lookup"><span data-stu-id="609d2-123">Conditionally compiles the script if a specified name is not defined.</span></span> |
| [<span data-ttu-id="609d2-124">**\#относится**</span><span class="sxs-lookup"><span data-stu-id="609d2-124">**\#include**</span></span>](-include.md) | <span data-ttu-id="609d2-125">Копирует содержимое файла в файл определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="609d2-125">Copies the contents of a file into the resource-definition file.</span></span>      |
| [<span data-ttu-id="609d2-126">**\#undef**</span><span class="sxs-lookup"><span data-stu-id="609d2-126">**\#undef**</span></span>](-undef.md)     | <span data-ttu-id="609d2-127">Удаляет определение указанного имени.</span><span class="sxs-lookup"><span data-stu-id="609d2-127">Removes the definition of the specified name.</span></span>                         |



 

<span data-ttu-id="609d2-128">Чтобы определить символы для идентификаторов ресурсов, используйте директиву **\# define** , чтобы определить их в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="609d2-128">To define symbols for your resource identifiers, use the **\#define** directive to define them in a header file.</span></span> <span data-ttu-id="609d2-129">Включите этот заголовок как в скрипт ресурсов, так и в исходный код приложения.</span><span class="sxs-lookup"><span data-stu-id="609d2-129">Include this header both in the resource script and your application source code.</span></span> <span data-ttu-id="609d2-130">Аналогичным образом вы определяете значения атрибутов и стилей ресурсов, включая Windows. h, в скрипте ресурсов.</span><span class="sxs-lookup"><span data-stu-id="609d2-130">Similarly, you define the values for resource attributes and styles by including Windows.h in the resource script.</span></span>

<span data-ttu-id="609d2-131">RC обрабатывает файлы с расширениями c и h особым образом.</span><span class="sxs-lookup"><span data-stu-id="609d2-131">RC treats files with the .c and .h extensions in a special manner.</span></span> <span data-ttu-id="609d2-132">Предполагается, что файл с одним из этих расширений не содержит ресурсов.</span><span class="sxs-lookup"><span data-stu-id="609d2-132">It assumes that a file with one of these extensions does not contain resources.</span></span> <span data-ttu-id="609d2-133">Если файл имеет расширение c или h, то версия-кандидат игнорирует все строки в файле, кроме директив препроцессора.</span><span class="sxs-lookup"><span data-stu-id="609d2-133">If a file has the .c or .h file name extension, RC ignores all lines in the file except the preprocessor directives.</span></span> <span data-ttu-id="609d2-134">Таким образом, чтобы включить файл, содержащий ресурсы в другом сценарии ресурсов, предоставьте файлу расширение, отличное от. c или. h.</span><span class="sxs-lookup"><span data-stu-id="609d2-134">Therefore, to include a file that contains resources in another resource script, give the file to be included an extension other than .c or .h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="609d2-135">См. также</span><span class="sxs-lookup"><span data-stu-id="609d2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="609d2-136">Директивы pragma</span><span class="sxs-lookup"><span data-stu-id="609d2-136">Pragma Directives</span></span>](pragma-directives.md)
</dt> </dl>

 

 




