---
description: В 64-разрядных операционных системах установщик Windows могут вызывать пользовательские действия, которые были скомпилированы для 32-или 64-разрядных систем.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: 64-разрядные пользовательские действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813369"
---
# <a name="64-bit-custom-actions"></a><span data-ttu-id="4aaa9-103">64-разрядные пользовательские действия</span><span class="sxs-lookup"><span data-stu-id="4aaa9-103">64-Bit Custom Actions</span></span>

<span data-ttu-id="4aaa9-104">В 64-разрядных операционных системах установщик Windows могут вызывать пользовательские действия, которые были скомпилированы для 32-или 64-разрядных систем.</span><span class="sxs-lookup"><span data-stu-id="4aaa9-104">On 64-bit operating systems, Windows Installer may call custom actions that have been compiled for 32-bit or 64-bit systems.</span></span>

<span data-ttu-id="4aaa9-105">64-разрядное пользовательское действие, основанное на [скриптах](scripts.md) , должно быть явно помечено как 64-разрядное настраиваемое действие путем добавления бита **msidbCustomActionType64BitScript** к числовому типу пользовательских действий в столбце Type [таблицы CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="4aaa9-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction table](customaction-table.md).</span></span>



| <span data-ttu-id="4aaa9-106">Константа</span><span class="sxs-lookup"><span data-stu-id="4aaa9-106">Constant</span></span>                             | <span data-ttu-id="4aaa9-107">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="4aaa9-107">Hexadecimal</span></span> | <span data-ttu-id="4aaa9-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="4aaa9-108">Decimal</span></span> | <span data-ttu-id="4aaa9-109">Значение</span><span class="sxs-lookup"><span data-stu-id="4aaa9-109">Meaning</span></span>                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| <span data-ttu-id="4aaa9-110">**msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="4aaa9-110">**msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="4aaa9-111">0x0001000</span><span class="sxs-lookup"><span data-stu-id="4aaa9-111">0x0001000</span></span>   | <span data-ttu-id="4aaa9-112">4096</span><span class="sxs-lookup"><span data-stu-id="4aaa9-112">4096</span></span>    | <span data-ttu-id="4aaa9-113">Это 64-разрядное настраиваемое действие, написанное в [скриптах](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="4aaa9-113">This is a 64-bit custom action written in [Scripts](scripts.md).</span></span> |



 

<span data-ttu-id="4aaa9-114">Пользовательские действия, основанные на [исполняемых файлах](executable-files.md) или [библиотеках динамической компоновки](dynamic-link-libraries.md) , которые были скомпилированы для 64-разрядных операционных систем, не обязательно должны включать этот дополнительный бит в столбец Type таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="4aaa9-114">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that have been complied for a 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction table.</span></span>

 

 



