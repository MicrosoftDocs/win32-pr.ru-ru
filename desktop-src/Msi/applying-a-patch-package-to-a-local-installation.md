---
description: Вы можете применить небольшое обновление к локальной установке MNP2000 с примером исправления Мнппатч. MSP, созданным при формировании пакета исправлений.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Применение пакета исправлений к локальной установке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264200"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a><span data-ttu-id="8007a-103">Применение пакета исправлений к локальной установке</span><span class="sxs-lookup"><span data-stu-id="8007a-103">Applying a Patch Package to a Local Installation</span></span>

<span data-ttu-id="8007a-104">Вы можете применить небольшое обновление к локальной установке MNP2000 с примером исправления Мнппатч. MSP, созданным при [формировании пакета исправлений](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="8007a-104">You may apply the small update to a local installation of MNP2000 with the sample patch MNPpatch.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="8007a-105">Общая процедура рассматривается в разделе [применение небольших обновлений путем исправления локальной установки продукта](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="8007a-105">The general procedure is discussed in the section [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span></span>

<span data-ttu-id="8007a-106">Установите исходный продукт MNP2000 локально на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8007a-106">Install the original MNP2000 product locally on your computer.</span></span> <span data-ttu-id="8007a-107">Убедитесь, что в нем имеется ошибка Concert.txt, что небольшое обновление должно быть исправлено.</span><span class="sxs-lookup"><span data-stu-id="8007a-107">Verify that this has the error Concert.txt that the small update is to fix.</span></span> <span data-ttu-id="8007a-108">Затем запустите установку, введя следующую командную строку.</span><span class="sxs-lookup"><span data-stu-id="8007a-108">Next launch the installation by entering the following command line.</span></span>

<span data-ttu-id="8007a-109">**msiexec/p MNP2000. MSP REINSTALL = ALL REINSTALLMODE = omus**</span><span class="sxs-lookup"><span data-stu-id="8007a-109">**msiexec /p MNP2000.msp REINSTALL=ALL REINSTALLMODE=omus**</span></span>

<span data-ttu-id="8007a-110">Повторно проверьте Concert.txt, принадлежащие MNP2000, чтобы убедиться, что установщик установил небольшое обновление для исправления этого файла.</span><span class="sxs-lookup"><span data-stu-id="8007a-110">Reexamine the Concert.txt belonging to MNP2000 to verify that the installer has applied the small update to fix this file.</span></span>

<span data-ttu-id="8007a-111">Чтобы применить небольшое обновление к административному образу, см. раздел [Применение пакета исправлений в административной установке](applying-a-patch-package-to-an-administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="8007a-111">To apply the small update to an administrative image, see [Applying a Patch Package to an Administrative Installation](applying-a-patch-package-to-an-administrative-installation.md).</span></span>

[<span data-ttu-id="8007a-112">Продолжить</span><span class="sxs-lookup"><span data-stu-id="8007a-112">Continue</span></span>](applying-a-patch-package-to-an-administrative-installation.md)

 

 



