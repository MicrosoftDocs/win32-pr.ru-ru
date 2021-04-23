---
description: Модули слияния по сути являются упрощенными MSI-файлами, то есть расширением имени файла для пакета установки установщик Windows. Стандартный модуль слияния имеет расширение имени файла MSM.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: О модулях слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345172"
---
# <a name="about-merge-modules"></a><span data-ttu-id="0de60-104">О модулях слияния</span><span class="sxs-lookup"><span data-stu-id="0de60-104">About Merge Modules</span></span>

<span data-ttu-id="0de60-105">Модули слияния по сути являются упрощенными MSI-файлами, то есть расширением имени файла для пакета установки установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="0de60-105">Merge modules are essentially simplified .msi files, which is the file name extension for a Windows Installer installation package.</span></span> <span data-ttu-id="0de60-106">Стандартный модуль слияния имеет расширение имени файла MSM.</span><span class="sxs-lookup"><span data-stu-id="0de60-106">A standard merge module has an .msm file name extension.</span></span>

<span data-ttu-id="0de60-107">Модуль слияния не может быть установлен отдельно, так как в нем отсутствуют некоторые важные таблицы базы данных, имеющиеся в базе данных установки.</span><span class="sxs-lookup"><span data-stu-id="0de60-107">A merge module cannot be installed alone because its lacks some vital database tables that are present in an installation database.</span></span> <span data-ttu-id="0de60-108">Модули слияния также содержат дополнительные таблицы, уникальные для себя.</span><span class="sxs-lookup"><span data-stu-id="0de60-108">Merge modules also contain additional tables that are unique to themselves.</span></span> <span data-ttu-id="0de60-109">Чтобы установить сведения, доставляемые модулем слияния с приложением, необходимо сначала выполнить слияние модуля с MSI-файлом приложения.</span><span class="sxs-lookup"><span data-stu-id="0de60-109">To install the information delivered by a merge module with an application, the module must first be merged into the application's .msi file.</span></span>

<span data-ttu-id="0de60-110">Модуль слияния состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="0de60-110">A merge module consists of the following parts:</span></span>

-   <span data-ttu-id="0de60-111">[База данных модуля слияния](merge-module-database.md) , содержащая свойства установки и логику установки, предоставляемую модулем слияния.</span><span class="sxs-lookup"><span data-stu-id="0de60-111">A [Merge Module Database](merge-module-database.md) containing the installation properties and setup logic being delivered by the merge module.</span></span>
-   <span data-ttu-id="0de60-112">[Ссылка на сводный информационный поток модуля слияния](merge-module-summary-information-stream-reference.md) , описывающий модуль.</span><span class="sxs-lookup"><span data-stu-id="0de60-112">A [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md) describing the module.</span></span>
-   <span data-ttu-id="0de60-113">CAB-файл [MergeModule.CABinet](mergemodule-cabinet.md) , хранящийся как поток внутри модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="0de60-113">A [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file stored as a stream inside the merge module.</span></span> <span data-ttu-id="0de60-114">Этот CAB-файл содержит все файлы, необходимые для компонентов, предоставляемых модулем слияния.</span><span class="sxs-lookup"><span data-stu-id="0de60-114">This cabinet contains all the files required by the components delivered by the merge module.</span></span>

<span data-ttu-id="0de60-115">[Модули слияния с несколькими языками](multiple-language-merge-modules.md) могут доставлять компоненты в пакет установки на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="0de60-115">[Multiple language merge modules](multiple-language-merge-modules.md) can deliver components to an installation package in multiple languages.</span></span> <span data-ttu-id="0de60-116">В модуле слияния с несколькими языками база данных содержит свойства установки и логику для более чем одного языка, а MergeModule.CABный CAB-файл inet включает все файлы, необходимые для установки компонентов со всеми языками, поддерживаемыми модулем.</span><span class="sxs-lookup"><span data-stu-id="0de60-116">In a multiple language merge module the database contains the installation properties and logic for more than one language and the MergeModule.CABinet cabinet includes all the files necessary to install components with all the languages supported by the module.</span></span>

 

 



