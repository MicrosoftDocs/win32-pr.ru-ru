---
description: Тип данных filename — это текстовая строка, содержащая имя файла или папку.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Имя файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544279"
---
# <a name="filename"></a><span data-ttu-id="4f1b4-103">Имя файла</span><span class="sxs-lookup"><span data-stu-id="4f1b4-103">Filename</span></span>

<span data-ttu-id="4f1b4-104">Тип данных filename — это текстовая строка, содержащая имя файла или папку.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-104">The Filename data type is a text string containing a file name or folder.</span></span> <span data-ttu-id="4f1b4-105">По умолчанию предполагается, что имя файла использует короткий синтаксис имени файла; то есть 8-символьное имя, точка (.) и 3-символьное расширение.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-105">By default, the file name is assumed to use short file name syntax; that is, eight-character name, period (.), and 3-character extension.</span></span> <span data-ttu-id="4f1b4-106">Необходимо всегда указывать короткое имя файла, так как может быть задано свойство [**шортфиленамес**](shortfilenames.md) или целевой том для установки может поддерживать только короткие имена файлов.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-106">A short file name must always be provided because the [**SHORTFILENAMES**](shortfilenames.md) property may be set or the target volume for the installation may only support short file names.</span></span>

<span data-ttu-id="4f1b4-107">Чтобы добавить длинное имя файла с коротким именем файла, отделите его от короткого имени файла с помощью вертикальной черты ( \| ).</span><span class="sxs-lookup"><span data-stu-id="4f1b4-107">To include a long file name with the short file name, separate it from the short file name with a vertical bar (\|).</span></span>

<span data-ttu-id="4f1b4-108">Например, следующие две строки являются допустимыми:</span><span class="sxs-lookup"><span data-stu-id="4f1b4-108">For example, the following two strings are valid:</span></span>

-   <span data-ttu-id="4f1b4-109">status.txt</span><span class="sxs-lookup"><span data-stu-id="4f1b4-109">status.txt</span></span>
-   <span data-ttu-id="4f1b4-110">пакета ISPAC ~1.txt\| Status.txt проекта</span><span class="sxs-lookup"><span data-stu-id="4f1b4-110">projec~1.txt\|Project Status.txt</span></span>

<span data-ttu-id="4f1b4-111">Короткие и длинные имена файлов не должны содержать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="4f1b4-111">Short and long file names must not contain the following characters:</span></span>

-   <span data-ttu-id="4f1b4-112">косая черта (/) или ( \\ )</span><span class="sxs-lookup"><span data-stu-id="4f1b4-112">slash (/) or (\\)</span></span>
-   <span data-ttu-id="4f1b4-113">вопросительный знак (?)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-113">question mark (?)</span></span>
-   <span data-ttu-id="4f1b4-114">Вертикальная черта ( \| )</span><span class="sxs-lookup"><span data-stu-id="4f1b4-114">vertical bar (\|)</span></span>
-   <span data-ttu-id="4f1b4-115">правая угловая скобка (>)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-115">right angle bracket (>)</span></span>
-   <span data-ttu-id="4f1b4-116">левая угловая скобка (<)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-116">left angle bracket (<)</span></span>
-   <span data-ttu-id="4f1b4-117">двоеточие (:)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-117">colon (:)</span></span>
-   <span data-ttu-id="4f1b4-118">звездочка ( \* )</span><span class="sxs-lookup"><span data-stu-id="4f1b4-118">asterisk (\*)</span></span>
-   <span data-ttu-id="4f1b4-119">Кавычки (")</span><span class="sxs-lookup"><span data-stu-id="4f1b4-119">quotation mark (")</span></span>

<span data-ttu-id="4f1b4-120">Кроме того, короткие имена файлов не должны содержать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="4f1b4-120">In addition, short file names must not contain the following characters:</span></span>

-   <span data-ttu-id="4f1b4-121">знак «плюс» (+)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-121">plus sign (+)</span></span>
-   <span data-ttu-id="4f1b4-122">запятая (,)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-122">comma (,)</span></span>
-   <span data-ttu-id="4f1b4-123">точка с запятой (;)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-123">semicolon (;)</span></span>
-   <span data-ttu-id="4f1b4-124">знак равенства (=)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-124">equals sign (=)</span></span>
-   <span data-ttu-id="4f1b4-125">левая квадратная скобка ( \[ )</span><span class="sxs-lookup"><span data-stu-id="4f1b4-125">left square bracket (\[)</span></span>
-   <span data-ttu-id="4f1b4-126">закрывающая квадратная скобка ( \] )</span><span class="sxs-lookup"><span data-stu-id="4f1b4-126">right square bracket (\])</span></span>

<span data-ttu-id="4f1b4-127">Не допускается использование пробелов перед разделителем вертикальной черты ( \| ) для короткого синтаксиса имени файла или длинного имени файла.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-127">No space is allowed preceding the vertical bar (\|) separator for the short file name/long file name syntax.</span></span> <span data-ttu-id="4f1b4-128">Короткие имена файлов не могут содержать пробел, хотя это может быть длинное имя файла.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-128">Short file names may not include a space, although a long file name may.</span></span> <span data-ttu-id="4f1b4-129">Пробел может существовать после разделителя, только если длинное имя файла начинается с пробела.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-129">A space can exist after the separator only if the long file name of the file name begins with the space.</span></span> <span data-ttu-id="4f1b4-130">Синтаксис полного пути не разрешен.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-130">No full-path syntax is allowed.</span></span>

> [!Note]  
> <span data-ttu-id="4f1b4-131">Формат столбца FileName таблицы [мсиембеддедуи](msiembeddedui-table.md) подобен типу данных Format имя_файла, за исключением того, что разделитель вертикальной черты ( \| ) для короткого имени файла или длинного имени файла недоступен.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-131">The format of the FileName column of the [MsiEmbeddedUI](msiembeddedui-table.md) table is like the format Filename data type except that the vertical bar (\|) separator for the short file name/long file name syntax is not available.</span></span>

 

 

 



