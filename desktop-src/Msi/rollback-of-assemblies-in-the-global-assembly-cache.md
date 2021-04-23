---
description: Двухэтапный процесс расширяет модель транзакций установщик Windows на продукты, содержащие сборки среды CLR. Это позволяет установщику откатить неудачные установки и удаления сборок.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Откат сборок в глобальном кэше сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809490"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a><span data-ttu-id="ecd11-104">Откат сборок в глобальном кэше сборок</span><span class="sxs-lookup"><span data-stu-id="ecd11-104">Rollback of Assemblies in the Global Assembly Cache</span></span>

<span data-ttu-id="ecd11-105">Двухэтапный процесс расширяет модель транзакций установщик Windows на продукты, содержащие сборки среды CLR.</span><span class="sxs-lookup"><span data-stu-id="ecd11-105">A two-step process extends the Windows Installer's transaction model to products containing common language runtime assemblies.</span></span> <span data-ttu-id="ecd11-106">Это позволяет установщику откатить неудачные установки и удаления сборок.</span><span class="sxs-lookup"><span data-stu-id="ecd11-106">This enables the installer to rollback unsuccessful installations and removals of assemblies.</span></span>

<span data-ttu-id="ecd11-107">На первом шаге установщик Windows использует платформу Microsoft .NET для создания одного интерфейса для каждой сборки.</span><span class="sxs-lookup"><span data-stu-id="ecd11-107">During the first step, the Windows Installer uses the Microsoft .NET Framework to create one interface for each assembly.</span></span> <span data-ttu-id="ecd11-108">Установщик Windows использует столько интерфейсов, сколько устанавливаются сборки.</span><span class="sxs-lookup"><span data-stu-id="ecd11-108">The Windows Installer uses as many interfaces as there are assemblies being installed.</span></span> <span data-ttu-id="ecd11-109">Фиксация сборки с помощью одного из этих интерфейсов означает, что сборка готова заменить любую существующую сборку с тем же именем, она еще не заменит ее.</span><span class="sxs-lookup"><span data-stu-id="ecd11-109">Committing an assembly using one of these interfaces only means that the assembly is ready to replace any existing assembly with the same name, it does not yet replace it.</span></span> <span data-ttu-id="ecd11-110">Если пользователь отменяет установку или возникает неустранимая ошибка установки, установщик Windows может по-прежнему выполнять откат сборки до предыдущего состояния, освобождая эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ecd11-110">If the user cancels the installation, or if there is a fatal installation error, the Windows Installer can still rollback the assembly to its previous state by releasing these interfaces.</span></span>

<span data-ttu-id="ecd11-111">После того как установщик Windows завершит установку всех сборок и установщик Windows компонентов, установщик может запустить второй шаг установки.</span><span class="sxs-lookup"><span data-stu-id="ecd11-111">After the Windows Installer completes installing all assemblies and Windows Installer components, the installer may initiate the second step of the installation.</span></span> <span data-ttu-id="ecd11-112">На втором шаге используется отдельная функция для выполнения окончательной фиксации всех новых сборок среды CLR.</span><span class="sxs-lookup"><span data-stu-id="ecd11-112">The second step uses a separate function to do the final commit of all the new common language runtime assemblies.</span></span> <span data-ttu-id="ecd11-113">Все существующие сборки с тем же именем заменяются.</span><span class="sxs-lookup"><span data-stu-id="ecd11-113">This replaces any existing assemblies with the same name.</span></span>

 

 



