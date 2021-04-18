---
description: Действие Инсталлсфпкаталогфиле устанавливает каталоги, используемые Windows Me для защиты файлов Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Действие Инсталлсфпкаталогфиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682479"
---
# <a name="installsfpcatalogfile-action"></a><span data-ttu-id="94676-103">Действие Инсталлсфпкаталогфиле</span><span class="sxs-lookup"><span data-stu-id="94676-103">InstallSFPCatalogFile Action</span></span>

<span data-ttu-id="94676-104">Действие Инсталлсфпкаталогфиле устанавливает каталоги, используемые Windows Me для защиты файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="94676-104">The InstallSFPCatalogFile action installs the catalogs used by Windows Me for Windows File Protection.</span></span> <span data-ttu-id="94676-105">Инсталлсфпкаталогфиле запрашивает [таблицу компонентов](component-table.md), [таблицу файлов](file-table.md), таблицу [филесфпкаталог](filesfpcatalog-table.md) и [таблицу сфпкаталог](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="94676-105">InstallSFPCatalogFile queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and [SFPCatalog table](sfpcatalog-table.md).</span></span> <span data-ttu-id="94676-106">Каталоги устанавливаются, если они связаны с файлом в компоненте, настроенном для локальной установки, или если они связаны с восстанавливаемым файлом в локально установленном компоненте.</span><span class="sxs-lookup"><span data-stu-id="94676-106">Catalogs are installed if they are associated with a file in a component that is set for local installation or if they are associated with a file being repaired in a locally installed component.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="94676-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="94676-107">Sequence Restrictions</span></span>

<span data-ttu-id="94676-108">Действие Инсталлсфпкаталогфиле должно быть упорядочено до [инсталлфилес](installfiles-action.md) и после [костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="94676-108">The InstallSFPCatalogFile action must be sequenced before [InstallFiles](installfiles-action.md) and after [CostFinalize](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="94676-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="94676-109">ActionData Messages</span></span>



| <span data-ttu-id="94676-110">Поле</span><span class="sxs-lookup"><span data-stu-id="94676-110">Field</span></span> | <span data-ttu-id="94676-111">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="94676-111">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="94676-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="94676-112">\[1\]</span></span> | <span data-ttu-id="94676-113">Имя устанавливаемого каталога.</span><span class="sxs-lookup"><span data-stu-id="94676-113">Name of the catalog being installed.</span></span>                          |
| <span data-ttu-id="94676-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="94676-114">\[2\]</span></span> | <span data-ttu-id="94676-115">Имя каталога, от которого зависит Установка этого каталога.</span><span class="sxs-lookup"><span data-stu-id="94676-115">Name of the catalog this catalog's installation depends upon.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="94676-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94676-116">Remarks</span></span>

<span data-ttu-id="94676-117">Каталог, который зависит от другого каталога, установленного после родительского каталога.</span><span class="sxs-lookup"><span data-stu-id="94676-117">A catalog that is dependent on another catalog installed after the parent catalog.</span></span>

 

 



