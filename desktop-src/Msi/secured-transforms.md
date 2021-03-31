---
description: Безопасные преобразования иногда необходимы в целях безопасности.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Безопасные преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913659"
---
# <a name="secured-transforms"></a><span data-ttu-id="38990-103">Безопасные преобразования</span><span class="sxs-lookup"><span data-stu-id="38990-103">Secured Transforms</span></span>

<span data-ttu-id="38990-104">Безопасные преобразования иногда необходимы в целях безопасности.</span><span class="sxs-lookup"><span data-stu-id="38990-104">Secured transforms are sometimes necessary for security reasons.</span></span> <span data-ttu-id="38990-105">Защищенные преобразования хранятся локально на компьютере пользователя в расположении, где в защищенной файловой системе пользователь не имеет доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="38990-105">Secured transforms are stored locally on the user's computer in a location where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="38990-106">Такие преобразования кэшируются в этом расположении во время установки или объявления пакета.</span><span class="sxs-lookup"><span data-stu-id="38990-106">Such transforms are cached in this location during the installation or advertisement of the package.</span></span> <span data-ttu-id="38990-107">Только администраторы и локальная система имеют доступ на запись к этому расположению.</span><span class="sxs-lookup"><span data-stu-id="38990-107">Only administrators and local system have write access to this location.</span></span> <span data-ttu-id="38990-108">Пользователь без прав администратора не сможет изменить файл преобразования.</span><span class="sxs-lookup"><span data-stu-id="38990-108">A non-admin user would not be able to modify the transform file.</span></span> <span data-ttu-id="38990-109">При последующих установках пакета по [требованию](installation-on-demand.md) или при [обслуживании](maintenance-installation.md) установщик использует кэшированные преобразования.</span><span class="sxs-lookup"><span data-stu-id="38990-109">During subsequent [installation-on-demand](installation-on-demand.md) or [maintenance installations](maintenance-installation.md) of the package, the installer uses the cached transforms.</span></span>

<span data-ttu-id="38990-110">Чтобы указать защищенное хранилище преобразований, задайте [политику трансформссекуре](transformssecure-policy.md), задайте свойство [**трансформссекуре**](transformssecure.md) или передайте символ @ или \| в список преобразований.</span><span class="sxs-lookup"><span data-stu-id="38990-110">To specify secured transform storage, set the [TransformsSecure policy](transformssecure-policy.md), set the [**TRANSFORMSSECURE**](transformssecure.md) property, or pass the @ or \| symbol in the transforms list.</span></span> <span data-ttu-id="38990-111">Обратите внимание, что в одном списке преобразований нельзя включать защищенные и незащищенные преобразования.</span><span class="sxs-lookup"><span data-stu-id="38990-111">Note that you cannot include secured and unsecured transforms in the same transforms list.</span></span> <span data-ttu-id="38990-112">См. раздел [применение преобразований](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="38990-112">See [Applying Transforms](applying-transforms.md).</span></span>

<span data-ttu-id="38990-113">При удалении продукта любым пользователем все защищенные преобразования для этого продукта удаляются с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="38990-113">The removal of the product by any user removes all secured transforms for that product from the user's computer.</span></span>

<span data-ttu-id="38990-114">Если установщик обнаруживает, что защищенное преобразование не доступно локально, оно пытается восстановить кэш преобразования из источника.</span><span class="sxs-lookup"><span data-stu-id="38990-114">If the installer finds that a secured transform is not locally available, it then attempts to restore the transform cache from a source.</span></span> <span data-ttu-id="38990-115">Безопасные преобразования могут быть защищены по исходному или защищенному полному пути:</span><span class="sxs-lookup"><span data-stu-id="38990-115">Secure transforms can be secure-at-source or secure-full-path:</span></span>

-   <span data-ttu-id="38990-116">[Преобразования с защитой по источнику](secure-at-source-transforms.md) , отсутствующие в локальном кэше преобразования, восстанавливаются из корня источника MSI-файла.</span><span class="sxs-lookup"><span data-stu-id="38990-116">[Secure-at-source transforms](secure-at-source-transforms.md) that are missing from the local transform cache are restored from the root of the source of the .msi file.</span></span>
-   <span data-ttu-id="38990-117">[Защищенные преобразования полного пути](secure-full-path-transforms.md) , отсутствующие в локальном кэше преобразования, восстанавливаются из исходного полного пути, указанного в списке преобразований.</span><span class="sxs-lookup"><span data-stu-id="38990-117">[Secure-full-path transforms](secure-full-path-transforms.md) that are missing from the local transform cache are restored from the original full path specified by the transforms list.</span></span>

 

 



