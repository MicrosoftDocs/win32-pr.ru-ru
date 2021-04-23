---
description: Список возможных причин, по которым установщик Windows удалению не удалось удалить все файлы приложения.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Удаление потерянных файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663575"
---
# <a name="removing-stranded-files"></a><span data-ttu-id="58dfe-103">Удаление потерянных файлов</span><span class="sxs-lookup"><span data-stu-id="58dfe-103">Removing Stranded Files</span></span>

<span data-ttu-id="58dfe-104">Если файл, который должен быть удален с компьютера пользователя, остается установленным после удаления, установщик может не удалить компонент, содержащий этот файл, по одной или нескольким из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="58dfe-104">If a file that should have been removed from the user's computer remains installed after running an uninstall, the installer may not be removing the component containing the file for one or more of the following reasons:</span></span>

-   <span data-ttu-id="58dfe-105">Бит Мсидбкомпонентаттрибутесперманент был задан для компонента в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="58dfe-105">The msidbComponentAttributesPermanent bit was set for the component in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="58dfe-106">Не было указано значение для компонента в столбце ComponentId таблицы Component.</span><span class="sxs-lookup"><span data-stu-id="58dfe-106">No value was entered for the component in the ComponentId column of the Component table.</span></span>
-   <span data-ttu-id="58dfe-107">Компонент используется другим приложением или компонентом, который по-прежнему установлен.</span><span class="sxs-lookup"><span data-stu-id="58dfe-107">The component is used by another application or feature that is still installed.</span></span>
-   <span data-ttu-id="58dfe-108">В таблице [условий](condition-table.md) указано условие, которое включает функцию во время установки и отключает эту функцию во время удаления.</span><span class="sxs-lookup"><span data-stu-id="58dfe-108">There is a condition specified in the [Condition](condition-table.md) table that enables a feature during installation and disables the feature during uninstallation.</span></span>
-   <span data-ttu-id="58dfe-109">Файл ключа для компонента содержит предыдущее число ссылок в разделе **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.</span><span class="sxs-lookup"><span data-stu-id="58dfe-109">The key file for the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="58dfe-110">Компонент устанавливается в системную папку, а любой файл в компоненте имеет предыдущее число ссылок в разделе **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.</span><span class="sxs-lookup"><span data-stu-id="58dfe-110">The component is installed in the System folder and any file in the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="58dfe-111">Установщик Windows не удаляет файлы или разделы реестра, защищенные [Защита ресурсов Windows](../wfp/windows-resource-protection-portal.md) (WRP).</span><span class="sxs-lookup"><span data-stu-id="58dfe-111">The Windows Installer does not remove any files or registry keys that are protected by [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) (WRP).</span></span> <span data-ttu-id="58dfe-112">Дополнительные сведения см. [в разделе использование установщик Windows и защита ресурсов Windows](windows-resource-protection-on-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="58dfe-112">For more information, see [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).</span></span> <span data-ttu-id="58dfe-113">В Windows Server 2003, Windows XP и Windows 2000 установщик не удаляет файлы, защищенные с помощью защиты файлов Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="58dfe-113">On Windows Server 2003, Windows XP, and Windows 2000, the installer does not remove any files that are protected by Windows File Protection (WFP).</span></span> <span data-ttu-id="58dfe-114">Если файл пути ключа или ключ реестра компонента защищены с помощью WFP или WRP, установщик не удаляет компонент.</span><span class="sxs-lookup"><span data-stu-id="58dfe-114">If a component's key path file or registry key is protected by WFP or WRP, the installer does not remove the component.</span></span>
    > [!Note]  
    > <span data-ttu-id="58dfe-115">Поскольку установщик Windows не устанавливает, не обновляет или не удаляет ресурсы, защищенные WRP, не следует включать защищенные ресурсы в пакет установки.</span><span class="sxs-lookup"><span data-stu-id="58dfe-115">Because Windows Installer does not install, update, or remove any resource that is protected by WRP, you should not include protected resources in an installation package.</span></span> <span data-ttu-id="58dfe-116">Вместо этого используйте только [поддерживаемые механизмы замены ресурсов](../wfp/supported-file-replacement-mechanisms.md) , описанные в разделе [Защита ресурсов Windows](../wfp/windows-resource-protection-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="58dfe-116">Instead, use only the [supported resource replacement mechanisms](../wfp/supported-file-replacement-mechanisms.md) described in the [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) section.</span></span>

     

 

 
