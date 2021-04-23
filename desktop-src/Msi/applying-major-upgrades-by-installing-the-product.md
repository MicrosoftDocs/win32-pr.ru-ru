---
description: Основное обновление можно применить, установив новый установочный пакет для обновленного продукта.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Применение основных обновлений путем установки продукта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650728"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a><span data-ttu-id="7cbfe-103">Применение основных обновлений путем установки продукта</span><span class="sxs-lookup"><span data-stu-id="7cbfe-103">Applying Major Upgrades by Installing the Product</span></span>

<span data-ttu-id="7cbfe-104">Основное обновление можно применить, установив новый установочный пакет для обновленного продукта.</span><span class="sxs-lookup"><span data-stu-id="7cbfe-104">A major upgrade can be applied by installing the new installation package for the upgraded product.</span></span> <span data-ttu-id="7cbfe-105">Поскольку основные обновления получают код продукта, отличный от исходного продукта, установка обновления должна рассматриваться как установка нового продукта.</span><span class="sxs-lookup"><span data-stu-id="7cbfe-105">Because major upgrades get a different product code than the original product, installing the upgrade must be treated as an installation of a new product.</span></span> <span data-ttu-id="7cbfe-106">Обновление можно просто установить как другой продукт.</span><span class="sxs-lookup"><span data-stu-id="7cbfe-106">The upgrade can simply be installed like another product.</span></span> <span data-ttu-id="7cbfe-107">Новый пакет установки может выполнять удаление старого продукта, включая [таблицу обновления](upgrade-table.md) , а также действие [Финдрелатедпродуктс](findrelatedproducts-action.md) и [действие RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="7cbfe-107">You can have the new installation package handle the removal of the old product by including the [Upgrade table](upgrade-table.md) and the [FindRelatedProducts action](findrelatedproducts-action.md) and [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

<span data-ttu-id="7cbfe-108">**Распространение крупного обновления до текущих пользователей из командной строки**</span><span class="sxs-lookup"><span data-stu-id="7cbfe-108">**To propagate a major upgrade to current users from the command line**</span></span>

-   <span data-ttu-id="7cbfe-109">В командной строке используйте команду: **msiexec/i \[** _путь к обновленному файлу MSI_ .*_\]_*</span><span class="sxs-lookup"><span data-stu-id="7cbfe-109">From the command line, use: **msiexec /i \[**_path to updated msi file_*_\]_*</span></span>

<span data-ttu-id="7cbfe-110">**Распространение крупного обновления до текущих пользователей из программы**</span><span class="sxs-lookup"><span data-stu-id="7cbfe-110">**To propagate a major upgrade to current users from a program**</span></span>

-   <span data-ttu-id="7cbfe-111">В программе вызовите [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) и укажите путь к обновленному MSI-файлу.</span><span class="sxs-lookup"><span data-stu-id="7cbfe-111">From a program, call [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) and specify the path to the updated msi file.</span></span>

 

 



