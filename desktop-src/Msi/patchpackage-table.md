---
description: В таблице Патчпаккаже описаны все пакеты исправлений, примененные к этому продукту. Для каждого пакета исправлений предлагается уникальный идентификатор для исправления, а также сведения о образе носителя, на котором находится исправление.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Таблица Патчпаккаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272786"
---
# <a name="patchpackage-table"></a><span data-ttu-id="d2d87-104">Таблица Патчпаккаже</span><span class="sxs-lookup"><span data-stu-id="d2d87-104">PatchPackage Table</span></span>

<span data-ttu-id="d2d87-105">В таблице Патчпаккаже описаны все пакеты исправлений, примененные к этому продукту.</span><span class="sxs-lookup"><span data-stu-id="d2d87-105">The PatchPackage table describes all patch packages that have been applied to this product.</span></span> <span data-ttu-id="d2d87-106">Для каждого пакета исправлений предлагается уникальный идентификатор для исправления, а также сведения о образе носителя, на котором находится исправление.</span><span class="sxs-lookup"><span data-stu-id="d2d87-106">For each patch package, the unique identifier for the patch is provided along with information about the media image the on which the patch is located.</span></span>

<span data-ttu-id="d2d87-107">Таблица Патчпаккаже содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="d2d87-107">The PatchPackage table has the following columns.</span></span>



| <span data-ttu-id="d2d87-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="d2d87-108">Column</span></span>  | <span data-ttu-id="d2d87-109">Type</span><span class="sxs-lookup"><span data-stu-id="d2d87-109">Type</span></span>                   | <span data-ttu-id="d2d87-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="d2d87-110">Key</span></span> | <span data-ttu-id="d2d87-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="d2d87-111">Nullable</span></span> |
|---------|------------------------|-----|----------|
| <span data-ttu-id="d2d87-112">патчид</span><span class="sxs-lookup"><span data-stu-id="d2d87-112">PatchId</span></span> | [<span data-ttu-id="d2d87-113">GUID</span><span class="sxs-lookup"><span data-stu-id="d2d87-113">GUID</span></span>](guid.md)       | <span data-ttu-id="d2d87-114">Да</span><span class="sxs-lookup"><span data-stu-id="d2d87-114">Y</span></span>   | <span data-ttu-id="d2d87-115">Нет</span><span class="sxs-lookup"><span data-stu-id="d2d87-115">N</span></span>        |
| <span data-ttu-id="d2d87-116">Мультимедиа\_</span><span class="sxs-lookup"><span data-stu-id="d2d87-116">Media\_</span></span> | [<span data-ttu-id="d2d87-117">Integer</span><span class="sxs-lookup"><span data-stu-id="d2d87-117">Integer</span></span>](integer.md) | <span data-ttu-id="d2d87-118">Нет</span><span class="sxs-lookup"><span data-stu-id="d2d87-118">N</span></span>   | <span data-ttu-id="d2d87-119">Нет</span><span class="sxs-lookup"><span data-stu-id="d2d87-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d2d87-120">Столбцы</span><span class="sxs-lookup"><span data-stu-id="d2d87-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d2d87-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>патчид</span><span class="sxs-lookup"><span data-stu-id="d2d87-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span></span>
</dt> <dd>

<span data-ttu-id="d2d87-122">Этот столбец содержит уникальный идентификатор для этого конкретного исправления.</span><span class="sxs-lookup"><span data-stu-id="d2d87-122">This column contains a unique identifier for this particular patch.</span></span>

</dd> <dt>

<span data-ttu-id="d2d87-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Носител\_</span><span class="sxs-lookup"><span data-stu-id="d2d87-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_</span></span>
</dt> <dd>

<span data-ttu-id="d2d87-124">Этот столбец является внешним ключом к столбцу DiskId [таблицы Media](media-table.md) и указывает диск, содержащий пакет исправлений.</span><span class="sxs-lookup"><span data-stu-id="d2d87-124">This column is a foreign key to the DiskId column of the [Media Table](media-table.md) and indicates the disk containing the patch package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2d87-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2d87-125">Remarks</span></span>

<span data-ttu-id="d2d87-126">Таблица Патчпаккаже является обязательной в каждом пакете исправлений.</span><span class="sxs-lookup"><span data-stu-id="d2d87-126">The PatchPackage table is required in every patch package.</span></span> <span data-ttu-id="d2d87-127">Если таблица отсутствует, попытки установить исправление завершились ошибкой с ошибкой 2768: преобразование в пакете исправлений недопустимо.</span><span class="sxs-lookup"><span data-stu-id="d2d87-127">If the table is missing, attempts to install the patch fail with "Error 2768: Transform in patch package is invalid."</span></span> <span data-ttu-id="d2d87-128">Эта таблица обычно добавляется в пакет установки путем преобразования из пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="d2d87-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="d2d87-129">Обычно он не создается непосредственно в установочном пакете.</span><span class="sxs-lookup"><span data-stu-id="d2d87-129">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="d2d87-130">Проверка</span><span class="sxs-lookup"><span data-stu-id="d2d87-130">Validation</span></span>

<dl>

[<span data-ttu-id="d2d87-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="d2d87-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d2d87-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="d2d87-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



