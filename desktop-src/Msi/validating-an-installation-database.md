---
description: Авторы пакетов установки должны всегда выполнять проверку своих пакетов, прежде чем пытаться установить пакет в первый раз и повторно запустить проверку при каждом внесении изменений в пакет.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Проверка базы данных установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896661"
---
# <a name="validating-an-installation-database"></a><span data-ttu-id="a3768-103">Проверка базы данных установки</span><span class="sxs-lookup"><span data-stu-id="a3768-103">Validating an Installation Database</span></span>

<span data-ttu-id="a3768-104">Авторы пакетов установки должны всегда выполнять проверку своих пакетов, прежде чем пытаться установить пакет в первый раз и повторно запустить проверку при каждом внесении изменений в пакет.</span><span class="sxs-lookup"><span data-stu-id="a3768-104">Authors of installation packages should always run validation on their packages before attempting to install the package for the first time and rerun validation whenever making any changes to the package.</span></span> <span data-ttu-id="a3768-105">Проверка проверяет базу данных на наличие ошибок, которые могут быть действительны по отдельности, но это приводит к неправильному поведению в контексте всей базы данных.</span><span class="sxs-lookup"><span data-stu-id="a3768-105">Validation scans the database for errors that may appear valid individually but that cause incorrect behavior in the context of the whole database.</span></span> <span data-ttu-id="a3768-106">Попытка установить пакет, который не прошел проверку, может повредить систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="a3768-106">Attempting to install a package that fails validation can damage the user's system.</span></span> <span data-ttu-id="a3768-107">См. раздел [Проверка пакетов](package-validation.md) и [внутренние средства оценки согласованности — ICEs](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="a3768-107">See the sections [Package Validation](package-validation.md) and [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="a3768-108">Образец пакета можно проверить с помощью [Orca.exe](orca-exe.md) или [Msival2.exe](msival2-exe.md).</span><span class="sxs-lookup"><span data-stu-id="a3768-108">You can validate the sample package using [Orca.exe](orca-exe.md) or [Msival2.exe](msival2-exe.md).</span></span> <span data-ttu-id="a3768-109">Чтобы просмотреть справку по Msival2.exe изменить каталоги и ввести в командной строке.</span><span class="sxs-lookup"><span data-stu-id="a3768-109">To view the help for Msival2.exe change directories and enter on the command line.</span></span>

<span data-ttu-id="a3768-110">Msival2 -?</span><span class="sxs-lookup"><span data-stu-id="a3768-110">Msival2 -?</span></span>

<span data-ttu-id="a3768-111">Файл. cub дарице. cub содержит пользовательские действия ICE, необходимые для выполнения проверки Msival2.exe.</span><span class="sxs-lookup"><span data-stu-id="a3768-111">The .cub file darice.cub contains the ICE custom actions needed by Msival2.exe to perform validation.</span></span> <span data-ttu-id="a3768-112">Проверка MNP2000.msi Enter</span><span class="sxs-lookup"><span data-stu-id="a3768-112">To validate the MNP2000.msi enter</span></span>

<span data-ttu-id="a3768-113">msival2 MNP2000.msi Дарице. cub</span><span class="sxs-lookup"><span data-stu-id="a3768-113">msival2 MNP2000.msi Darice.cub</span></span>

<span data-ttu-id="a3768-114">Описание сообщений об ошибках и предупреждений, возвращенных проверкой, см. в [справочнике по Ice](ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a3768-114">For a description of the error and warning messages returned by validation see the [ICE Reference](ice-reference.md).</span></span> <span data-ttu-id="a3768-115">Исправьте все ошибки в пакете и повторно запустите проверку по мере необходимости, пока пакет не пройдет проверку без ошибок.</span><span class="sxs-lookup"><span data-stu-id="a3768-115">Correct all the errors in the package and rerun validation as necessary until the package passes validation without errors.</span></span>

<span data-ttu-id="a3768-116">После того как пакет проходит проверку, можно установить образец пакета, щелкнув значок MNP2000.msi или из командной строки, используя [Параметры командной строки](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="a3768-116">Once the package passes validation, you can install the sample package by clicking on the MNP2000.msi icon or from the command line using the [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="a3768-117">После этого будет выполнен пример установки.</span><span class="sxs-lookup"><span data-stu-id="a3768-117">This completes the sample installation.</span></span>

## <a name="next-example"></a><span data-ttu-id="a3768-118">Следующий пример</span><span class="sxs-lookup"><span data-stu-id="a3768-118">Next example</span></span>

[<span data-ttu-id="a3768-119">Пример обновления</span><span class="sxs-lookup"><span data-stu-id="a3768-119">An Upgrade Example</span></span>](an-upgrade-example.md)

 

 



