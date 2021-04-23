---
description: При запуске компьютера локальный центр безопасности (LSA) автоматически загружает все зарегистрированные библиотеки поддержки безопасности и пакеты проверки подлинности (SSP/AP) в пространство процесса. На следующих иллюстрациях показан процесс инициализации.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Инициализация режима LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546346"
---
# <a name="lsa-mode-initialization"></a><span data-ttu-id="72881-104">Инициализация режима LSA</span><span class="sxs-lookup"><span data-stu-id="72881-104">LSA Mode Initialization</span></span>

<span data-ttu-id="72881-105">При запуске компьютера [*локальный центр безопасности*](../secgloss/l-gly.md) (LSA) автоматически загружает [*все зарегистрированные*](../secgloss/s-gly.md) / DLL-библиотеки [*пакета проверки подлинности*](../secgloss/a-gly.md) (SSP/AP) в пространство процесса.</span><span class="sxs-lookup"><span data-stu-id="72881-105">When the computer system is started, the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) automatically loads all registered [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) DLLs into its process space.</span></span> <span data-ttu-id="72881-106">На следующих иллюстрациях показан процесс инициализации.</span><span class="sxs-lookup"><span data-stu-id="72881-106">The following illustrations show the initialization process.</span></span>

> [!Note]  
> <span data-ttu-id="72881-107">"Kerberos" представляет собой Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP, а "мой SSP/AP" представляет пользовательский поставщик общих служб (SSP), который содержит два пользовательских пакета безопасности.</span><span class="sxs-lookup"><span data-stu-id="72881-107">"Kerberos" represents the Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP, and "My SSP/AP" represents a custom SSP/AP that contains two custom security packages.</span></span>

 

![Инициализация режима LSA](images/lsamode1.png)

<span data-ttu-id="72881-109">При запуске LSA вызывает функцию [**сплсамодеинитиализе**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) в каждом SSP или ТД для получения указателей на функции, реализуемые каждым [*пакетом безопасности*](../secgloss/s-gly.md) в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="72881-109">At startup, the LSA calls the [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) function in each SSP/AP to obtain pointers to the functions implemented by each [*security package*](../secgloss/s-gly.md) in the DLL.</span></span> <span data-ttu-id="72881-110">Указатели функций передаются в LSA в массиве структур [**\_ \_ таблиц функций SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) .</span><span class="sxs-lookup"><span data-stu-id="72881-110">The function pointers are passed to the LSA in an array of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures.</span></span>

![LSA вызывает сплсамодеинитиализе для получения указателей на функцию](images/lsamode2.png)

<span data-ttu-id="72881-112">После получения набора структур [**\_ \_ ТАБЛИЦ функций SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) LSA вызывает функцию метода [**Initialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) для каждого пакета безопасности.</span><span class="sxs-lookup"><span data-stu-id="72881-112">After receiving the set of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures, the LSA calls each security package's [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) function.</span></span> <span data-ttu-id="72881-113">LSA использует этот вызов функции для передачи каждого пакета безопасности в структуру [**\_ \_ \_ таблицы функций LSA SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) , которая содержит указатели на функции поддержки LSA, доступные для пакетов безопасности.</span><span class="sxs-lookup"><span data-stu-id="72881-113">The LSA uses this function call to pass each security package an [**LSA\_SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) structure, which contains pointers to the LSA support functions available to security packages.</span></span> <span data-ttu-id="72881-114">Помимо сохранения указателей на функции поддержки LSA, пользовательские пакеты безопасности должны использовать свою реализацию функции " **инициализировать** " для выполнения любой обработки, связанной с инициализацией.</span><span class="sxs-lookup"><span data-stu-id="72881-114">In addition to storing the pointers to the LSA support functions, custom security packages should use their implementation of the **SpInitialize** function to perform any initialization-related processing.</span></span>

<span data-ttu-id="72881-115">Список функций поддержки LSA, доступных для пакетов безопасности в режиме LSA, см. в разделе [функции LSA, вызываемые SSP или ТД](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="72881-115">For a list of the LSA support functions available to LSA-mode security packages, see [LSA Functions Called by SSP/APs](authentication-functions.md).</span></span>

<span data-ttu-id="72881-116">Сведения о регистрации библиотеки DLL поставщика общих служб и AP см. в разделе [Регистрация DLL-библиотек SSP и AP](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="72881-116">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

 

 
