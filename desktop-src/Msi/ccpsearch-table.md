---
description: Таблица Ккпсеарч содержит список подписей файлов, используемых для программы проверки соответствия (CCP). По крайней мере один из этих файлов должен присутствовать на компьютере пользователя, чтобы пользователь был в соответствии с программой.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Таблица Ккпсеарч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662911"
---
# <a name="ccpsearch-table"></a><span data-ttu-id="334a4-104">Таблица Ккпсеарч</span><span class="sxs-lookup"><span data-stu-id="334a4-104">CCPSearch Table</span></span>

<span data-ttu-id="334a4-105">Таблица Ккпсеарч содержит список подписей файлов, используемых для программы проверки соответствия (CCP).</span><span class="sxs-lookup"><span data-stu-id="334a4-105">The CCPSearch table contains the list of file signatures used for the Compliance Checking Program (CCP).</span></span> <span data-ttu-id="334a4-106">По крайней мере один из этих файлов должен присутствовать на компьютере пользователя, чтобы пользователь был в соответствии с программой.</span><span class="sxs-lookup"><span data-stu-id="334a4-106">At least one of these files needs to be present on a user's computer for the user to be in compliance with the program.</span></span>

<span data-ttu-id="334a4-107">Таблица Ккпсеарч содержит следующий столбец.</span><span class="sxs-lookup"><span data-stu-id="334a4-107">The CCPSearch table has the following column.</span></span>



| <span data-ttu-id="334a4-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="334a4-108">Column</span></span>      | <span data-ttu-id="334a4-109">Type</span><span class="sxs-lookup"><span data-stu-id="334a4-109">Type</span></span>                         | <span data-ttu-id="334a4-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="334a4-110">Key</span></span> | <span data-ttu-id="334a4-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="334a4-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="334a4-112">Образец\_</span><span class="sxs-lookup"><span data-stu-id="334a4-112">Signature\_</span></span> | [<span data-ttu-id="334a4-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="334a4-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="334a4-114">Да</span><span class="sxs-lookup"><span data-stu-id="334a4-114">Y</span></span>   | <span data-ttu-id="334a4-115">Нет</span><span class="sxs-lookup"><span data-stu-id="334a4-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="334a4-116">Столбец</span><span class="sxs-lookup"><span data-stu-id="334a4-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="334a4-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Образец\_</span><span class="sxs-lookup"><span data-stu-id="334a4-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="334a4-118">Сигнатура \_ представляет собой уникальную сигнатуру файла и является также внешним ключом в таблицах [Signature](signature-table.md), [реглокатор](reglocator-table.md), [инилокатор](inilocator-table.md), [комплокатор](complocator-table.md)и [дрлокатор](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="334a4-118">The Signature\_ represents a unique file signature and is also the external key into the [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="334a4-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="334a4-119">Remarks</span></span>

<span data-ttu-id="334a4-120">Эта таблица упоминается при выполнении [действия ккпсеарч](ccpsearch-action.md) или [рмккпсеарч](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="334a4-120">This table is referred to when the [CCPSearch action](ccpsearch-action.md) or the [RMCCPSearch action](rmccpsearch-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="334a4-121">Проверка</span><span class="sxs-lookup"><span data-stu-id="334a4-121">Validation</span></span>

<dl>

[<span data-ttu-id="334a4-122">ICE03</span><span class="sxs-lookup"><span data-stu-id="334a4-122">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="334a4-123">ICE06</span><span class="sxs-lookup"><span data-stu-id="334a4-123">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="334a4-124">ICE32</span><span class="sxs-lookup"><span data-stu-id="334a4-124">ICE32</span></span>](ice32.md)  
</dl>

 

 



