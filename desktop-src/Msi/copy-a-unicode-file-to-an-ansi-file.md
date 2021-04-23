---
description: Файл WiToAnsi.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. В этом примере показано, как использовать скрипт для перезаписи текстового файла в Юникоде как текстового файла ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Копирование файла Юникода в файл ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910711"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a><span data-ttu-id="d6f3a-104">Копирование файла Юникода в файл ANSI</span><span class="sxs-lookup"><span data-stu-id="d6f3a-104">Copy a Unicode File to an ANSI File</span></span>

<span data-ttu-id="d6f3a-105">Файл WiToAnsi.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="d6f3a-105">The VBScript file WiToAnsi.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="d6f3a-106">В этом примере показано, как использовать скрипт для перезаписи текстового файла в Юникоде как текстового файла ANSI.</span><span class="sxs-lookup"><span data-stu-id="d6f3a-106">This sample shows how script is used to rewrite a Unicode text file as an ANSI text file.</span></span>

<span data-ttu-id="d6f3a-107">Для использования этого примера требуется CScript.exe или WScript.exe версии сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="d6f3a-107">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="d6f3a-108">Чтобы использовать CScript.exe для запуска этого образца, введите командную строку в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="d6f3a-108">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="d6f3a-109">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="d6f3a-109">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="d6f3a-110">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="d6f3a-110">or if too few arguments are specified.</span></span> <span data-ttu-id="d6f3a-111">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="d6f3a-111">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="d6f3a-112">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="d6f3a-112">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="d6f3a-113">**cscript WiToAnsi.vbs \[ путь к файлу в Юникоде \] \[ для файла ANSI\]**</span><span class="sxs-lookup"><span data-stu-id="d6f3a-113">**cscript WiToAnsi.vbs \[path to Unicode file\]\[path to ANSI file\]**</span></span>

<span data-ttu-id="d6f3a-114">Укажите текстовый файл в Юникоде, который преобразуется.</span><span class="sxs-lookup"><span data-stu-id="d6f3a-114">Specify the Unicode text file that is being converted.</span></span> <span data-ttu-id="d6f3a-115">Укажите создаваемый текстовый файл в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d6f3a-115">Specify the ANSI text file that is being created.</span></span> <span data-ttu-id="d6f3a-116">Если файл ANSI не указан, файл Юникода заменяется.</span><span class="sxs-lookup"><span data-stu-id="d6f3a-116">If no ANSI file is specified, the Unicode file is replaced.</span></span>

<span data-ttu-id="d6f3a-117">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="d6f3a-117">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="d6f3a-118">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [средства разработки установщик Windows](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d6f3a-118">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



