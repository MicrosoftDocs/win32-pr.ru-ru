---
description: Действие BindImage привязывает каждый исполняемый файл или библиотеку DLL, которые должны быть привязаны к импортируемым им библиотекам DLL.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Действие BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909056"
---
# <a name="bindimage-action"></a><span data-ttu-id="8701e-103">Действие BindImage</span><span class="sxs-lookup"><span data-stu-id="8701e-103">BindImage Action</span></span>

<span data-ttu-id="8701e-104">Действие BindImage привязывает каждый исполняемый файл или библиотеку DLL, которые должны быть привязаны к импортируемым им библиотекам DLL.</span><span class="sxs-lookup"><span data-stu-id="8701e-104">The BindImage action binds each executable or DLL that must be bound to the DLLs imported by it.</span></span> <span data-ttu-id="8701e-105">Действие BindImage действует для каждого файла в таблице [BindImage](bindimage-table.md) , но только для тех, которые должны быть установлены локально.</span><span class="sxs-lookup"><span data-stu-id="8701e-105">The BindImage action acts on each file in the [BindImage](bindimage-table.md) table, but only those that are to be installed locally.</span></span> <span data-ttu-id="8701e-106">Установщик рассчитывает виртуальный адрес каждой функции, импортированной из всех библиотек DLL, а затем сохраняет вычисленный виртуальный адрес в [*таблице адресов импорта*](i-gly.md) импортируемого образа (IAT).</span><span class="sxs-lookup"><span data-stu-id="8701e-106">The installer computes the virtual address of each function imported from all DLLs, then saves the computed virtual address in the importing image's [*import address table*](i-gly.md) (IAT).</span></span>

<span data-ttu-id="8701e-107">Действие BindImage внутренне вызывает API Windows **биндимажеекс** .</span><span class="sxs-lookup"><span data-stu-id="8701e-107">The BindImage Action internally calls the **BindImageEx** Windows API.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8701e-108">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="8701e-108">Sequence Restrictions</span></span>

<span data-ttu-id="8701e-109">Действие BindImage должно следовать после действия [инсталлфилес](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8701e-109">The BindImage action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8701e-110">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="8701e-110">ActionData Messages</span></span>



| <span data-ttu-id="8701e-111">Поле</span><span class="sxs-lookup"><span data-stu-id="8701e-111">Field</span></span> | <span data-ttu-id="8701e-112">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="8701e-112">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="8701e-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8701e-113">\[1\]</span></span> | <span data-ttu-id="8701e-114">Идентификатор исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="8701e-114">File identifier of executable.</span></span> |



 

 

 



