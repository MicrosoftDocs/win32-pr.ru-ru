---
description: Небольшое обновление вносит изменения в один или несколько файлов приложения, которые являются слишком небольшими, чтобы гарантировать изменение кода продукта.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Небольшие обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143834"
---
# <a name="small-updates"></a><span data-ttu-id="69131-103">Небольшие обновления</span><span class="sxs-lookup"><span data-stu-id="69131-103">Small Updates</span></span>

<span data-ttu-id="69131-104">Небольшое обновление вносит изменения в один или несколько файлов приложения, которые являются слишком небольшими, чтобы гарантировать изменение кода продукта.</span><span class="sxs-lookup"><span data-stu-id="69131-104">A small update makes changes to one or more application files that are too minor to warrant changing the product code.</span></span> <span data-ttu-id="69131-105">Небольшое обновление также часто называют обновлением для быстрого устранения исправлений (QFE).</span><span class="sxs-lookup"><span data-stu-id="69131-105">A small update is also commonly referred to as a quick fix engineering (QFE) update.</span></span> <span data-ttu-id="69131-106">Небольшое обновление не допускают повторной организации дерева компонентов компонентов.</span><span class="sxs-lookup"><span data-stu-id="69131-106">A small update does not permit reorganization of the feature-component tree.</span></span>

<span data-ttu-id="69131-107">Типичное небольшое обновление изменяет только один или два файла или раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="69131-107">A typical small update changes only one or two files or a registry key.</span></span> <span data-ttu-id="69131-108">Так как небольшое обновление изменяет сведения в MSI-файле, необходимо изменить код пакета установки.</span><span class="sxs-lookup"><span data-stu-id="69131-108">Because a small update changes the information in the .msi file, the installation package code must be changed.</span></span> <span data-ttu-id="69131-109">Код пакета хранится в свойстве [**Сводка номера редакции**](revision-number-summary.md) [информационного потока сводки](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="69131-109">The package code is stored in the [**Revision Number Summary**](revision-number-summary.md) property of the [Summary Information Stream](summary-information-stream.md).</span></span>

<span data-ttu-id="69131-110">Код продукта никогда не изменяется при небольшом обновлении, поэтому все изменения, представленные небольшим обновлением, должны соответствовать рекомендациям, описанным в разделе [изменение кода продукта](changing-the-product-code.md).</span><span class="sxs-lookup"><span data-stu-id="69131-110">The product code is never changed with a small update, so all of the changes introduced by a small update have to be consistent with the guidelines described in [Changing the Product Code](changing-the-product-code.md).</span></span> <span data-ttu-id="69131-111">Обновление требует [значительных](major-upgrades.md) обновлений для изменения [**ProductCode**](productcode.md).</span><span class="sxs-lookup"><span data-stu-id="69131-111">An update requires a [major upgrade](major-upgrades.md) to change the [**ProductCode**](productcode.md).</span></span> <span data-ttu-id="69131-112">Если необходимо различать продукты без изменения кода продукта, используйте [незначительное обновление](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="69131-112">If it is necessary to differentiate between products without changing the product code, use a [minor upgrade](minor-upgrades.md).</span></span>

<span data-ttu-id="69131-113">Сведения о применении пакета обновления небольшого размера к пакету установщик Windows см. в статьях [Создание небольшого исправления обновления](creating-a-small-update-patch.md), [применение небольших обновлений путем исправления локальной установки продукта](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [применение небольших обновлений путем переустановки продукта](applying-small-updates-by-reinstalling-the-product.md)и [применение небольших обновлений путем исправления административного образа](applying-small-updates-by-patching-an-administrative-image.md).</span><span class="sxs-lookup"><span data-stu-id="69131-113">For information on how to apply a small update patch package to a Windows Installer package, see [Creating a Small Update Patch](creating-a-small-update-patch.md), [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md), and [Applying Small Updates by Patching an Administrative Image](applying-small-updates-by-patching-an-administrative-image.md).</span></span>

 

 



