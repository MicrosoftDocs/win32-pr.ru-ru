---
description: Если таблица в модуле слияния указана в таблице Модулеигноретабле, она не объединяется в MSI-файл.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Таблица Модулеигноретабле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272268"
---
# <a name="moduleignoretable-table"></a><span data-ttu-id="87143-103">Таблица Модулеигноретабле</span><span class="sxs-lookup"><span data-stu-id="87143-103">ModuleIgnoreTable Table</span></span>

<span data-ttu-id="87143-104">Если таблица в модуле слияния указана в таблице Модулеигноретабле, она не объединяется в MSI-файл.</span><span class="sxs-lookup"><span data-stu-id="87143-104">If a table in the merge module is listed in the ModuleIgnoreTable table, it is not merged into the .msi file.</span></span> <span data-ttu-id="87143-105">Если таблица уже существует в MSI-файле, слияние не изменяется.</span><span class="sxs-lookup"><span data-stu-id="87143-105">If the table already exists in the .msi file, it is not modified by the merge.</span></span> <span data-ttu-id="87143-106">Таким образом, таблицы в Модулеигноретабле могут содержать ненужные данные после слияния.</span><span class="sxs-lookup"><span data-stu-id="87143-106">The tables in the ModuleIgnoreTable can therefore contain data that is unneeded after the merge.</span></span>

<span data-ttu-id="87143-107">Таблица Модулеигноретабле содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="87143-107">The ModuleIgnoreTable table has the following columns.</span></span>



| <span data-ttu-id="87143-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="87143-108">Column</span></span> | <span data-ttu-id="87143-109">Type</span><span class="sxs-lookup"><span data-stu-id="87143-109">Type</span></span>                         | <span data-ttu-id="87143-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="87143-110">Key</span></span> | <span data-ttu-id="87143-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="87143-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="87143-112">Таблица</span><span class="sxs-lookup"><span data-stu-id="87143-112">Table</span></span>  | [<span data-ttu-id="87143-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="87143-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="87143-114">Да</span><span class="sxs-lookup"><span data-stu-id="87143-114">Y</span></span>   | <span data-ttu-id="87143-115">Нет</span><span class="sxs-lookup"><span data-stu-id="87143-115">No</span></span>       |



 

## <a name="columns"></a><span data-ttu-id="87143-116">Столбцы</span><span class="sxs-lookup"><span data-stu-id="87143-116">Columns</span></span>

<dl> <dt>

<span data-ttu-id="87143-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Таблица</span><span class="sxs-lookup"><span data-stu-id="87143-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="87143-118">Имя таблицы в модуле слияния, который не должен быть объединен в MSI-файл.</span><span class="sxs-lookup"><span data-stu-id="87143-118">Name of the table in the merge module that is not to be merged into the .msi file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87143-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87143-119">Remarks</span></span>

<span data-ttu-id="87143-120">Чтобы максимально ограничить размер файла MSM, разработчикам рекомендуется удалить неиспользуемые таблицы из модулей, предназначенных для повторного распространения, а не перечислить эти таблицы в таблице Модулеигноретабле.</span><span class="sxs-lookup"><span data-stu-id="87143-120">To minimize the size of the .msm file, it is recommended that developers remove unused tables from modules intended for redistribution rather than listing these tables in the ModuleIgnoreTable table.</span></span>

 

 



