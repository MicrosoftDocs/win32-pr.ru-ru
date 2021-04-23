---
description: При установке исправления и одного или нескольких пользовательских преобразований в приложение сначала устанавливается исправление, а затем преобразования настройки.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Исправление настроенных приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345552"
---
# <a name="patching-customized-applications"></a><span data-ttu-id="1aaa4-103">Исправление настроенных приложений</span><span class="sxs-lookup"><span data-stu-id="1aaa4-103">Patching Customized Applications</span></span>

<span data-ttu-id="1aaa4-104">При установке исправления и одного или нескольких пользовательских преобразований в приложение сначала устанавливается исправление, а затем преобразования настройки.</span><span class="sxs-lookup"><span data-stu-id="1aaa4-104">When installing a patch and one or more customization transforms to an application, the patch is typically installed first, followed by the customization transforms.</span></span> <span data-ttu-id="1aaa4-105">По проекту это исправление не нарушается последующей установкой настройки.</span><span class="sxs-lookup"><span data-stu-id="1aaa4-105">By design, the patch is not broken by the subsequent installation of the customization.</span></span> <span data-ttu-id="1aaa4-106">Однако сначала установка преобразований, а затем исправление, может нарушить настройку.</span><span class="sxs-lookup"><span data-stu-id="1aaa4-106">However, installing the transforms first, and then the patch, may break the customization.</span></span>

<span data-ttu-id="1aaa4-107">Например, перерыв в настройке может произойти, когда исправление используется для обновления продукта с версии 1 до версии 2, а преобразование настройки, которое работает для версии 1, не работает в версии 2.</span><span class="sxs-lookup"><span data-stu-id="1aaa4-107">For example, a break in the customization could occur when a patch is used to update a product from version 1 to version 2 and a customization transform that works for version 1 does not work for version 2.</span></span> <span data-ttu-id="1aaa4-108">В этом случае обновление версии не может быть применено к настроенному продукту без предварительного удаления и повторной установки исходного продукта.</span><span class="sxs-lookup"><span data-stu-id="1aaa4-108">In this case, the version update patch cannot be applied to a customized product without first uninstalling and then reinstalling the original product.</span></span>

 

 



