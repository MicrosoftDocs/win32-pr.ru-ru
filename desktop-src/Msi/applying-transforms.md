---
description: Свойство TRANSFORMs содержит список преобразований для пакета установки. Установщик применяет все преобразования в списке преобразования во всех установках, объявлениях, установке по запросу или при обслуживании пакета.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Применение преобразований
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2367e02396ec33e517f8abfe579060c0a0986be2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909095"
---
# <a name="applying-transforms"></a><span data-ttu-id="e10cf-104">Применение преобразований</span><span class="sxs-lookup"><span data-stu-id="e10cf-104">Applying Transforms</span></span>

<span data-ttu-id="e10cf-105">Свойство [**TRANSFORMS**](transforms.md) содержит список преобразований для пакета установки.</span><span class="sxs-lookup"><span data-stu-id="e10cf-105">The [**TRANSFORMS**](transforms.md) property contains the list of transforms for an installation package.</span></span> <span data-ttu-id="e10cf-106">Установщик применяет все преобразования в списке преобразования во всех установках, объявлениях, установке по запросу или при обслуживании пакета.</span><span class="sxs-lookup"><span data-stu-id="e10cf-106">The installer applies all the transforms in the transforms list at every installation, advertisement, installation-on-demand, or maintenance installation of the package.</span></span>

<span data-ttu-id="e10cf-107">Свойство [**TRANSFORMS**](transforms.md) задается путем указания списка преобразований в командной строке. Однако при использовании [параметра командной строки](command-line-options.md)/жм или/жу список преобразований должен быть указан с помощью параметра/t.</span><span class="sxs-lookup"><span data-stu-id="e10cf-107">The [**TRANSFORMS**](transforms.md) property is set by specifying the list of transforms on the command line; however, when using either the /jm or /ju [command line option](command-line-options.md), the transforms list must be specified using the /t option.</span></span>

<span data-ttu-id="e10cf-108">Обратите внимание, что список преобразований не может быть изменен после установки и может быть удален только путем удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="e10cf-108">Note that the transforms list cannot be modified once installed and can only be removed by uninstalling the application.</span></span>

> [!Note]  
> <span data-ttu-id="e10cf-109">Пакет установщик Windows может применять не более 255 преобразований при установке приложения или обновления.</span><span class="sxs-lookup"><span data-stu-id="e10cf-109">A Windows Installer package can apply no more than 255 transforms when installing an application or update.</span></span> <span data-ttu-id="e10cf-110">Если требуется много преобразований, следует устранить необходимость их объединения и предыдущие преобразования.</span><span class="sxs-lookup"><span data-stu-id="e10cf-110">When many transforms are necessary, they should be combined and previous obsolete transforms should be eliminated.</span></span>

 

<span data-ttu-id="e10cf-111">В следующей таблице приведены примеры различных преобразований строк, которые можно добавить в список преобразований.</span><span class="sxs-lookup"><span data-stu-id="e10cf-111">The following table provides examples of various transforms strings that could be added to the transforms list.</span></span>



| <span data-ttu-id="e10cf-112">Преобразует строку</span><span class="sxs-lookup"><span data-stu-id="e10cf-112">Transforms string</span></span>                                                                                                              | <span data-ttu-id="e10cf-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e10cf-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10cf-114">прев форму. MST;: transform3. MST;.</span><span class="sxs-lookup"><span data-stu-id="e10cf-114">transform1.mst;:transform2.mst;:transform3.mst</span></span>                                                                                 | <span data-ttu-id="e10cf-115">Преобразования в формате Form2. MST и transform3. MST являются [встроенными преобразованиями](embedded-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e10cf-115">Transform2.mst and transform3.mst are [embedded transforms](embedded-transforms.md).</span></span> <span data-ttu-id="e10cf-116">Transform. MST — это [безопасное преобразование в исходном](secure-at-source-transforms.md) виде, только если задано [**свойство трансформссекуре**](transformssecure.md) или [трансформссекуре](transformssecure-policy.md) . в противном случае [Transform является незащищенным преобразованием](unsecured-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e10cf-116">transform1.mst is a [secure-at-source transform](secure-at-source-transforms.md) only if the [**TRANSFORMSSECURE**](transformssecure.md) property or [TransformsSecure policy](transformssecure-policy.md) is set, otherwise transform1 is an [unsecured transform](unsecured-transforms.md).</span></span> |
| <span data-ttu-id="e10cf-117">\\\\\\путь к общей папке сервера \\ — файл \\ Form1. MST;: "Form2. MST"</span><span class="sxs-lookup"><span data-stu-id="e10cf-117">\\\\server\\share\\path\\transform1.mst;:transform2.mst</span></span>                                                                        | <span data-ttu-id="e10cf-118">Преобразование Form2. MST является [встроенным преобразованием](embedded-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e10cf-118">Transform2.mst is an [embedded transform](embedded-transforms.md).</span></span> <span data-ttu-id="e10cf-119">Transform. MST — это [Преобразование с безопасным полным путем](secure-full-path-transforms.md) только в том случае, если задано свойство [**трансформссекуре**](transformssecure.md) или [трансформссекуре](transformssecure-policy.md) . в противном случае [Transform является незащищенным преобразованием](unsecured-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e10cf-119">transform1.mst is a [secure-full-path transform](secure-full-path-transforms.md) only if the [**TRANSFORMSSECURE**](transformssecure.md) property or [TransformsSecure policy](transformssecure-policy.md) is set, otherwise transform1 is an [unsecured transform](unsecured-transforms.md).</span></span>                   |
| <span data-ttu-id="e10cf-120">@: reform2. MST; прев форму. MST @transform1.mst ;: "Form2. MST"</span><span class="sxs-lookup"><span data-stu-id="e10cf-120">@:transform2.mst;transform1.mst @transform1.mst;:transform2.mst</span></span><br/>                                                     | <span data-ttu-id="e10cf-121">Преобразование Form2. MST является встроенным преобразованием.</span><span class="sxs-lookup"><span data-stu-id="e10cf-121">Transform2.mst is an embedded transform.</span></span> <span data-ttu-id="e10cf-122">Преобразование Form1. MST — это автономные [преобразования с защитой по источнику](secure-at-source-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e10cf-122">transform1.mst is a stand-alone [secure-at-source transforms](secure-at-source-transforms.md).</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="e10cf-123">\|\\\\\\путь к общей папке сервера — файл \\ \\ Form1. MST;: "Form2. MST \| :", "[Form2. MST; \\ \\ " \\путь к общей папке сервера — файл \\ \\ Form1. MST</span><span class="sxs-lookup"><span data-stu-id="e10cf-123">\|\\\\server\\share\\path\\transform1.mst;:transform2.mst \|:transform2.mst;\\\\server\\share\\path\\transform1.mst</span></span><br/> | <span data-ttu-id="e10cf-124">Преобразование Form2. MST является встроенным преобразованием.</span><span class="sxs-lookup"><span data-stu-id="e10cf-124">Transform2.mst is an embedded transform.</span></span> <span data-ttu-id="e10cf-125">Преобразование Form1. MST — это автономные [преобразования с безопасным полным путем](secure-full-path-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e10cf-125">transform1.mst is a Standalone [secure-full-path transforms](secure-full-path-transforms.md).</span></span>                                                                                                                                                                                                                                                 |



 

 

 




