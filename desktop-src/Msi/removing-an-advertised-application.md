---
description: Чтобы удалить приложение, установленное в объявленном состоянии, просто удалите его с помощью Мсиинсталлпродукт или Мсиконфигурепродукт. Кроме того, объявленное приложение можно удалить из командной строки. См. раздел Параметры командной строки.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Удаление объявленного приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910695"
---
# <a name="removing-an-advertised-application"></a><span data-ttu-id="9f5d6-105">Удаление объявленного приложения</span><span class="sxs-lookup"><span data-stu-id="9f5d6-105">Removing an Advertised Application</span></span>

<span data-ttu-id="9f5d6-106">Чтобы удалить приложение, установленное в объявленном состоянии, просто удалите его с помощью [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) или [**мсиконфигурепродукт**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span><span class="sxs-lookup"><span data-stu-id="9f5d6-106">To remove an application that has been installed in the advertised state, simply uninstall it using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span></span> <span data-ttu-id="9f5d6-107">Кроме того, объявленное приложение можно удалить из командной строки.</span><span class="sxs-lookup"><span data-stu-id="9f5d6-107">You can also remove an advertised application from the command line.</span></span> <span data-ttu-id="9f5d6-108">См. раздел [Параметры командной строки](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="9f5d6-108">See [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="9f5d6-109">Обратите внимание, что объявленное приложение может быть невозможно удалить, если вы создали пакет таким образом, что выполнение установки будет условным, если инструкция **не установлена**.</span><span class="sxs-lookup"><span data-stu-id="9f5d6-109">Note that you may be unable to remove an advertised application if you have authored the package in such a way that running an installation is conditional upon the statement **NOT Installed**.</span></span> <span data-ttu-id="9f5d6-110">Объявленное приложение не установлено на компьютере пользователя, и установщик не устанавливает свойство [**Installed**](installed.md) .</span><span class="sxs-lookup"><span data-stu-id="9f5d6-110">An advertised application is not installed on the user's computer and the installer does not set the [**Installed**](installed.md) Property.</span></span> <span data-ttu-id="9f5d6-111">Пакет должен быть создан таким образом, чтобы объявленные приложения можно было удалить.</span><span class="sxs-lookup"><span data-stu-id="9f5d6-111">The package must be authored so that advertised applications can be uninstalled.</span></span>

 

 



