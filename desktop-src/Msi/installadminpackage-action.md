---
description: Действие Инсталладминпаккаже копирует базу данных продукта в точку административной установки, которая определяется свойством TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Действие Инсталладминпаккаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991683"
---
# <a name="installadminpackage-action"></a><span data-ttu-id="c127e-103">Действие Инсталладминпаккаже</span><span class="sxs-lookup"><span data-stu-id="c127e-103">InstallAdminPackage Action</span></span>

<span data-ttu-id="c127e-104">Действие Инсталладминпаккаже копирует базу данных продукта в точку административной установки, которая определяется свойством [**targetDir**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="c127e-104">The InstallAdminPackage action copies the product database to the administrative installation point, which is defined by the [**TARGETDIR**](targetdir.md) property.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c127e-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="c127e-105">Sequence Restrictions</span></span>

<span data-ttu-id="c127e-106">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="c127e-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c127e-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="c127e-107">ActionData Messages</span></span>



| <span data-ttu-id="c127e-108">Поле</span><span class="sxs-lookup"><span data-stu-id="c127e-108">Field</span></span> | <span data-ttu-id="c127e-109">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="c127e-109">Description of action data</span></span>                                 |
|-------|------------------------------------------------------------|
| <span data-ttu-id="c127e-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c127e-110">\[1\]</span></span> | <span data-ttu-id="c127e-111">Имя файлов установки.</span><span class="sxs-lookup"><span data-stu-id="c127e-111">Name of install files.</span></span>                                     |
| <span data-ttu-id="c127e-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="c127e-112">\[6\]</span></span> | <span data-ttu-id="c127e-113">Размер базы данных.</span><span class="sxs-lookup"><span data-stu-id="c127e-113">Size of database.</span></span>                                          |
| <span data-ttu-id="c127e-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="c127e-114">\[9\]</span></span> | <span data-ttu-id="c127e-115">Идентификатор административной установки — каталог Point.</span><span class="sxs-lookup"><span data-stu-id="c127e-115">Identifier of administrative installation–point directory.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c127e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c127e-116">Remarks</span></span>

<span data-ttu-id="c127e-117">Действие Инсталладминпаккаже также обновляет сводные данные базы данных и удаляет все CAB-файлы, расположенные в потоках после копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="c127e-117">The InstallAdminPackage action also updates the summary information of the database and removes any cabinet files located in streams after the database is copied.</span></span>

 

 



