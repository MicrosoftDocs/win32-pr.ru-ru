---
description: Узнайте о установщик Windows концепциях, начинающихся с буквы R, например с помощью сокращенного пользовательского интерфейса и устойчивости.
ms.assetid: 868cb5b7-d5ab-41c7-a6d4-d7964a8ff6de
title: R (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2622ddd13bcd0c6ed7969e88eb27d41e281bf2f4
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011277"
---
# <a name="r-windows-installer"></a><span data-ttu-id="f286d-103">R (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="f286d-103">R (Windows Installer)</span></span>

<span data-ttu-id="f286d-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р [. J K](i-gly.md) L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="f286d-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f286d-105"><span id="_msi_reduced_ui_gly"></span><span id="_MSI_REDUCED_UI_GLY"></span>**сокращенный пользовательский интерфейс**</span><span class="sxs-lookup"><span data-stu-id="f286d-105"><span id="_msi_reduced_ui_gly"></span><span id="_MSI_REDUCED_UI_GLY"></span>**reduced UI**</span></span>
</dt> <dd>

<span data-ttu-id="f286d-106">Уровень [*внутренних возможностей пользовательского интерфейса*](i-gly.md) установщика.</span><span class="sxs-lookup"><span data-stu-id="f286d-106">Level of the installer's [*internal user interface*](i-gly.md) capabilities.</span></span> <span data-ttu-id="f286d-107">Отображает только созданные немодальные диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="f286d-107">Displays only authored modeless dialog boxes.</span></span> <span data-ttu-id="f286d-108">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f286d-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

</dd> <dt>

<span data-ttu-id="f286d-109"><span id="_msi_reinstall_gly"></span><span id="_MSI_REINSTALL_GLY"></span>**какому**</span><span class="sxs-lookup"><span data-stu-id="f286d-109"><span id="_msi_reinstall_gly"></span><span id="_MSI_REINSTALL_GLY"></span>**reinstall**</span></span>
</dt> <dd>

<span data-ttu-id="f286d-110">Частичная или полная переустановка установленного приложения.</span><span class="sxs-lookup"><span data-stu-id="f286d-110">Partial or complete reinstallation of an installed application.</span></span> <span data-ttu-id="f286d-111">Обычно это делается для восстановления приложения, если какие либо файлы, либо записи реестра были повреждены или отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="f286d-111">Commonly done to repair an application if any files or registry entries have become corrupted or are missing.</span></span> <span data-ttu-id="f286d-112">Дополнительные сведения см. в разделе [Переустановка компонента или приложения](reinstalling-a-feature-or-application.md).</span><span class="sxs-lookup"><span data-stu-id="f286d-112">For more information, see [Reinstalling a Feature or Application](reinstalling-a-feature-or-application.md).</span></span>

</dd> <dt>

<span data-ttu-id="f286d-113"><span id="_msi_resiliency_gly"></span><span id="_MSI_RESILIENCY_GLY"></span>**устойчивость**</span><span class="sxs-lookup"><span data-stu-id="f286d-113"><span id="_msi_resiliency_gly"></span><span id="_MSI_RESILIENCY_GLY"></span>**resiliency**</span></span>
</dt> <dd>

<span data-ttu-id="f286d-114">Возможность корректного восстановления после ошибки без создания сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f286d-114">Application capability of graceful recovery from error without generating error messages.</span></span> <span data-ttu-id="f286d-115">Дополнительные сведения см. в разделе [устойчивость](resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="f286d-115">For more information, see [Resiliency](resiliency.md).</span></span>

</dd> <dt>

<span data-ttu-id="f286d-116"><span id="_msi_rollback_gly"></span><span id="_MSI_ROLLBACK_GLY"></span>**отката**</span><span class="sxs-lookup"><span data-stu-id="f286d-116"><span id="_msi_rollback_gly"></span><span id="_MSI_ROLLBACK_GLY"></span>**rollback**</span></span>
</dt> <dd>

<span data-ttu-id="f286d-117">Автоматическое восстановление исходного состояния компьютера в случае сбоя установки.</span><span class="sxs-lookup"><span data-stu-id="f286d-117">Automatic restoration of the original state of the computer should the installation fail.</span></span> <span data-ttu-id="f286d-118">Дополнительные сведения см. в разделе [ROLLBACK Installation (установщик Windows)](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="f286d-118">For more information, see [Rollback Installation (Windows Installer)](rollback-installation.md).</span></span>

</dd> </dl>

 

 



