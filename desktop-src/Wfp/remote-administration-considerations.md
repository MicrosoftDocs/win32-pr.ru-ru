---
description: Существуют некоторые соображения, которые уникальны для удаленных администраторов систем.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Рекомендации по удаленному администрированию WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702759"
---
# <a name="wfp-remote-administration-considerations"></a><span data-ttu-id="2280c-103">Рекомендации по удаленному администрированию WFP</span><span class="sxs-lookup"><span data-stu-id="2280c-103">WFP Remote Administration Considerations</span></span>

<span data-ttu-id="2280c-104">Существуют некоторые соображения, которые уникальны для удаленных администраторов систем.</span><span class="sxs-lookup"><span data-stu-id="2280c-104">There are some considerations that are unique to remotely administered systems.</span></span> <span data-ttu-id="2280c-105">Во-первых, при удаленном развертывании программ (с помощью SMS или MSI) на экране локального администратора (если он есть) отображаются диалоговые окна ошибок WFP, а не службы установки.</span><span class="sxs-lookup"><span data-stu-id="2280c-105">First, when software installation is remotely deployed (using SMS or MSI), WFP error dialog boxes are displayed on the screen of a locally logged on administrator (if present), not to the installation service.</span></span> <span data-ttu-id="2280c-106">Во-вторых, если администратор выполняет удаленное подключение к серверу терминалов и устанавливает приложение, заменяющее защищенные системные файлы, диалоговые окна ошибок WFP отображаются только в основной консоли, а не в удаленном окне администратора.</span><span class="sxs-lookup"><span data-stu-id="2280c-106">Second, if an administrator logs into a terminal server remotely and installs an application that replaces protected system files, the WFP error dialog boxes are displayed only in the main console, not the administrator's remote window.</span></span>

<span data-ttu-id="2280c-107">По этим причинам WFP подавляет свои диалоговые окна ошибок до тех пор, пока администратор не войдет в систему локально.</span><span class="sxs-lookup"><span data-stu-id="2280c-107">For these reasons, WFP suppresses its error dialog boxes until an administrator logs on locally.</span></span> <span data-ttu-id="2280c-108">Удаленные администраторы могут найти ошибки замены файлов в журнале системных событий.</span><span class="sxs-lookup"><span data-stu-id="2280c-108">Remote administrators can find file replacement errors in the system event log.</span></span>

<span data-ttu-id="2280c-109">**Windows Vista и Windows Server 2008:** Удаленное администрирование WFP не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2280c-109">**Windows Vista and Windows Server 2008:** WFP remote administration is not supported.</span></span>

 

 



