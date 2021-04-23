---
description: В этом примере показано, как создать пакет исправлений, который применяет небольшое обновление к образцу пакета установки, рассматриваемого в примере установки.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Пример небольшого обновления исправлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662978"
---
# <a name="a-small-update-patching-example"></a><span data-ttu-id="077b5-103">Пример небольшого обновления исправлений</span><span class="sxs-lookup"><span data-stu-id="077b5-103">A Small Update Patching Example</span></span>

<span data-ttu-id="077b5-104">В этом примере показано, как создать [пакет исправлений](patch-packages.md) , который применяет [небольшое обновление](small-updates.md) к образцу пакета установки, рассматриваемого в [примере установки](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="077b5-104">This example illustrates how to create a [patch package](patch-packages.md) that applies a [small update](small-updates.md) to the sample installation package discussed in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="077b5-105">Небольшое обновление вносит изменения в один или несколько файлов приложения, которые считаются слишком небольшими, чтобы гарантировать изменение кода продукта.</span><span class="sxs-lookup"><span data-stu-id="077b5-105">A small update makes changes to one or more application files that are judged to be too minor to warrant changing the product code.</span></span> <span data-ttu-id="077b5-106">Дополнительные сведения см. в разделе [Установка исправлений и обновления](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="077b5-106">For more information see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="077b5-107">В этом примере показано, как создать пакет исправлений установщик Windows, который обновляет функцию концерта гипотетического продукта MNP2000 для исправления ошибки в исходном продукте.</span><span class="sxs-lookup"><span data-stu-id="077b5-107">This example illustrates how to create a Windows Installer patch package that updates the Concert feature of the hypothetical product MNP2000 to fix an error in the original product.</span></span> <span data-ttu-id="077b5-108">В примере пакета исправлений применяется небольшое обновление продукта, которое не требует изменения кода продукта.</span><span class="sxs-lookup"><span data-stu-id="077b5-108">The example patch package applies a small update to the product that does not require changing the product code.</span></span> <span data-ttu-id="077b5-109">Дополнительные сведения о основных обновлениях см. в разделе [основные обновления](major-upgrades.md) в разделе об [исправлениях и обновлениях](patching-and-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="077b5-109">See the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section for more information about major upgrades.</span></span>

<span data-ttu-id="077b5-110">Образец пакета обновления имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="077b5-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="077b5-111">Она корректирует незначительную ошибку в расписании концерта, отображаемом функцией концерта.</span><span class="sxs-lookup"><span data-stu-id="077b5-111">It corrects a minor error in the Concert schedule displayed by the Concert feature.</span></span>
-   <span data-ttu-id="077b5-112">Он обновляет код пакета в соответствии с измененным пакетом установки.</span><span class="sxs-lookup"><span data-stu-id="077b5-112">It updates the package code to reflect the installation package has changed.</span></span>
-   <span data-ttu-id="077b5-113">Небольшое обновление можно применить путем исправления локальной установки продукта.</span><span class="sxs-lookup"><span data-stu-id="077b5-113">The small update can be applied by patching the local installation of the product.</span></span>

[<span data-ttu-id="077b5-114">Продолжить</span><span class="sxs-lookup"><span data-stu-id="077b5-114">Continue</span></span>](planning-a-small-update-patch.md)

 

 



