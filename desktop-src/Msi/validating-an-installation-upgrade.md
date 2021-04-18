---
description: При каждом внесении изменений в пакет Авторы пакетов обновления должны всегда выполнять проверку своих пакетов, прежде чем пытаться установить пакет в первый раз и повторно запустить проверку.
ms.assetid: c578c020-18be-47ea-8f59-c1bbd45f1260
title: Проверка обновления установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cab7f45d3d5c19a71dac8c7a2d0150409b3a45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674493"
---
# <a name="validating-an-installation-upgrade"></a><span data-ttu-id="f8b0d-103">Проверка обновления установки</span><span class="sxs-lookup"><span data-stu-id="f8b0d-103">Validating an Installation Upgrade</span></span>

<span data-ttu-id="f8b0d-104">При каждом внесении изменений в пакет Авторы пакетов обновления должны всегда выполнять проверку своих пакетов, прежде чем пытаться установить пакет в первый раз и повторно запустить проверку.</span><span class="sxs-lookup"><span data-stu-id="f8b0d-104">Whenever making any changes to the package, authors of upgrade packages should always run validation on their packages before attempting to install the package for the first time and rerun validation.</span></span> <span data-ttu-id="f8b0d-105">Выполните проверку пакета обновления так же, как и для пакета установки.</span><span class="sxs-lookup"><span data-stu-id="f8b0d-105">Run validation on an upgrade package in the same way as for an installation package.</span></span> <span data-ttu-id="f8b0d-106">Дополнительные сведения см. в разделе [Проверка базы данных установки](validating-an-installation-database.md).</span><span class="sxs-lookup"><span data-stu-id="f8b0d-106">For details, see [Validating an Installation Database](validating-an-installation-database.md).</span></span>

<span data-ttu-id="f8b0d-107">Это завершает пример пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="f8b0d-107">This completes the sample upgrade package.</span></span> <span data-ttu-id="f8b0d-108">Чтобы установить первую установку обновления MNP2000.msi а затем установите MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="f8b0d-108">To install the upgrade first install MNP2000.msi and then install MNP2001.msi.</span></span> <span data-ttu-id="f8b0d-109">При удалении MNP2001 исходные и обновленные продукты удаляются с компьютера.</span><span class="sxs-lookup"><span data-stu-id="f8b0d-109">When you uninstall MNP2001 both the original and upgrade products are removed from your computer.</span></span>

## <a name="next-example"></a><span data-ttu-id="f8b0d-110">Следующий пример</span><span class="sxs-lookup"><span data-stu-id="f8b0d-110">Next example</span></span>

[<span data-ttu-id="f8b0d-111">Пример преобразования настройки</span><span class="sxs-lookup"><span data-stu-id="f8b0d-111">A Customization Transform Example</span></span>](a-customization-transform-example.md)

 

 



