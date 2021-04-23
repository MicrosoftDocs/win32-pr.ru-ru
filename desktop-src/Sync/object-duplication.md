---
description: Функция Дупликатехандле создает дубликат маркера, который может использоваться другим указанным процессом.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Дублирование объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f8e0948ce55f5d25d7567346ecdec97f04b24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081122"
---
# <a name="object-duplication"></a><span data-ttu-id="db90c-103">Дублирование объектов</span><span class="sxs-lookup"><span data-stu-id="db90c-103">Object Duplication</span></span>

<span data-ttu-id="db90c-104">Функция [**дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) создает дубликат маркера, который может использоваться другим указанным процессом.</span><span class="sxs-lookup"><span data-stu-id="db90c-104">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function creates a duplicate handle that can be used by another specified process.</span></span> <span data-ttu-id="db90c-105">Этот метод совместного использования дескрипторов объектов более сложен, чем использование именованных объектов или наследования.</span><span class="sxs-lookup"><span data-stu-id="db90c-105">This method of sharing object handles is more complex than using named objects or inheritance.</span></span> <span data-ttu-id="db90c-106">Для этого требуется связь между процессом создания и процессом, в котором повторяется этот маркер.</span><span class="sxs-lookup"><span data-stu-id="db90c-106">It requires communication between the creating process and the process into which the handle is duplicated.</span></span> <span data-ttu-id="db90c-107">Необходимые сведения (значение маркера и идентификатор процесса) могут быть переданы любыми методами взаимодействия между процессами, такими как именованные каналы или именованная общая память.</span><span class="sxs-lookup"><span data-stu-id="db90c-107">The necessary information (the handle value and process identifier) can be communicated by any of the interprocess communication methods, such as named pipes or named shared memory.</span></span>

 

 
