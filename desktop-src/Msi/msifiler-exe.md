---
description: MsiFiler.exe заполняет таблицу файлов версиями, языками и размерами на основе исходного каталога. Также можно обновить таблицу Мсифилехаш с помощью хэшей файлов.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662370"
---
# <a name="msifilerexe"></a><span data-ttu-id="d76ed-104">Msifiler.exe</span><span class="sxs-lookup"><span data-stu-id="d76ed-104">Msifiler.exe</span></span>

<span data-ttu-id="d76ed-105">MsiFiler.exe заполняет [таблицу файлов](file-table.md) версиями, языками и размерами на основе исходного каталога.</span><span class="sxs-lookup"><span data-stu-id="d76ed-105">MsiFiler.exe populates the [File table](file-table.md) with file versions, languages, and sizes based upon a source directory.</span></span> <span data-ttu-id="d76ed-106">Также можно обновить [таблицу мсифилехаш](msifilehash-table.md) с помощью хэшей файлов.</span><span class="sxs-lookup"><span data-stu-id="d76ed-106">It can also update the [MsiFileHash table](msifilehash-table.md) with file hashes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d76ed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d76ed-107">Syntax</span></span>

<span data-ttu-id="d76ed-108">**msifiler.exe-d** *{Database}* **\[ -v \] \[ -h \] \[ -s алтсаурце \]**</span><span class="sxs-lookup"><span data-stu-id="d76ed-108">**msifiler.exe -d** *{database}* **\[-v\] \[-h\] \[-s ALTSOURCE\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="d76ed-109">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="d76ed-109">Command Line Options</span></span>

<span data-ttu-id="d76ed-110">В Msifiler.exe используются следующие параметры командной строки без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="d76ed-110">Msifiler.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="d76ed-111">Вместо тире можно использовать разделитель с косой чертой.</span><span class="sxs-lookup"><span data-stu-id="d76ed-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="d76ed-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="d76ed-112">Option</span></span> | <span data-ttu-id="d76ed-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="d76ed-113">Parameter</span></span>   | <span data-ttu-id="d76ed-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d76ed-114">Description</span></span>                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76ed-115">-d</span><span class="sxs-lookup"><span data-stu-id="d76ed-115">-d</span></span>     | <span data-ttu-id="d76ed-116">*database*</span><span class="sxs-lookup"><span data-stu-id="d76ed-116">*database*</span></span>  | <span data-ttu-id="d76ed-117">База данных (MSI-файл), которая должна быть обновлена.</span><span class="sxs-lookup"><span data-stu-id="d76ed-117">The database (.msi file) that is to be updated.</span></span>                                                                                                                              |
| <span data-ttu-id="d76ed-118">-v</span><span class="sxs-lookup"><span data-stu-id="d76ed-118">-v</span></span>     |             | <span data-ttu-id="d76ed-119">Использовать режим подробного вывода.</span><span class="sxs-lookup"><span data-stu-id="d76ed-119">Use verbose mode.</span></span>                                                                                                                                                            |
| <span data-ttu-id="d76ed-120">-H</span><span class="sxs-lookup"><span data-stu-id="d76ed-120">-h</span></span>     |             | <span data-ttu-id="d76ed-121">Заполнение [таблицы мсифилехаш](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="d76ed-121">Populate the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="d76ed-122">При этом создается таблица, если она еще не существует.</span><span class="sxs-lookup"><span data-stu-id="d76ed-122">This creates the table if it does not already exist.</span></span> <span data-ttu-id="d76ed-123">Таблицу Мсифилехаш можно использовать только с файлами без версий.</span><span class="sxs-lookup"><span data-stu-id="d76ed-123">The MsiFileHash table can only be used with unversioned files.</span></span> |
| <span data-ttu-id="d76ed-124">-S</span><span class="sxs-lookup"><span data-stu-id="d76ed-124">-s</span></span>     | <span data-ttu-id="d76ed-125">*алтсаурце*</span><span class="sxs-lookup"><span data-stu-id="d76ed-125">*ALTSOURCE*</span></span> | <span data-ttu-id="d76ed-126">АЛТСАУРЦЕ указывает альтернативный каталог для поиска файлов.</span><span class="sxs-lookup"><span data-stu-id="d76ed-126">ALTSOURCE specifies an alternative directory to find the files.</span></span>                                                                                                              |



 

<span data-ttu-id="d76ed-127">Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="d76ed-127">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d76ed-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d76ed-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d76ed-129">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="d76ed-129">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="d76ed-130">Использование таблицы Directory</span><span class="sxs-lookup"><span data-stu-id="d76ed-130">Using the Directory Table</span></span>](using-the-directory-table.md)
</dt> <dt>

[<span data-ttu-id="d76ed-131">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="d76ed-131">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



