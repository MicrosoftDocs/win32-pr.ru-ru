---
description: Файл VBScript Manifestchk.vbs — это средство проверки, предоставляемое в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows, которое проверяет файлы манифеста приложения и сборки.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423862"
---
# <a name="manifestchkvbs"></a><span data-ttu-id="8d5d9-103">Manifestchk.vbs</span><span class="sxs-lookup"><span data-stu-id="8d5d9-103">Manifestchk.vbs</span></span>

<span data-ttu-id="8d5d9-104">Файл VBScript Manifestchk.vbs — это средство проверки, предоставляемое в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows, которое проверяет файлы манифеста приложения и сборки.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-104">The VBScript file Manifestchk.vbs is a validation tool provided in the Microsoft Windows Software Development Kit (SDK) that validates application and assembly manifest files.</span></span>

<span data-ttu-id="8d5d9-105">Для выполнения этого примера требуется сервер сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-105">Running this sample requires Windows Script Host.</span></span> <span data-ttu-id="8d5d9-106">Дополнительные сведения о сервере сценариев Windows см. в разделе "сервер сценариев Windows" Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-106">For more information about Windows Script Host, see the Windows Script Host section of the Windows SDK.</span></span> <span data-ttu-id="8d5d9-107">Сервер сценариев Windows на самом деле состоит из двух узлов.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-107">Windows Script Host is actually two hosts.</span></span> <span data-ttu-id="8d5d9-108">CScript.exe — это версия, позволяющая запускать скрипты из командной строки.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-108">CScript.exe is the version that enables you to run scripts from the command prompt.</span></span> <span data-ttu-id="8d5d9-109">CScript.exe предоставляет параметры командной строки для установки свойств скрипта.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-109">CScript.exe provides command-line switches for setting script properties.</span></span>

<span data-ttu-id="8d5d9-110">Формат командной строки следующий:</span><span class="sxs-lookup"><span data-stu-id="8d5d9-110">The command-line format is the following:</span></span>

<span data-ttu-id="8d5d9-111">**Cscript//нолого manifestchk.vbs/s:** *\[ диск: \] \[ путь \] счемафиленаме* **/m:** *\[ диск: \] \[ путь \] манифестфиленаме* **\[ /q \] /t:** *параметр*</span><span class="sxs-lookup"><span data-stu-id="8d5d9-111">**Cscript //nologo manifestchk.vbs /s:** *\[drive:\]\[path\]schemafilename* **/m:** *\[drive:\]\[path\]manifestfilename* **\[/q\] /t:** *option*</span></span>

<span data-ttu-id="8d5d9-112">Флаги, определенные для Manifestchk.vbs, описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-112">The flags defined for Manifestchk.vbs are described in the following table.</span></span>



| <span data-ttu-id="8d5d9-113">Flag</span><span class="sxs-lookup"><span data-stu-id="8d5d9-113">Flag</span></span> | <span data-ttu-id="8d5d9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8d5d9-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5d9-115">/s</span><span class="sxs-lookup"><span data-stu-id="8d5d9-115">/s</span></span>   | <span data-ttu-id="8d5d9-116">Указывает имя файла схемы манифеста для проверки манифестов.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-116">Specifies the manifest schema file name to validate manifests against.</span></span> <span data-ttu-id="8d5d9-117">См. схему в [схеме файла манифеста](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="8d5d9-117">See the schema at [Manifest File Schema](manifest-file-schema.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8d5d9-118">/m</span><span class="sxs-lookup"><span data-stu-id="8d5d9-118">/m</span></span>   | <span data-ttu-id="8d5d9-119">Указывает имя файла манифеста для проверки.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-119">Specifies the manifest file name to validate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8d5d9-120">/q</span><span class="sxs-lookup"><span data-stu-id="8d5d9-120">/q</span></span>   | <span data-ttu-id="8d5d9-121">Подавляет все выходные данные в консоли.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-121">Suppresses all output to the console.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8d5d9-122">/t</span><span class="sxs-lookup"><span data-stu-id="8d5d9-122">/t</span></span>   | <span data-ttu-id="8d5d9-123">Указывает тип файла манифеста.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-123">Specifies the type of manifest file.</span></span> <span data-ttu-id="8d5d9-124">Допустимые значения: Проверка [схемы файла манифеста](manifest-file-schema.md) манифеста [сборки](assembly-manifests.md) или [манифеста приложения](application-manifests.md) .</span><span class="sxs-lookup"><span data-stu-id="8d5d9-124">The valid values are: AM   Validate the [manifest file schema](manifest-file-schema.md) of an [assembly manifest](assembly-manifests.md) or [application manifest](application-manifests.md)</span></span><br/> <span data-ttu-id="8d5d9-125">КОМПЬЮТЕР Проверка [схемы файла конфигурации издателя](publisher-configuration-file-schema.md) [файла конфигурации издателя](publisher-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="8d5d9-125">PC   Validate the [publisher configuration file schema](publisher-configuration-file-schema.md) of a [publisher configuration file](publisher-configuration-files.md)</span></span><br/> <span data-ttu-id="8d5d9-126">AC проверяет схему файла конфигурации приложения для [файла конфигурации приложения](application-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="8d5d9-126">AC   Validate the application configuration file schema of an [application configuration file](application-configuration-files.md).</span></span><br/> |



 

<span data-ttu-id="8d5d9-127">Если флаг/q не указан, Manifestchk.vbs отображает подробные сведения о первой ошибке, обнаруженной в файле, и отображает сообщение о том, успешно ли прошел процесс проверки.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-127">If the /q flag is not specified, Manifestchk.vbs displays detailed information about the first error encountered in the file, and displays a message stating whether the validation process was successful or not.</span></span>

<span data-ttu-id="8d5d9-128">Эта программа проверяет наличие следующих средств:</span><span class="sxs-lookup"><span data-stu-id="8d5d9-128">This utility checks for the following:</span></span>

-   <span data-ttu-id="8d5d9-129">Допустимая Командная строка.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-129">A valid command line.</span></span>
-   <span data-ttu-id="8d5d9-130">Установлена версия MSXML 3.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-130">That MSXML version 3 is installed.</span></span>
-   <span data-ttu-id="8d5d9-131">В манифесте используется XML-код правильного формата.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-131">That the manifest uses well-formed XML.</span></span>
-   <span data-ttu-id="8d5d9-132">, Что манифест соглашается с предоставленной схемой.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-132">That the manifest agrees with the provided schema.</span></span> <span data-ttu-id="8d5d9-133">Обратите внимание, что Manifestchk.vbs проверяет файл манифеста на основе только того, что указано в указанной схеме.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-133">Note that Manifestchk.vbs verifies the manifest file based only on what is specified in the provided schema.</span></span> <span data-ttu-id="8d5d9-134">Пример схемы манифеста см. в разделе [Схема файла манифеста](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="8d5d9-134">For an example of a manifest schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="8d5d9-135">Cscript.exe возвращает значение 0, если процесс проверки прошел успешно, и 1, если он не был успешным.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-135">Cscript.exe returns a value of 0 if the validation process was successful and 1 if it was not successful.</span></span> <span data-ttu-id="8d5d9-136">При наличии ошибки в аргументе командной строки возвращается значение 2.</span><span class="sxs-lookup"><span data-stu-id="8d5d9-136">It returns 2 if there is an error in a command line argument.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d5d9-137">См. также</span><span class="sxs-lookup"><span data-stu-id="8d5d9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d5d9-138">Средства разработки параллельных сборок</span><span class="sxs-lookup"><span data-stu-id="8d5d9-138">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




