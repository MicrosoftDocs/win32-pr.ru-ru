---
description: Узнайте о установщик Windows концепциях, начинающихся с буквы A, например на этапе специальных возможностей и приобретения.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011127"
---
# <a name="a-windows-installer"></a><span data-ttu-id="72a0c-103">A (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="72a0c-103">A (Windows Installer)</span></span>

<span data-ttu-id="72a0c-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р [. J K](i-gly.md) L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="72a0c-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="72a0c-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**режима**</span><span class="sxs-lookup"><span data-stu-id="72a0c-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibility**</span></span>
</dt> <dd>

<span data-ttu-id="72a0c-106">Реализация разработки для предоставления доступа к пользовательскому интерфейсу установщика для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="72a0c-106">Design implementation for making the installer's user interface accessible to all users.</span></span> <span data-ttu-id="72a0c-107">Дополнительные сведения о специальных возможностях см. в разделе Общие сведения: [Специальные возможности](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="72a0c-107">For more information about accessibility, see the overview topic: [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="72a0c-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**Фаза приобретения**</span><span class="sxs-lookup"><span data-stu-id="72a0c-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**acquisition phase**</span></span>
</dt> <dd>

<span data-ttu-id="72a0c-109">Этап установки, в течение которого установщик определяет процедуру.</span><span class="sxs-lookup"><span data-stu-id="72a0c-109">Phase of installation during which the installer determines procedure.</span></span> <span data-ttu-id="72a0c-110">Этап приобретения начинается, когда приложение или пользователь сообщает [*установщик Windows*](m-gly.md) установить приложение или компонент.</span><span class="sxs-lookup"><span data-stu-id="72a0c-110">Acquisition phase begins when an application or user instructs [*Windows Installer*](m-gly.md) to install an application or feature.</span></span> <span data-ttu-id="72a0c-111">Затем установщик запрашивает в [*базе данных*](i-gly.md) сведения о том, что он создает [*Скрипт выполнения*](e-gly.md) для установки.</span><span class="sxs-lookup"><span data-stu-id="72a0c-111">The installer then queries the [*database*](i-gly.md) for information as it generates the [*execution script*](e-gly.md) for the installation.</span></span> <span data-ttu-id="72a0c-112">Дополнительные сведения о стадиях установки см. в разделе [механизм установки](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="72a0c-112">For more information about the phases of an installation, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="72a0c-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**поддержки**</span><span class="sxs-lookup"><span data-stu-id="72a0c-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**action**</span></span>
</dt> <dd>

<span data-ttu-id="72a0c-114">Многие функции, выполняемые установщик Windows, инкапсулируются в действия.</span><span class="sxs-lookup"><span data-stu-id="72a0c-114">Many of the functions performed by Windows Installer are encapsulated into actions.</span></span> <span data-ttu-id="72a0c-115">Каждое действие задает выполнение определенной функции, а общая последовательность процедур установки определяется последовательностью действий в [*таблицах последовательности*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="72a0c-115">Each action specifies the execution of a particular function and the total procedural flow of the installation is prescribed by the sequence of actions in the [*Sequence tables*](s-gly.md).</span></span> <span data-ttu-id="72a0c-116">[*Стандартные действия*](s-gly.md) встроены в установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="72a0c-116">[*Standard actions*](s-gly.md) are built into Windows Installer.</span></span> <span data-ttu-id="72a0c-117">[*Пользовательские действия*](c-gly.md) записываются автором [*пакета*](p-gly.md)установки.</span><span class="sxs-lookup"><span data-stu-id="72a0c-117">[*Custom actions*](c-gly.md) are written by the author of the installation [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="72a0c-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Режим одобрения администратором**</span><span class="sxs-lookup"><span data-stu-id="72a0c-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Admin Approval Mode**</span></span>
</dt> <dd>

<span data-ttu-id="72a0c-119">Состояние утверждения, включенное функцией защиты учетных записей (UAC), которое запускает всех пользователей с минимальными правами, включая администраторов.</span><span class="sxs-lookup"><span data-stu-id="72a0c-119">The approval state enabled by User Account Protection (UAC) that runs all users with least privilege, including administrators.</span></span> <span data-ttu-id="72a0c-120">Пользователям необходимо предоставить согласие на повышение прав на установку, требующую прав администратора.</span><span class="sxs-lookup"><span data-stu-id="72a0c-120">Users are required to provide consent to elevate installations that require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="72a0c-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**размещения**</span><span class="sxs-lookup"><span data-stu-id="72a0c-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**advertising**</span></span>
</dt> <dd>

<span data-ttu-id="72a0c-122">Возможность сделать интерфейсы необходимыми для загрузки и сделать приложение доступным без установки приложения.</span><span class="sxs-lookup"><span data-stu-id="72a0c-122">Capability to make the interfaces required for loading and to make an application available without installing the application.</span></span> <span data-ttu-id="72a0c-123">Когда пользователь или приложение активирует объявленный интерфейс, установщик продолжает установку необходимых компонентов.</span><span class="sxs-lookup"><span data-stu-id="72a0c-123">When a user or application activates an advertised interface, the installer then proceeds to install the necessary components.</span></span> <span data-ttu-id="72a0c-124">Два типа рекламы — это [*назначение*](/windows) и [*Публикация*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="72a0c-124">The two types of advertising are [*assigning*](/windows) and [*publishing*](p-gly.md).</span></span> <span data-ttu-id="72a0c-125">Дополнительные сведения см. в разделе также [*Install-On-Demand*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="72a0c-125">For more information, see also [*install-on-demand*](i-gly.md).</span></span> <span data-ttu-id="72a0c-126">Дополнительные сведения о том, как установщик объявляет приложения, см. в статье [объявление](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="72a0c-126">For more information about how the installer advertises applications, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72a0c-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Служба сведений о приложениях (AIS)**</span><span class="sxs-lookup"><span data-stu-id="72a0c-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span></span>
</dt> <dd>

<span data-ttu-id="72a0c-128">Системная служба Windows Vista, которая упрощает запуск установок, требующих повышенных привилегий для запуска.</span><span class="sxs-lookup"><span data-stu-id="72a0c-128">A system service of Windows Vista that facilitates starting installations that require elevated privileges to run.</span></span> <span data-ttu-id="72a0c-129">Предоставляет пользовательский интерфейс согласия, используемый контролем учетных записей, для запроса пользователя на авторизацию администратора.</span><span class="sxs-lookup"><span data-stu-id="72a0c-129">Provides the Consent UI used by User Account Control to prompt a user for administrator authorization.</span></span>

</dd> <dt>

<span data-ttu-id="72a0c-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**предоставление**</span><span class="sxs-lookup"><span data-stu-id="72a0c-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assigning**</span></span>
</dt> <dd>

<span data-ttu-id="72a0c-131">Делает приложение доступным и делает его недоступным, как если бы оно было установлено для пользователя, без фактической установки.</span><span class="sxs-lookup"><span data-stu-id="72a0c-131">Makes an application available, and makes it appear as if it has been installed to a user, without actually installing it.</span></span> <span data-ttu-id="72a0c-132">Назначение добавляет ярлыки и значки в меню " **Пуск** ", связывает соответствующие файлы и записывает записи реестра для приложения.</span><span class="sxs-lookup"><span data-stu-id="72a0c-132">Assigning adds shortcuts and icons to the **Start** menu, associates appropriate files, and writes registry entries for the application.</span></span> <span data-ttu-id="72a0c-133">Когда пользователь пытается открыть назначенное приложение, установщик устанавливает приложение.</span><span class="sxs-lookup"><span data-stu-id="72a0c-133">When a user tries to open an assigned application, then the installer installs the application.</span></span> <span data-ttu-id="72a0c-134">Назначение и [*Публикация*](p-gly.md) — это два метода [*рекламы*](/windows).</span><span class="sxs-lookup"><span data-stu-id="72a0c-134">Assigning and [*publishing*](p-gly.md) are two methods of [*advertising*](/windows).</span></span> <span data-ttu-id="72a0c-135">Дополнительные сведения см. в статье [объявление](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="72a0c-135">For more information, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72a0c-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**асинхронное выполнение**</span><span class="sxs-lookup"><span data-stu-id="72a0c-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchronous execution**</span></span>
</dt> <dd>

<span data-ttu-id="72a0c-137">[*Настраиваемое действие*](c-gly.md) , в течение которого установщик запускает отдельные потоки настраиваемого действия и текущую установку одновременно.</span><span class="sxs-lookup"><span data-stu-id="72a0c-137">[*Custom action*](c-gly.md) during which the installer runs separate threads of the custom action and the current installation simultaneously.</span></span> <span data-ttu-id="72a0c-138">Дополнительные сведения см. в разделе [синхронные и асинхронные настраиваемые действия](synchronous-and-asynchronous-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="72a0c-138">For more information, see [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md).</span></span>

</dd> </dl>

 

 
