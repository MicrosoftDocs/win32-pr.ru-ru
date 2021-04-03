---
description: При административной установке создается исходный образ приложения или продукта в сети.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Применение небольших обновлений путем исправления административного образа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998294"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a><span data-ttu-id="64f7c-103">Применение небольших обновлений путем исправления административного образа</span><span class="sxs-lookup"><span data-stu-id="64f7c-103">Applying Small Updates by Patching an Administrative Image</span></span>

<span data-ttu-id="64f7c-104">При [административной установке](administrative-installation.md) создается исходный образ приложения или продукта в сети.</span><span class="sxs-lookup"><span data-stu-id="64f7c-104">An [administrative installation](administrative-installation.md) creates a source image of an application or product on a network.</span></span> <span data-ttu-id="64f7c-105">Пользователи рабочей группы, которые имеют доступ к этому административному образу, могут установить продукт из этого источника.</span><span class="sxs-lookup"><span data-stu-id="64f7c-105">Users in a workgroup who have access to this administrative image can install the product from this source.</span></span> <span data-ttu-id="64f7c-106">Обновление приложения для этой Рабочей группы выполняется в два этапа:</span><span class="sxs-lookup"><span data-stu-id="64f7c-106">Updating the application for this workgroup is done in two steps:</span></span>

-   <span data-ttu-id="64f7c-107">Во – первых, к административному образу можно применить небольшое исправление обновления.</span><span class="sxs-lookup"><span data-stu-id="64f7c-107">First, the small update patch can be applied to the administrative image.</span></span>
-   <span data-ttu-id="64f7c-108">Во вторых, изменения в небольшом обновлении должны распространяться на пользователей.</span><span class="sxs-lookup"><span data-stu-id="64f7c-108">Second, the changes in the small update need to be propagated to the users.</span></span>

<span data-ttu-id="64f7c-109">**Применение небольшого исправления обновления к административному образу**</span><span class="sxs-lookup"><span data-stu-id="64f7c-109">**To apply a small update patch to an administrative image**</span></span>

1.  <span data-ttu-id="64f7c-110">Получите небольшое обновление в виде [пакета исправлений](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="64f7c-110">Obtain the small update in the form of a [patch package](patch-packages.md).</span></span> <span data-ttu-id="64f7c-111">Например, небольшое обновление с именем patch. MSP.</span><span class="sxs-lookup"><span data-stu-id="64f7c-111">For example, the small update named Patch.msp.</span></span>
2.  <span data-ttu-id="64f7c-112">Получите путь к административному образу.</span><span class="sxs-lookup"><span data-stu-id="64f7c-112">Obtain the path to the administrative image.</span></span>
3.  <span data-ttu-id="64f7c-113">Из командной строки используйте:</span><span class="sxs-lookup"><span data-stu-id="64f7c-113">From the command line use:</span></span>

    <span data-ttu-id="64f7c-114">**msiexec/a** *\[ путь к административному образу. \] MSI файл* **/p** *patch. MSP*</span><span class="sxs-lookup"><span data-stu-id="64f7c-114">**msiexec /a** *\[path to administrative image .msi file\]* **/p** *patch.msp*</span></span>

4.  <span data-ttu-id="64f7c-115">При этом обновляются файлы приложения и MSI административного образа.</span><span class="sxs-lookup"><span data-stu-id="64f7c-115">This updates the application files and the .msi file of the administrative image.</span></span> <span data-ttu-id="64f7c-116">Список параметров, которые можно использовать с Msiexec.exe, см. в разделе [Параметры командной строки](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="64f7c-116">For a list of the options that can be used with Msiexec.exe, see [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="64f7c-117">Установщик Windows автоматически определяет, использует ли административный образ короткие имена файлов и задает свойство [**шортфиленамес**](shortfilenames.md) .</span><span class="sxs-lookup"><span data-stu-id="64f7c-117">Windows Installer automatically determines whether the administrative image is using short file names and sets the [**SHORTFILENAMES**](shortfilenames.md) property.</span></span>
5.  <span data-ttu-id="64f7c-118">Итоговый административный образ аналогичен тому, который был создан административной установкой с помощью полного компакт-диска, включающего обновление.</span><span class="sxs-lookup"><span data-stu-id="64f7c-118">The resulting administrative image is the same as that produced by an administrative installation using a full product CD-ROM that includes the update.</span></span> <span data-ttu-id="64f7c-119">Когда новые пользователи устанавливают приложение из этого источника, они получают обновленное приложение.</span><span class="sxs-lookup"><span data-stu-id="64f7c-119">When new users install the application from this source they receive the updated application.</span></span>

<span data-ttu-id="64f7c-120">**Распространение небольшого обновления в рабочую группу**</span><span class="sxs-lookup"><span data-stu-id="64f7c-120">**To propagate the small update to the workgroup**</span></span>

-   <span data-ttu-id="64f7c-121">Члены Рабочей группы получают изменения путем повторной установки приложения из административного образа с помощью процедуры, описанной в разделе [применение небольших обновлений путем переустановки продукта](applying-small-updates-by-reinstalling-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="64f7c-121">Members of the workgroup obtain the changes by reinstalling the application from the administrative image using the procedure described in [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md).</span></span>

 

 



