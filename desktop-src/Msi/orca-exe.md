---
description: Orca.exe является редактором таблиц базы данных для создания и редактирования пакетов установщик Windows и модулей слияния.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f17874e08fcdbfdbab38c480219579897b9896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072690"
---
# <a name="orcaexe"></a><span data-ttu-id="25823-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="25823-103">Orca.exe</span></span>

<span data-ttu-id="25823-104">Orca.exe является редактором таблиц базы данных для создания и редактирования пакетов установщик Windows и модулей слияния.</span><span class="sxs-lookup"><span data-stu-id="25823-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="25823-105">Средство предоставляет графический интерфейс для проверки, выделяя определенные записи, в которых возникают ошибки или предупреждения проверки.</span><span class="sxs-lookup"><span data-stu-id="25823-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="25823-106">Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="25823-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="25823-107">Он предоставляется в виде файла Orca.msi.</span><span class="sxs-lookup"><span data-stu-id="25823-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="25823-108">После установки компонентов Windows SDK для разработчиков установщик Windows дважды щелкните Orca.msi, чтобы установить Orca.exe файл.</span><span class="sxs-lookup"><span data-stu-id="25823-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="25823-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25823-109">Syntax</span></span>

<span data-ttu-id="25823-110">\**Orca\*\*\*\[<options>\]\[<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="25823-110">**orca** *\[<options>\]\[<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="25823-111">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="25823-111">Command Line Options</span></span>

<span data-ttu-id="25823-112">В Orca.exe используются следующие параметры командной строки без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="25823-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="25823-113">Вместо тире можно использовать разделитель с косой чертой.</span><span class="sxs-lookup"><span data-stu-id="25823-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="25823-114">Параметр</span><span class="sxs-lookup"><span data-stu-id="25823-114">Option</span></span> | <span data-ttu-id="25823-115">Описание</span><span class="sxs-lookup"><span data-stu-id="25823-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="25823-116">-Q</span><span class="sxs-lookup"><span data-stu-id="25823-116">-q</span></span>     | <span data-ttu-id="25823-117">Тихий режим</span><span class="sxs-lookup"><span data-stu-id="25823-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="25823-118">-S</span><span class="sxs-lookup"><span data-stu-id="25823-118">-s</span></span>     | <span data-ttu-id="25823-119"><*база* данных> схемой \[ "Orca. dat" — по умолчанию\]</span><span class="sxs-lookup"><span data-stu-id="25823-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="25823-120">-?</span><span class="sxs-lookup"><span data-stu-id="25823-120">-?</span></span>     | <span data-ttu-id="25823-121">Диалоговое окно справки</span><span class="sxs-lookup"><span data-stu-id="25823-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="25823-122">Orca.exe использует следующие параметры командной строки без учета регистра в модулях слияния.</span><span class="sxs-lookup"><span data-stu-id="25823-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="25823-123">Вместо тире можно использовать разделитель с косой чертой.</span><span class="sxs-lookup"><span data-stu-id="25823-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="25823-124">При выполнении слияния необходимо выполнить слияние для>-f,-m и <*sourceFile* .</span><span class="sxs-lookup"><span data-stu-id="25823-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="25823-125">Параметр</span><span class="sxs-lookup"><span data-stu-id="25823-125">Option</span></span>     | <span data-ttu-id="25823-126">Описание</span><span class="sxs-lookup"><span data-stu-id="25823-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="25823-127">-c</span><span class="sxs-lookup"><span data-stu-id="25823-127">-c</span></span>         | <span data-ttu-id="25823-128">Зафиксировать слияние в базу данных, если ошибок нет.</span><span class="sxs-lookup"><span data-stu-id="25823-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="25823-129">-!</span><span class="sxs-lookup"><span data-stu-id="25823-129">-!</span></span>         | <span data-ttu-id="25823-130">Зафиксировать слияние в базу данных, даже если возникли ошибки.</span><span class="sxs-lookup"><span data-stu-id="25823-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="25823-131">-M</span><span class="sxs-lookup"><span data-stu-id="25823-131">-m</span></span>         | <span data-ttu-id="25823-132"><*модуль слияния модулей> для* слияния с базой данных.</span><span class="sxs-lookup"><span data-stu-id="25823-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="25823-133">-f</span><span class="sxs-lookup"><span data-stu-id="25823-133">-f</span></span>         | <span data-ttu-id="25823-134">Функция \[ : Feature2 \] функции для подключения к модулю слияния.</span><span class="sxs-lookup"><span data-stu-id="25823-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="25823-135">-r</span><span class="sxs-lookup"><span data-stu-id="25823-135">-r</span></span>         | <span data-ttu-id="25823-136"><*идентификатор каталога*> запись каталога для перенаправления корневого элемента модуля.</span><span class="sxs-lookup"><span data-stu-id="25823-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="25823-137">-X</span><span class="sxs-lookup"><span data-stu-id="25823-137">-x</span></span>         | <span data-ttu-id="25823-138"><*каталог*> извлечь файлы в образ в каталоге.</span><span class="sxs-lookup"><span data-stu-id="25823-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="25823-139">-g</span><span class="sxs-lookup"><span data-stu-id="25823-139">-g</span></span>         | <span data-ttu-id="25823-140"><язык *языкового*>, используемый для открытия модуля.</span><span class="sxs-lookup"><span data-stu-id="25823-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="25823-141">-l</span><span class="sxs-lookup"><span data-stu-id="25823-141">-l</span></span>         | <span data-ttu-id="25823-142"><файл *журнала*> файл для использования в качестве журнала. Добавьте его, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="25823-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="25823-143">-i</span><span class="sxs-lookup"><span data-stu-id="25823-143">-i</span></span>         | <span data-ttu-id="25823-144"><*каталог*> извлечь файлы в исходный образ в каталоге.</span><span class="sxs-lookup"><span data-stu-id="25823-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="25823-145">-CAB</span><span class="sxs-lookup"><span data-stu-id="25823-145">-cab</span></span>       | <span data-ttu-id="25823-146"><*имя файла*> извлечь CAB-файл MSM в файл.</span><span class="sxs-lookup"><span data-stu-id="25823-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="25823-147">-лфн</span><span class="sxs-lookup"><span data-stu-id="25823-147">-lfn</span></span>       | <span data-ttu-id="25823-148">Используйте длинные имена файлов во время извлечения.</span><span class="sxs-lookup"><span data-stu-id="25823-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="25823-149">— Настройка</span><span class="sxs-lookup"><span data-stu-id="25823-149">-configure</span></span> | <span data-ttu-id="25823-150"><*filename*> настроить модуль, используя данные из файла.</span><span class="sxs-lookup"><span data-stu-id="25823-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="25823-151">См. также</span><span class="sxs-lookup"><span data-stu-id="25823-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25823-152">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="25823-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="25823-153">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="25823-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



