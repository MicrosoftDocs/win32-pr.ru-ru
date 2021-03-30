---
description: В 64-разрядных операционных системах установщик Windows может вызывать пользовательские действия, компилируемые для 32-разрядных или 64-разрядных систем.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Использование 64-разрядных настраиваемых действий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998907"
---
# <a name="using-64-bit-custom-actions"></a><span data-ttu-id="3eb8f-103">Использование 64-разрядных настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="3eb8f-103">Using 64-bit Custom Actions</span></span>

<span data-ttu-id="3eb8f-104">В 64-разрядных операционных системах установщик Windows может вызывать пользовательские действия, компилируемые для 32-разрядных или 64-разрядных систем.</span><span class="sxs-lookup"><span data-stu-id="3eb8f-104">On 64-bit operating systems, Windows Installer can call custom actions that are compiled for 32-bit or 64-bit systems.</span></span> <span data-ttu-id="3eb8f-105">64-разрядное пользовательское действие на основе [скриптов](scripts.md) должно быть явно помечено как 64-разрядное настраиваемое действие путем добавления бита **msidbCustomActionType64BitScript** к числовому типу настраиваемого действия в столбце Type [таблицы CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="3eb8f-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom action numeric type in the Type column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="3eb8f-106">Пользовательские действия, основанные на [исполняемых файлах](executable-files.md) или [библиотеках динамической компоновки](dynamic-link-libraries.md) , которые соответствуют 64-разрядным операционным системам, не нуждаются в включении этого дополнительного бита в столбец Type таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="3eb8f-106">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that are complied for 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction Table.</span></span>

<span data-ttu-id="3eb8f-107">Дополнительные сведения см. в статье [64-разрядные пользовательские действия](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3eb8f-107">For more information, see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

 

 



