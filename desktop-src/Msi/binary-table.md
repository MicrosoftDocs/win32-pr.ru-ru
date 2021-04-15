---
description: Двоичная таблица содержит двоичные данные для таких элементов, как точечные рисунки, анимации и значки. Двоичная таблица также используется для хранения данных настраиваемых действий. См. раздел ограничения OLE для потоков.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Двоичная таблица
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662921"
---
# <a name="binary-table"></a><span data-ttu-id="9bfbf-105">Двоичная таблица</span><span class="sxs-lookup"><span data-stu-id="9bfbf-105">Binary Table</span></span>

<span data-ttu-id="9bfbf-106">Двоичная таблица содержит двоичные данные для таких элементов, как точечные рисунки, анимации и значки.</span><span class="sxs-lookup"><span data-stu-id="9bfbf-106">The Binary table holds the binary data for items such as bitmaps, animations, and icons.</span></span> <span data-ttu-id="9bfbf-107">Двоичная таблица также используется для хранения данных настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="9bfbf-107">The binary table is also used to store data for custom actions.</span></span> <span data-ttu-id="9bfbf-108">См. раздел [ограничения OLE для потоков](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="9bfbf-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="9bfbf-109">Двоичная таблица содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="9bfbf-109">The Binary table has the following columns.</span></span>



| <span data-ttu-id="9bfbf-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="9bfbf-110">Column</span></span> | <span data-ttu-id="9bfbf-111">Type</span><span class="sxs-lookup"><span data-stu-id="9bfbf-111">Type</span></span>                         | <span data-ttu-id="9bfbf-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="9bfbf-112">Key</span></span> | <span data-ttu-id="9bfbf-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="9bfbf-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="9bfbf-114">Имя</span><span class="sxs-lookup"><span data-stu-id="9bfbf-114">Name</span></span>   | [<span data-ttu-id="9bfbf-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="9bfbf-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="9bfbf-116">Да</span><span class="sxs-lookup"><span data-stu-id="9bfbf-116">Y</span></span>   | <span data-ttu-id="9bfbf-117">Нет</span><span class="sxs-lookup"><span data-stu-id="9bfbf-117">N</span></span>        |
| <span data-ttu-id="9bfbf-118">Данные</span><span class="sxs-lookup"><span data-stu-id="9bfbf-118">Data</span></span>   | [<span data-ttu-id="9bfbf-119">Двоичный</span><span class="sxs-lookup"><span data-stu-id="9bfbf-119">Binary</span></span>](binary.md)         | <span data-ttu-id="9bfbf-120">Нет</span><span class="sxs-lookup"><span data-stu-id="9bfbf-120">N</span></span>   | <span data-ttu-id="9bfbf-121">Нет</span><span class="sxs-lookup"><span data-stu-id="9bfbf-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9bfbf-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="9bfbf-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9bfbf-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="9bfbf-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="9bfbf-124">Уникальный ключ, идентифицирующий определенные двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="9bfbf-124">A unique key that identifies the particular binary data.</span></span> <span data-ttu-id="9bfbf-125">Если двоичные данные относятся к элементу управления, ключ отображается в столбце text связанного элемента управления в [таблице управления](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="9bfbf-125">If the binary data is for a control, the key appears in the Text column of the associated control in the [Control table](control-table.md).</span></span> <span data-ttu-id="9bfbf-126">Этот ключ должен быть уникальным для всех элементов управления, для которых требуются двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="9bfbf-126">This key must be unique among all controls requiring binary data.</span></span>

</dd> <dt>

<span data-ttu-id="9bfbf-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="9bfbf-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="9bfbf-128">Неформатированные двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="9bfbf-128">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="9bfbf-129">Проверка</span><span class="sxs-lookup"><span data-stu-id="9bfbf-129">Validation</span></span>

<dl>

[<span data-ttu-id="9bfbf-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="9bfbf-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9bfbf-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="9bfbf-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9bfbf-132">ICE17</span><span class="sxs-lookup"><span data-stu-id="9bfbf-132">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="9bfbf-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="9bfbf-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



