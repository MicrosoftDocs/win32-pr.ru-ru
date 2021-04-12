---
description: Msival2.exe — это служебная программа командной строки, которая может выполнять набор встроенных средств оценки согласованности — ICEs.
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272795"
---
# <a name="msival2exe"></a><span data-ttu-id="f61c3-103">Msival2.exe</span><span class="sxs-lookup"><span data-stu-id="f61c3-103">Msival2.exe</span></span>

<span data-ttu-id="f61c3-104">Msival2.exe — это служебная программа командной строки, которая может выполнять набор [встроенных средств оценки согласованности — ICEs](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="f61c3-104">Msival2.exe is a command line utility that can run a suite of [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="f61c3-105">Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f61c3-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="f61c3-106">Дополнительные сведения о языке ICEs и файле CUB см. в разделе [Использование встроенных средств оценки согласованности](using-internal-consistency-evaluators.md).</span><span class="sxs-lookup"><span data-stu-id="f61c3-106">For more information about ICEs and the CUB file, see [Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f61c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f61c3-107">Syntax</span></span>

<span data-ttu-id="f61c3-108">**Msival2** *{Database} {CUB file} \[ -f \] \[ -l {ФАЙЛ_ЖУРНАЛА} \] \[ -i {идентификатор Ice} \[ : {идентификатор Ice}... \] \]*</span><span class="sxs-lookup"><span data-stu-id="f61c3-108">**Msival2** *{database}{CUB file}\[-f\]\[-l {logfile}\]\[-i {ICE Id}\[:{ICE Id}...\]\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="f61c3-109">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="f61c3-109">Command Line Options</span></span>

<span data-ttu-id="f61c3-110">В Msival2.exe используются следующие параметры командной строки без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="f61c3-110">Msival2.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="f61c3-111">Вместо тире можно использовать разделитель с косой чертой.</span><span class="sxs-lookup"><span data-stu-id="f61c3-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="f61c3-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="f61c3-112">Option</span></span> | <span data-ttu-id="f61c3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f61c3-113">Description</span></span>                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f61c3-114">-f</span><span class="sxs-lookup"><span data-stu-id="f61c3-114">-f</span></span>     | <span data-ttu-id="f61c3-115">Отфильтровать все информационные сообщения от отображаемых результатов.</span><span class="sxs-lookup"><span data-stu-id="f61c3-115">Filter out all informational messages from the displayed results.</span></span> <span data-ttu-id="f61c3-116">Отображаются все остальные типы сообщений.</span><span class="sxs-lookup"><span data-stu-id="f61c3-116">All other types of messages are displayed.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="f61c3-117">-i</span><span class="sxs-lookup"><span data-stu-id="f61c3-117">-i</span></span>     | <span data-ttu-id="f61c3-118">Выполните только значение ICEs, указанное в командной строке в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="f61c3-118">Run only the ICEs listed on the command line in the order specified.</span></span> <span data-ttu-id="f61c3-119">Каждое настраиваемое действие ICE должно быть указано в том виде, в каком оно отображается в [таблице CustomAction](customaction-table.md) файла cub.</span><span class="sxs-lookup"><span data-stu-id="f61c3-119">Each ICE custom action should be listed as it appears in the [CustomAction table](customaction-table.md) of the CUB file.</span></span> <span data-ttu-id="f61c3-120">Если этот параметр не указан, средство запускает набор по умолчанию ICEs, заданный автором файла CUB.</span><span class="sxs-lookup"><span data-stu-id="f61c3-120">If this option is omitted, the tool runs the default set of ICEs specified by the author of the CUB file.</span></span> |
| <span data-ttu-id="f61c3-121">-l</span><span class="sxs-lookup"><span data-stu-id="f61c3-121">-l</span></span>     | <span data-ttu-id="f61c3-122">Запись результатов в указанный файл.</span><span class="sxs-lookup"><span data-stu-id="f61c3-122">Write results to the specified file.</span></span> <span data-ttu-id="f61c3-123">Файл не должен быть уже существует.</span><span class="sxs-lookup"><span data-stu-id="f61c3-123">The file must not already exist.</span></span> <span data-ttu-id="f61c3-124">Если файл существует, он не перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="f61c3-124">If the file exists, it is not overwritten.</span></span>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="f61c3-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f61c3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f61c3-126">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="f61c3-126">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="f61c3-127">Внутренние средства оценки согласованности — ICEs</span><span class="sxs-lookup"><span data-stu-id="f61c3-127">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
</dt> <dt>

[<span data-ttu-id="f61c3-128">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="f61c3-128">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



