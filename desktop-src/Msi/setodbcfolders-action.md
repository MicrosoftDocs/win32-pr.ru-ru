---
description: Действие Сетодбкфолдерс проверяет наличие существующих драйверов ODBC в системе и присваивает целевому каталогу каждого нового драйвера расположение существующего драйвера.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Действие Сетодбкфолдерс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673209"
---
# <a name="setodbcfolders-action"></a><span data-ttu-id="a541b-103">Действие Сетодбкфолдерс</span><span class="sxs-lookup"><span data-stu-id="a541b-103">SetODBCFolders Action</span></span>

<span data-ttu-id="a541b-104">Действие Сетодбкфолдерс проверяет наличие существующих драйверов ODBC в системе и присваивает целевому каталогу каждого нового драйвера расположение существующего драйвера.</span><span class="sxs-lookup"><span data-stu-id="a541b-104">The SetODBCFolders action checks for existing ODBC drivers on the system and sets the target directory of each new driver to the location of an existing driver.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a541b-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="a541b-105">Sequence Restrictions</span></span>

<span data-ttu-id="a541b-106">Действие Сетодбкфолдерс должно следовать после [действия костфинализе](costfinalize-action.md) и перед [действием инсталлвалидате](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="a541b-106">The SetODBCFolders action must come after the [CostFinalize action](costfinalize-action.md) and before the [InstallValidate action](installvalidate-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a541b-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="a541b-107">ActionData Messages</span></span>



| <span data-ttu-id="a541b-108">Поле</span><span class="sxs-lookup"><span data-stu-id="a541b-108">Field</span></span> | <span data-ttu-id="a541b-109">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="a541b-109">Description of action data</span></span>                                                          |
|-------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a541b-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a541b-110">\[1\]</span></span> | <span data-ttu-id="a541b-111">Описание драйвера.</span><span class="sxs-lookup"><span data-stu-id="a541b-111">Driver description.</span></span> <span data-ttu-id="a541b-112">Ключ драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="a541b-112">The ODBC driver key.</span></span>                                            |
| <span data-ttu-id="a541b-113">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a541b-113">\[2\]</span></span> | <span data-ttu-id="a541b-114">Исходное расположение нового драйвера.</span><span class="sxs-lookup"><span data-stu-id="a541b-114">Original folder location of the new driver.</span></span>                                         |
| <span data-ttu-id="a541b-115">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a541b-115">\[3\]</span></span> | <span data-ttu-id="a541b-116">Новое расположение папки для нового драйвера.</span><span class="sxs-lookup"><span data-stu-id="a541b-116">New folder location for the new driver.</span></span> <span data-ttu-id="a541b-117">Это расположение существующего драйвера.</span><span class="sxs-lookup"><span data-stu-id="a541b-117">This is the location of an existing driver.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a541b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a541b-118">Remarks</span></span>

<span data-ttu-id="a541b-119">Это действие помещает новый драйвер в тот же каталог, что и существующий драйвер, который заменяется.</span><span class="sxs-lookup"><span data-stu-id="a541b-119">This action places a new driver into the same directory as the existing driver being replaced.</span></span> <span data-ttu-id="a541b-120">Действие Сетодбкфолдерс использует [таблицу Directory](directory-table.md) для задания местоположений существующих драйверов, которые требуется заменить.</span><span class="sxs-lookup"><span data-stu-id="a541b-120">The SetODBCFolders action uses the [Directory table](directory-table.md) to set the locations of existing drivers that are to be replaced.</span></span>

 

 



