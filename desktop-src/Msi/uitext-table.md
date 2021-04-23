---
description: Таблица Уитекст содержит локализованные версии некоторых строк, используемых в пользовательском интерфейсе. Эти строки не являются частью какой бы то ни было другой таблицы. Таблица Уитекст предназначена для строк, которые не имеют логического места в какой-либо другой таблице.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: Таблица Уитекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143426"
---
# <a name="uitext-table"></a><span data-ttu-id="9644b-105">Таблица Уитекст</span><span class="sxs-lookup"><span data-stu-id="9644b-105">UIText Table</span></span>

<span data-ttu-id="9644b-106">Таблица Уитекст содержит локализованные версии некоторых строк, используемых в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="9644b-106">The UIText table contains the localized versions of some of the strings used in the user interface.</span></span> <span data-ttu-id="9644b-107">Эти строки не являются частью какой бы то ни было другой таблицы.</span><span class="sxs-lookup"><span data-stu-id="9644b-107">These strings are not part of any other table.</span></span> <span data-ttu-id="9644b-108">Таблица Уитекст предназначена для строк, которые не имеют логического места в какой-либо другой таблице.</span><span class="sxs-lookup"><span data-stu-id="9644b-108">The UIText table is for strings that have no logical place in any other table.</span></span>

<span data-ttu-id="9644b-109">Таблица Уитекст содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="9644b-109">The UIText table has the following columns.</span></span>



| <span data-ttu-id="9644b-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="9644b-110">Column</span></span> | <span data-ttu-id="9644b-111">Type</span><span class="sxs-lookup"><span data-stu-id="9644b-111">Type</span></span>                         | <span data-ttu-id="9644b-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="9644b-112">Key</span></span> | <span data-ttu-id="9644b-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="9644b-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="9644b-114">Ключ</span><span class="sxs-lookup"><span data-stu-id="9644b-114">Key</span></span>    | [<span data-ttu-id="9644b-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="9644b-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="9644b-116">Да</span><span class="sxs-lookup"><span data-stu-id="9644b-116">Y</span></span>   | <span data-ttu-id="9644b-117">Нет</span><span class="sxs-lookup"><span data-stu-id="9644b-117">N</span></span>        |
| <span data-ttu-id="9644b-118">Текст</span><span class="sxs-lookup"><span data-stu-id="9644b-118">Text</span></span>   | [<span data-ttu-id="9644b-119">Text</span><span class="sxs-lookup"><span data-stu-id="9644b-119">Text</span></span>](text.md)             | <span data-ttu-id="9644b-120">Нет</span><span class="sxs-lookup"><span data-stu-id="9644b-120">N</span></span>   | <span data-ttu-id="9644b-121">Да</span><span class="sxs-lookup"><span data-stu-id="9644b-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9644b-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="9644b-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9644b-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел</span><span class="sxs-lookup"><span data-stu-id="9644b-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="9644b-124">Уникальный ключ, определяющий определенную строку.</span><span class="sxs-lookup"><span data-stu-id="9644b-124">A unique key that identifies the particular string.</span></span>

</dd> <dt>

<span data-ttu-id="9644b-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Полнотекстовым</span><span class="sxs-lookup"><span data-stu-id="9644b-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="9644b-126">Локализованная версия строки.</span><span class="sxs-lookup"><span data-stu-id="9644b-126">The localized version of the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9644b-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9644b-127">Remarks</span></span>

<span data-ttu-id="9644b-128">Некоторые элементы управления используют таблицу Уитекст в качестве источника строк.</span><span class="sxs-lookup"><span data-stu-id="9644b-128">Some controls use the UIText table as a source of strings.</span></span> <span data-ttu-id="9644b-129">Сведения о том, какие строки требуются в этой таблице для каждого конкретного элемента управления, см. в разделе отдельные элементы управления в [справочнике по пользовательскому интерфейсу](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9644b-129">For information about which strings are required in this table for each particular control, see the individual controls in the [User Interface Reference](user-interface-reference.md).</span></span>

## <a name="validation"></a><span data-ttu-id="9644b-130">Проверка</span><span class="sxs-lookup"><span data-stu-id="9644b-130">Validation</span></span>

<dl>

[<span data-ttu-id="9644b-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="9644b-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9644b-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="9644b-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



