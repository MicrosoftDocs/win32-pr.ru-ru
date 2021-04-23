---
description: Действие Дисаблероллбакк отключает откат для оставшейся части установки.
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: Действие Дисаблероллбакк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740e838a6dca2d97db616703faf24c590ab69bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154827"
---
# <a name="disablerollback-action"></a><span data-ttu-id="8ea56-103">Действие Дисаблероллбакк</span><span class="sxs-lookup"><span data-stu-id="8ea56-103">DisableRollback Action</span></span>

<span data-ttu-id="8ea56-104">Действие Дисаблероллбакк отключает [откат](rollback-installation.md) для оставшейся части установки.</span><span class="sxs-lookup"><span data-stu-id="8ea56-104">The DisableRollback Action disables [rollback](rollback-installation.md) for the remainder of the installation.</span></span> <span data-ttu-id="8ea56-105">Откат отключен только для действий, которые упорядочены после действия Дисаблероллбакк в таблицах последовательности.</span><span class="sxs-lookup"><span data-stu-id="8ea56-105">Rollback is disabled only for the actions that are sequenced after the DisableRollback action in the sequence tables.</span></span> <span data-ttu-id="8ea56-106">Откат будет отключен для всей установки, если действие Дисаблероллбакк является виртуализированным до [действия инсталлинитиализе](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="8ea56-106">Rollback is disabled for the entire installation if the DisableRollback action is sequenced before the [InstallInitialize action](installinitialize-action.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8ea56-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="8ea56-107">Sequence Restrictions</span></span>

<span data-ttu-id="8ea56-108">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="8ea56-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-message"></a><span data-ttu-id="8ea56-109">Сообщение Актиондата</span><span class="sxs-lookup"><span data-stu-id="8ea56-109">ActionData Message</span></span>

<span data-ttu-id="8ea56-110">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="8ea56-110">There are no ActionData messages.</span></span>

 

 



