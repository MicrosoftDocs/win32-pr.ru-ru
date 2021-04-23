---
description: ICE88 проверяет, что каталог, указанный в столбце Дирпроперти таблицы Инифиле, существует в установщик Windows пакете.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912304"
---
# <a name="ice88"></a><span data-ttu-id="e2d22-103">ICE88</span><span class="sxs-lookup"><span data-stu-id="e2d22-103">ICE88</span></span>

<span data-ttu-id="e2d22-104">ICE88 проверяет, что каталог, указанный в столбце Дирпроперти [таблицы инифиле](inifile-table.md) , существует в установщик Windows пакете.</span><span class="sxs-lookup"><span data-stu-id="e2d22-104">ICE88 validates that the directory referenced in the DirProperty column of the [IniFile table](inifile-table.md) exists in the Windows Installer package.</span></span> <span data-ttu-id="e2d22-105">ICE88 выдает предупреждение, если значение Дирпроперти не представляет свойства в каталоге, Аппсеарч или таблицах свойств, определенных [свойствах системной папки](property-reference.md)или свойстве, заданном настраиваемым действием типа 51.</span><span class="sxs-lookup"><span data-stu-id="e2d22-105">ICE88 issues a warning if the DirProperty value does not represent a property in the Directory, AppSearch, or Property tables, certain [system folder properties](property-reference.md), or a property set by a type 51 custom action.</span></span>

<span data-ttu-id="e2d22-106">ICE88 просматривает следующие таблицы и свойства.</span><span class="sxs-lookup"><span data-stu-id="e2d22-106">ICE88 scans the following tables and properties.</span></span>

-   [<span data-ttu-id="e2d22-107">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="e2d22-107">Directory Table</span></span>](directory-table.md)
-   [<span data-ttu-id="e2d22-108">Таблица Аппсеарч</span><span class="sxs-lookup"><span data-stu-id="e2d22-108">AppSearch Table</span></span>](appsearch-table.md)
-   [<span data-ttu-id="e2d22-109">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="e2d22-109">Property Table</span></span>](property-table.md)
-   <span data-ttu-id="e2d22-110">[Таблица CustomAction](customaction-table.md) , где настраиваемое действие является [пользовательским действием типа 51](custom-action-type-51.md)</span><span class="sxs-lookup"><span data-stu-id="e2d22-110">[CustomAction Table](customaction-table.md) , where the custom action is a [Custom Action Type 51](custom-action-type-51.md)</span></span>
-   [<span data-ttu-id="e2d22-111">**ProgramFilesFolder, свойство**</span><span class="sxs-lookup"><span data-stu-id="e2d22-111">**ProgramFilesFolder Property**</span></span>](programfilesfolder.md)
-   [<span data-ttu-id="e2d22-112">**Коммонфилесфолдер, свойство**</span><span class="sxs-lookup"><span data-stu-id="e2d22-112">**CommonFilesFolder Property**</span></span>](commonfilesfolder.md)
-   [<span data-ttu-id="e2d22-113">**Системфолдер, свойство**</span><span class="sxs-lookup"><span data-stu-id="e2d22-113">**SystemFolder Property**</span></span>](systemfolder.md)
-   [<span data-ttu-id="e2d22-114">**ProgramFiles64Folder, свойство**</span><span class="sxs-lookup"><span data-stu-id="e2d22-114">**ProgramFiles64Folder Property**</span></span>](programfiles64folder.md)
-   [<span data-ttu-id="e2d22-115">**CommonFiles64Folder, свойство**</span><span class="sxs-lookup"><span data-stu-id="e2d22-115">**CommonFiles64Folder Property**</span></span>](commonfiles64folder.md)
-   [<span data-ttu-id="e2d22-116">**System64Folder, свойство**</span><span class="sxs-lookup"><span data-stu-id="e2d22-116">**System64Folder Property**</span></span>](system64folder.md)

## <a name="result"></a><span data-ttu-id="e2d22-117">Результат</span><span class="sxs-lookup"><span data-stu-id="e2d22-117">Result</span></span>

<span data-ttu-id="e2d22-118">ICE88 отправляет следующее предупреждение.</span><span class="sxs-lookup"><span data-stu-id="e2d22-118">ICE88 posts the following warning.</span></span>



| <span data-ttu-id="e2d22-119">Предупреждение ICE88</span><span class="sxs-lookup"><span data-stu-id="e2d22-119">ICE88 Warning</span></span>                                                                                                                                                                  | <span data-ttu-id="e2d22-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e2d22-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d22-121">В записи таблицы Инифиле (Инифиле =) \[ 3 \] дирпроперти = \[ 1 \] не найден в таблицах Directory/Property/Аппсеарч/CA-Type51 и не является одним из свойств установщика.</span><span class="sxs-lookup"><span data-stu-id="e2d22-121">In the IniFile table entry (IniFile=) \[3\] the DirProperty=\[1\] is not found in Directory/Property/AppSearch/CA-Type51 tables and it is not one of the installer properties.</span></span> | <span data-ttu-id="e2d22-122">Для каждой записи в таблице Инифиле ICE88 считывает значение в столбце Дирпроперти.</span><span class="sxs-lookup"><span data-stu-id="e2d22-122">For each record in the IniFile table, ICE88 reads the value in the DirProperty column.</span></span> <span data-ttu-id="e2d22-123">ICE88 сканирует значение в таблице [Directory](directory-table.md), таблице [Аппсеарч](appsearch-table.md)и [таблице свойств](property-table.md) , а также просматривает список свойств, заданных установщиком.</span><span class="sxs-lookup"><span data-stu-id="e2d22-123">ICE88 scans for the value in the [Directory Table](directory-table.md), [AppSearch Table](appsearch-table.md), and [Property Table](property-table.md) and also scans the list of properties set by the installer.</span></span> <span data-ttu-id="e2d22-124">ICE88 отправляет это предупреждение, если значение не найдено в проверке.</span><span class="sxs-lookup"><span data-stu-id="e2d22-124">ICE88 posts this warning if the value cannot be found in the scan.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e2d22-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e2d22-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2d22-126">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="e2d22-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



