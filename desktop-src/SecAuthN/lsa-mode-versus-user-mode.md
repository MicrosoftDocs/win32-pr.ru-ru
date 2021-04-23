---
description: Если пакет безопасности SSP/AP функционирует как пакет проверки подлинности, он загружается в пространство процессов локального центра безопасности (LSA) и считается в режиме LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: В режиме LSA и в пользовательском режиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081292"
---
# <a name="lsa-mode-vs-user-mode"></a><span data-ttu-id="0e489-103">В режиме LSA и в пользовательском режиме</span><span class="sxs-lookup"><span data-stu-id="0e489-103">LSA Mode vs. User Mode</span></span>

<span data-ttu-id="0e489-104">Если [*пакет безопасности*](../secgloss/s-gly.md) SSP/AP функционирует как [*пакет проверки подлинности*](../secgloss/a-gly.md), он загружается в пространство процессов [*локального центра безопасности*](../secgloss/l-gly.md) (LSA) и считается в режиме LSA.</span><span class="sxs-lookup"><span data-stu-id="0e489-104">When an SSP/AP [*security package*](../secgloss/s-gly.md) is functioning as an [*authentication package*](../secgloss/a-gly.md), it is loaded into the process space of the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) and is said to be in LSA mode.</span></span> <span data-ttu-id="0e489-105">Вход приложений доступ к функциям пакета проверки подлинности с помощью [функций LSA logon](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0e489-105">Logon applications access authentication package functionality using the [LSA Logon Functions](authentication-functions.md).</span></span> <span data-ttu-id="0e489-106">Разработчики могут использовать функции поддержки LSA, доступные только для пакетов безопасности в режиме LSA, чтобы реализовать более сложные пакеты проверки подлинности, чем поддерживалось ранее.</span><span class="sxs-lookup"><span data-stu-id="0e489-106">Developers can use LSA support functions available only to LSA-mode security packages to implement more sophisticated authentication packages than previously supported.</span></span>

<span data-ttu-id="0e489-107">Когда [*пакет безопасности*](../secgloss/s-gly.md) предоставляет службы безопасности для клиентского или серверного приложения, он загружается в клиентские и серверные процессы и считается в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="0e489-107">When a [*security package*](../secgloss/s-gly.md) provides security services to a client/server application, it is loaded into the client and server processes and is said to be in user mode.</span></span> <span data-ttu-id="0e489-108">Клиентские и серверные приложения обращаются к службам поддержки безопасности пакета безопасности с помощью [*интерфейса поставщика поддержки безопасности*](../secgloss/s-gly.md) (Майкрософт) (SSPI).</span><span class="sxs-lookup"><span data-stu-id="0e489-108">Client/server applications access the security package's security support services using Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI).</span></span>

<span data-ttu-id="0e489-109">Поддержка LSA для SSP/APs включает функции, которые могут использоваться экземплярами безопасности в режиме LSA и в режиме пользователя для взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="0e489-109">LSA support for SSP/APs includes functions that the LSA-mode and user-mode instances of a security package can use to communicate.</span></span> <span data-ttu-id="0e489-110">Кроме того, экземпляр пакета безопасности в пользовательском режиме может делегировать выбранные запросы информации в экземпляр пакета LSA-Mode.</span><span class="sxs-lookup"><span data-stu-id="0e489-110">Additionally, the user-mode instance of a security package can delegate selected requests for information to the LSA-mode instance of the package.</span></span>

<span data-ttu-id="0e489-111">Дополнительные сведения о инициализации пакетов безопасности для каждого режима см. в статье [инициализация в режиме LSA](lsa-mode-initialization.md) и [Инициализация пользовательского режима](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="0e489-111">For details about how security packages are initialized for each mode, see [LSA-mode Initialization](lsa-mode-initialization.md) and [User-mode Initialization](user-mode-initialization.md).</span></span>

 

 
