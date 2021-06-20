---
description: Сведения о перечислениях, используемых в параллельных API-интерфейсах сборок, таких как ASM_CMP_FLAGS и CREATE_ASM_NAME_OBJ_FLAGS.
ms.assetid: e73c37e3-7879-4754-b39c-91be64fc8d73
title: Параллельные перечисления сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f393ab9d8657ecaa52cad555dad5a831699687
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404747"
---
# <a name="side-by-side-assembly-enumerations"></a><span data-ttu-id="9de11-103">Параллельные перечисления сборок</span><span class="sxs-lookup"><span data-stu-id="9de11-103">Side-by-Side Assembly Enumerations</span></span>

<span data-ttu-id="9de11-104">Параллельный API сборки использует следующие перечисления.</span><span class="sxs-lookup"><span data-stu-id="9de11-104">The side-by-side assembly API uses the following enumerations.</span></span>



| <span data-ttu-id="9de11-105">Перечисление</span><span class="sxs-lookup"><span data-stu-id="9de11-105">Enumeration</span></span>                                                         | <span data-ttu-id="9de11-106">Описание</span><span class="sxs-lookup"><span data-stu-id="9de11-106">Description</span></span>                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9de11-107">**\_ \_ Флаги ASM CMP**</span><span class="sxs-lookup"><span data-stu-id="9de11-107">**ASM\_CMP\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | <span data-ttu-id="9de11-108">Используется методом [**Equals**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) для указания, какие части двух имен сборок следует сравнить.</span><span class="sxs-lookup"><span data-stu-id="9de11-108">Used by the [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) method to specify which parts of two assembly names to compare.</span></span>                                                                       |
| [<span data-ttu-id="9de11-109">**\_ \_ Флаги вывода ASM**</span><span class="sxs-lookup"><span data-stu-id="9de11-109">**ASM\_DISPLAY\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | <span data-ttu-id="9de11-110">Используется [**методом,**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) чтобы указать, какие части имени параллельной сборки следует включить в строковое представление имени.</span><span class="sxs-lookup"><span data-stu-id="9de11-110">Used by the [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) method to specify which portions of the side-by-side assembly name to include in the string representation of the name.</span></span> |
| [<span data-ttu-id="9de11-111">**\_имя ASM**</span><span class="sxs-lookup"><span data-stu-id="9de11-111">**ASM\_NAME**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | <span data-ttu-id="9de11-112">Идентификаторы свойств для пар "имя-значение" в имени параллельной сборки.</span><span class="sxs-lookup"><span data-stu-id="9de11-112">Property IDs for the name-value pairs in an side-by-side assembly name.</span></span>                                                                                                                    |
| [<span data-ttu-id="9de11-113">**СОЗДАТЬ \_ \_ имя ASM \_ \_ Флаги obj**</span><span class="sxs-lookup"><span data-stu-id="9de11-113">**CREATE\_ASM\_NAME\_OBJ\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | <span data-ttu-id="9de11-114">Используется функцией [**креатеассемблинамеобжект**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) для указания параллельного имени сборки.</span><span class="sxs-lookup"><span data-stu-id="9de11-114">Used by the [**CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) function to specify the side-by-side assembly name.</span></span>                                                               |



 

 

 



