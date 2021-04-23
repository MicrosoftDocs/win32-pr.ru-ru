---
description: Устойчивость — это возможность корректного восстановления приложения из ситуаций, в которых отсутствует важный компонент, или заменен несовместимой версией.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Устойчивость
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664264"
---
# <a name="resiliency"></a><span data-ttu-id="b09ac-103">Устойчивость</span><span class="sxs-lookup"><span data-stu-id="b09ac-103">Resiliency</span></span>

<span data-ttu-id="b09ac-104">Устойчивость — это возможность корректного восстановления приложения из ситуаций, в которых отсутствует важный компонент, или заменен несовместимой версией.</span><span class="sxs-lookup"><span data-stu-id="b09ac-104">Resiliency is the ability of an application to recover gracefully from situations in which a vital component is missing, or has been replaced by an incompatible version.</span></span> <span data-ttu-id="b09ac-105">Создавая пакет установки и используя [функции установщика](installer-functions.md), разработчики могут использовать установщик Windows для создания устойчивых приложений, способных восстанавливаться из таких ситуаций.</span><span class="sxs-lookup"><span data-stu-id="b09ac-105">By authoring an installation package and using the [Installer Functions](installer-functions.md), developers can use the Windows Installer to produce resilient applications capable of recovering from such situations.</span></span>

-   <span data-ttu-id="b09ac-106">Используйте исходный список установщика, чтобы повысить устойчивость приложений, использующих сетевые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b09ac-106">Use the installer's source list to increase the resiliency of applications that rely on network resources.</span></span> <span data-ttu-id="b09ac-107">Дополнительные сведения см. в разделе [устойчивость источника](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="b09ac-107">For more information, see [Source Resiliency](source-resiliency.md).</span></span>
-   <span data-ttu-id="b09ac-108">Используйте API установщика, чтобы проверить, установлен ли важный компонент, компонент, файл или версия файла.</span><span class="sxs-lookup"><span data-stu-id="b09ac-108">Use the installer's API to check whether a vital feature, component, file, or file version is installed.</span></span>
-   <span data-ttu-id="b09ac-109">Используйте API установщика для проверки пути к компоненту во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b09ac-109">Use the installer's API to check the path to a component at run time.</span></span> <span data-ttu-id="b09ac-110">Это сокращает зависимость приложения от путей статических файлов, которые обычно различаются между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="b09ac-110">This reduces your application's dependency on static file paths, which commonly differ between computers.</span></span>
-   <span data-ttu-id="b09ac-111">Используйте установщик для повторной установки поврежденных ярлыков, записей реестра и других компонентов без повторного запуска программы установки.</span><span class="sxs-lookup"><span data-stu-id="b09ac-111">Use the installer to reinstall damaged shortcuts, registry entries, and other components without having to rerun setup.</span></span>
-   <span data-ttu-id="b09ac-112">Чтобы повысить устойчивость установки продукта, оставьте включенной функцию отката.</span><span class="sxs-lookup"><span data-stu-id="b09ac-112">Increase the resiliency of your product's installation by leaving the rollback capability of the installer enabled.</span></span> <span data-ttu-id="b09ac-113">Дополнительные сведения см. в разделе [ROLLBACK Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="b09ac-113">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



