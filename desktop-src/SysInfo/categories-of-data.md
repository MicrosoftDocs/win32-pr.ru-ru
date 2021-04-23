---
description: 'Перед помещением данных в реестр приложение должно разделить данные на две категории: данные конкретного компьютера и данные, относящиеся к пользователю.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Категории данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664721"
---
# <a name="categories-of-data"></a><span data-ttu-id="328cc-103">Категории данных</span><span class="sxs-lookup"><span data-stu-id="328cc-103">Categories of Data</span></span>

<span data-ttu-id="328cc-104">Перед помещением данных в реестр приложение должно разделить данные на две категории: данные конкретного компьютера и данные, относящиеся к пользователю.</span><span class="sxs-lookup"><span data-stu-id="328cc-104">Before putting data into the registry, an application should divide the data into two categories: computer-specific data and user-specific data.</span></span> <span data-ttu-id="328cc-105">Это различие заключается в том, что приложение может поддерживать нескольких пользователей, а также нахождение данных пользователя по сети и их использование в различных расположениях, что позволяет размещать данные профиля пользователя независимо от расположения.</span><span class="sxs-lookup"><span data-stu-id="328cc-105">By making this distinction, an application can support multiple users, and yet locate user-specific data over a network and use that data in different locations, allowing location-independent user profile data.</span></span> <span data-ttu-id="328cc-106">(Профиль пользователя — это набор данных конфигурации, сохраненных для каждого пользователя.)</span><span class="sxs-lookup"><span data-stu-id="328cc-106">(A user profile is a set of configuration data saved for every user.)</span></span>

<span data-ttu-id="328cc-107">При установке приложения оно должно записывать данные, относящиеся к конкретному компьютеру, в ключе **\_ локального \_ компьютера hKey** .</span><span class="sxs-lookup"><span data-stu-id="328cc-107">When the application is installed, it should record the computer-specific data under the **HKEY\_LOCAL\_MACHINE** key.</span></span> <span data-ttu-id="328cc-108">В частности, он должен создать ключи для названия компании, названия продукта и номера версии, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="328cc-108">In particular, it should create keys for the company name, product name, and version number, as shown in the following example:</span></span>

<span data-ttu-id="328cc-109">**HKey \_ Локальное \_ \\ программное обеспечение \\**_MyCompany \\ мипродукт \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="328cc-109">**HKEY\_LOCAL\_MACHINE\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

<span data-ttu-id="328cc-110">Если приложение поддерживает COM, оно должно записывать эти данные в **\_ \_ \\ \\ классы программного обеспечения локального компьютера hKey**.</span><span class="sxs-lookup"><span data-stu-id="328cc-110">If the application supports COM, it should record that data under **HKEY\_LOCAL\_MACHINE\\Software\\Classes**.</span></span>

<span data-ttu-id="328cc-111">Приложение должно записывать данные, относящиеся к пользователю, в раздел **hKey \_ текущий \_ пользователь** , как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="328cc-111">An application should record user-specific data under the **HKEY\_CURRENT\_USER** key, as shown in the following example:</span></span>

<span data-ttu-id="328cc-112">**HKey \_ Текущее \_ пользовательское \\ программное обеспечение \\**_MyCompany \\ мипродукт \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="328cc-112">**HKEY\_CURRENT\_USER\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

 

 



