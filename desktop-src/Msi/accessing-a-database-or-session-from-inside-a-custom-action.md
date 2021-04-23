---
description: Нельзя получить доступ к сеансу установщика из настраиваемого действия, которое не является текущим сеансом установки.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Доступ к базе данных или сеансу из настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998317"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a><span data-ttu-id="59230-103">Доступ к базе данных или сеансу из настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="59230-103">Accessing a Database or Session from Inside a Custom Action</span></span>

<span data-ttu-id="59230-104">Нельзя получить доступ к сеансу установщика из настраиваемого действия, которое не является текущим сеансом установки.</span><span class="sxs-lookup"><span data-stu-id="59230-104">You cannot access an installer session from a custom action that is not the current installation session.</span></span> <span data-ttu-id="59230-105">Пользовательские действия ограничены работой только с активной базой данных сеанса и без других баз данных.</span><span class="sxs-lookup"><span data-stu-id="59230-105">Custom actions are limited to working with only the active database of the session and no other databases.</span></span> <span data-ttu-id="59230-106">Следующие установщик Windows [функции базы данных](database-functions.md) не должны вызываться из настраиваемого действия, так как они нуждаются в обработке базы данных, которая не является базой данных текущего сеанса установки.</span><span class="sxs-lookup"><span data-stu-id="59230-106">The following Windows Installer [Database Functions](database-functions.md) must not be called from a custom action, because they require a handle to a database that is not the database of the current installation session:</span></span>

[<span data-ttu-id="59230-107">**мсидатабасемерже**</span><span class="sxs-lookup"><span data-stu-id="59230-107">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[<span data-ttu-id="59230-108">**мсикреатетрансформсуммаринфо**</span><span class="sxs-lookup"><span data-stu-id="59230-108">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[<span data-ttu-id="59230-109">**мсидатабасеапплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="59230-109">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[<span data-ttu-id="59230-110">**мсидатабасекоммит**</span><span class="sxs-lookup"><span data-stu-id="59230-110">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[<span data-ttu-id="59230-111">**мсидатабасикспорт**</span><span class="sxs-lookup"><span data-stu-id="59230-111">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[<span data-ttu-id="59230-112">**мсидатабасеженератетрансформ**</span><span class="sxs-lookup"><span data-stu-id="59230-112">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[<span data-ttu-id="59230-113">**мсидатабасеимпорт**</span><span class="sxs-lookup"><span data-stu-id="59230-113">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[<span data-ttu-id="59230-114">**мсиенаблеуипревиев**</span><span class="sxs-lookup"><span data-stu-id="59230-114">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[<span data-ttu-id="59230-115">**мсижетдатабасестате**</span><span class="sxs-lookup"><span data-stu-id="59230-115">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a><span data-ttu-id="59230-116">См. также</span><span class="sxs-lookup"><span data-stu-id="59230-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59230-117">Доступ к текущему сеансу установщика из пользовательского действия</span><span class="sxs-lookup"><span data-stu-id="59230-117">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



