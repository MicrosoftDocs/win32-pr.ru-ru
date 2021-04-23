---
description: Интерфейс Ивсскомпонент позволяет средству записи точно настроить точное восстановление файлов на основе компонентов.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Настройка целевых объектов восстановления VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692874"
---
# <a name="setting-vss-restore-targets"></a><span data-ttu-id="12e9f-103">Настройка целевых объектов восстановления VSS</span><span class="sxs-lookup"><span data-stu-id="12e9f-103">Setting VSS Restore Targets</span></span>

<span data-ttu-id="12e9f-104">Интерфейс [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) позволяет средству записи точно настроить точное восстановление файлов на основе компонентов.</span><span class="sxs-lookup"><span data-stu-id="12e9f-104">The [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface enables a writer to fine-tune exactly how files are restored on a component-by-component basis.</span></span>

<span data-ttu-id="12e9f-105">Так как конфигурация системы во время восстановления возможна, что не ожидалось во время резервного копирования, предоставляется механизм восстановления цели.</span><span class="sxs-lookup"><span data-stu-id="12e9f-105">Because it is possible that the system configuration during restore is something other than that anticipated during backup, the restore target mechanism is provided.</span></span>

<span data-ttu-id="12e9f-106">Он позволяет модулям записи вызывать [**ивсскомпонент:: сетресторетаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) , чтобы изменить способ восстановления этих компонентов, [*явно включаемых*](vssgloss-e.md) в документ компонентов резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="12e9f-106">It allows writers to call [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) to change how those components that are [*explicitly included*](vssgloss-e.md) in the Backup Components Document are restored.</span></span> <span data-ttu-id="12e9f-107">Это также изменяет механизм восстановления, используемый для этих компонентов, которые [*неявно включены*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="12e9f-107">This also changes the restoration mechanism used on those components that are [*implicitly included*](vssgloss-i.md).</span></span>

<span data-ttu-id="12e9f-108">Восстановление файлов, выполняемое во время перезагрузки системы (в случае невозможности замены с помощью значений перечисления [**\_ ресторемесод \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) VSS \_ рме \_ RESTORE \_ при \_ перезагрузке и VSS \_ рме \_ RESTORE при \_ \_ перезагрузке \_ \_ \_ ), не может затронуть целевые объекты восстановления, так как службы VSS не будут копировать файлы в их окончательное расположение. </span><span class="sxs-lookup"><span data-stu-id="12e9f-108">File restoration that takes place during a system reboot (under the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration values VSS\_RME\_RESTORE\_AT\_REBOOT and VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE) cannot be affected by restore targets because there are no running VSS services when **MoveFileEx** copies files to their final location.</span></span>

<span data-ttu-id="12e9f-109">Аналогичным образом, служба VSS \_ рме \_ может не повлиять на пользовательские восстановления, поскольку каждое Пользовательское восстановление относится к конкретному модулю записи и может принимать или пропускать целевые объекты восстановления.</span><span class="sxs-lookup"><span data-stu-id="12e9f-109">Similarly, VSS\_RME\_CUSTOM restores may or may not be affected, because each custom restore is specific to a given writer and can choose to respect or ignore restore targets.</span></span>

<span data-ttu-id="12e9f-110">Инициаторы запроса и модули записи могут использовать [**ивсскомпонент:: жетресторетаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) для проверки целевого объекта восстановления набора компонентов.</span><span class="sxs-lookup"><span data-stu-id="12e9f-110">Requesters and writers can use [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) to check the restore target of a component set.</span></span>

<span data-ttu-id="12e9f-111">[**Ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) поддерживает следующие целевые объекты восстановления, которые могут быть установлены для набора компонентов по отдельности.</span><span class="sxs-lookup"><span data-stu-id="12e9f-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) supports the following restore targets, which can be set on a component set by component set basis:</span></span>

-   <span data-ttu-id="12e9f-112">исходный модуль VSS \_ RT \_ .</span><span class="sxs-lookup"><span data-stu-id="12e9f-112">VSS\_RT\_ORIGINAL.</span></span> <span data-ttu-id="12e9f-113">Метод Restore, указанный в перечислении перечисления [**\_ \_ ресторемесод для VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) , будет соблюдаться.</span><span class="sxs-lookup"><span data-stu-id="12e9f-113">The restore method specified by the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration will be respected.</span></span>
-   <span data-ttu-id="12e9f-114">\_ \_ альтернатива VSS RT.</span><span class="sxs-lookup"><span data-stu-id="12e9f-114">VSS\_RT\_ALTERNATE.</span></span> <span data-ttu-id="12e9f-115">Файлы восстанавливаются в расположение, определенное на основе существующего сопоставления альтернативного расположения.</span><span class="sxs-lookup"><span data-stu-id="12e9f-115">The files are restored to a location determined from an existing alternate location mapping.</span></span> <span data-ttu-id="12e9f-116">Если сопоставление с альтернативным расположением, соответствующее пути в подкомпоненте набора компонентов, существует, по возможности восстановите в альтернативное расположение. в противном случае возвратите ошибку.</span><span class="sxs-lookup"><span data-stu-id="12e9f-116">If an alternate location mapping matching a path in a component set subcomponent exists, restore to the alternate location if possible; otherwise, return an error.</span></span>

 

 



