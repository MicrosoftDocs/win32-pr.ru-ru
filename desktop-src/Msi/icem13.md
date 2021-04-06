---
description: ICEM13 проверяет, что модуль слияния не содержит сборок политики издателя и конфигурации.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909023"
---
# <a name="icem13"></a><span data-ttu-id="b59aa-103">ICEM13</span><span class="sxs-lookup"><span data-stu-id="b59aa-103">ICEM13</span></span>

<span data-ttu-id="b59aa-104">ICEM13 проверяет, что модуль слияния не содержит сборок политики издателя и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b59aa-104">ICEM13 verifies that the merge module does not contain publisher policy and configuration assemblies.</span></span> <span data-ttu-id="b59aa-105">Сборки политики издателя и конфигурации не должны включаться в модули слияния, предназначенные для распространения, так как это может повлиять на другие приложения на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="b59aa-105">Publisher policy and configuration assemblies should not be included in merge modules intended for redistribution because this can affect other applications on a user's computer.</span></span>

<span data-ttu-id="b59aa-106">Этот ИЦЕМ доступен в файле Мержемод. CUB, который входит в состав пакета SDK для установщик Windows 2,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="b59aa-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="b59aa-107">Дополнительные сведения см. в разделе [Windows SDK компонентов для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="b59aa-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="b59aa-108">Результат</span><span class="sxs-lookup"><span data-stu-id="b59aa-108">Result</span></span>

<span data-ttu-id="b59aa-109">ICEM13 отправляет предупреждающее сообщение, если обнаруживает компонент, указанный в поле Component [таблицы мсиассембли](msiassembly-table.md) модуля слияния, которая является политикой издателя или сборкой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b59aa-109">ICEM13 posts a warning message if it finds a component specified in the Component field of the merge module's [MsiAssembly Table](msiassembly-table.md) that is a publisher policy or configuration assembly.</span></span>

## <a name="example"></a><span data-ttu-id="b59aa-110">Пример</span><span class="sxs-lookup"><span data-stu-id="b59aa-110">Example</span></span>

<span data-ttu-id="b59aa-111">ICEM13 отправляет следующее предупреждающее сообщение при обнаружении строки в [таблице мсиассембли](msiassembly-table.md) с компонентом " \[ 1 \] ", указанным в поле Component, которое является политикой издателя или сборкой конфигурации, включенной в модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="b59aa-111">ICEM13 posts the following warning message if it finds a row in the [MsiAssembly Table](msiassembly-table.md) with a component '\[1\]' specified in the Component field that is a publisher policy or configuration assembly that has been included in the merge module.</span></span>

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

<span data-ttu-id="b59aa-112">Можно установить политику издателя и сборки конфигурации с помощью установщик Windows, поэтому не рекомендуется распространять эти сборки в модулях слияния.</span><span class="sxs-lookup"><span data-stu-id="b59aa-112">It is possible to install publisher policy and configuration assemblies using the Windows Installer, it is not recommended that these assemblies be redistributed in merge modules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b59aa-113">См. также</span><span class="sxs-lookup"><span data-stu-id="b59aa-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b59aa-114">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="b59aa-114">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



