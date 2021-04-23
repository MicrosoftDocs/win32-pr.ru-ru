---
title: Перечисление ресурсов
description: В этом разделе обсуждаются функции, используемые для получения списков ресурсов.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ea7f2600f6da98cff6f16853092004a542b0f206
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105651569"
---
# <a name="enumerating-resources"></a><span data-ttu-id="328e4-103">Перечисление ресурсов</span><span class="sxs-lookup"><span data-stu-id="328e4-103">Enumerating resources</span></span>

<span data-ttu-id="328e4-104">В некоторых ситуациях может потребоваться обнаружить содержимое ресурсов неизвестного переносимого исполняемого модуля (PE).</span><span class="sxs-lookup"><span data-stu-id="328e4-104">In certain situations, you might want to discover the resource contents of an unknown portable executable (PE) module.</span></span> <span data-ttu-id="328e4-105">Windows SDK предоставляет функции перечисления ресурсов, позволяющие приложению получать списки типов ресурсов, имен и языков в указанном модуле.</span><span class="sxs-lookup"><span data-stu-id="328e4-105">The Windows SDK provides resource enumeration functions that enable your application to obtain lists of resource types, names, and languages in a specified module.</span></span>

* <span data-ttu-id="328e4-106">Функции [**енумресаурцетипев**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) и [**енумресаурцетипесексв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) предоставляют список типов ресурсов, найденных в модуле.</span><span class="sxs-lookup"><span data-stu-id="328e4-106">The [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) and [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) functions provide a list of resource types found in the module.</span></span>
* <span data-ttu-id="328e4-107">Функции [**енумресаурценамесв**](/windows/win32/api/Winbase/nf-winbase-enumresourcenamesw) и [**енумресаурценамесексв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) предоставляют имя каждого ресурса в заданном типе.</span><span class="sxs-lookup"><span data-stu-id="328e4-107">The [**EnumResourceNamesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcenamesw) and [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) functions provide the name of each resource within a given type.</span></span>
* <span data-ttu-id="328e4-108">Функции [**енумресаурцелангуажесв**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) и [**енумресаурцелангуажесексв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) предоставляют язык для каждого ресурса с заданным именем и типом.</span><span class="sxs-lookup"><span data-stu-id="328e4-108">The [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) and [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) functions provide the language of each resource of a given name and type.</span></span> 

<span data-ttu-id="328e4-109">Эти функции и связанные с ними функции обратного вызова позволяют приложению создать список всех ресурсов в модуле.</span><span class="sxs-lookup"><span data-stu-id="328e4-109">These functions and their associated callback functions enable your application to create a list of all resources in a module.</span></span> <span data-ttu-id="328e4-110">Этот процесс описан в разделе [Создание списка ресурсов](using-resources.md).</span><span class="sxs-lookup"><span data-stu-id="328e4-110">This process is described in [Creating a resource list](using-resources.md).</span></span>

## <a name="-see-also"></a><span data-ttu-id="328e4-111">— см. также</span><span class="sxs-lookup"><span data-stu-id="328e4-111">-see-also</span></span>

[<span data-ttu-id="328e4-112">Msistuff.exe пример приложения</span><span class="sxs-lookup"><span data-stu-id="328e4-112">Msistuff.exe sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
