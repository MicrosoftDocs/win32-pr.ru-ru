---
title: Управление версиями и резервные стратегии
description: Когда приложение обнаруживает частичное обновление с помощью одного из описанных выше методов или считывает набор объектов, Дата вступления в силу которых еще не достигнута, приложение должно корректно работать с ситуацией.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- Управление версиями и резервные стратегии AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887615"
---
# <a name="versioning-and-fallback-strategies"></a><span data-ttu-id="2b5f5-104">Управление версиями и резервные стратегии</span><span class="sxs-lookup"><span data-stu-id="2b5f5-104">Versioning and Fallback Strategies</span></span>

<span data-ttu-id="2b5f5-105">Когда приложение обнаруживает частичное обновление с помощью одного из описанных выше методов или считывает набор объектов, Дата вступления в силу которых еще не достигнута, приложение должно корректно работать с ситуацией.</span><span class="sxs-lookup"><span data-stu-id="2b5f5-105">When an application detects a partial update using one of the preceding techniques or reads a set of objects whose effective date has not yet been reached, the application must deal with the situation gracefully.</span></span> <span data-ttu-id="2b5f5-106">Для некоторых приложений корректное реагирование заключается в том, чтобы вернуться к предыдущей версии рассматриваемых объектов.</span><span class="sxs-lookup"><span data-stu-id="2b5f5-106">For some applications, the graceful response is to "fall back" to a previous version of the objects in question.</span></span> <span data-ttu-id="2b5f5-107">Службы домен Active Directory не предоставляют средства управления версиями — приложения, которым необходима эта возможность, должны предоставлять ее самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="2b5f5-107">Active Directory Domain Services do not provide a versioning facility—applications that want this capability must provide it themselves.</span></span> <span data-ttu-id="2b5f5-108">Подходы к управлении версиями включают в себя сохранение "последних известных" значений в кэше локально и хранение нескольких наборов объектов в каталоге, например в "старых", "текущих" и "новых" контейнерах.</span><span class="sxs-lookup"><span data-stu-id="2b5f5-108">Approaches to versioning include keeping the "last known good" values cached locally and storing multiple sets of objects in the directory, for example, in "old," "current," and "new" containers.</span></span> <span data-ttu-id="2b5f5-109">Многие другие схемы возможны.</span><span class="sxs-lookup"><span data-stu-id="2b5f5-109">Many other schemes are possible.</span></span>

<span data-ttu-id="2b5f5-110">Реализации должны соблюдать осторожность, чтобы избежать непредвиденных последствий.</span><span class="sxs-lookup"><span data-stu-id="2b5f5-110">Implementations must take care to avoid unintended consequences.</span></span> <span data-ttu-id="2b5f5-111">Более ранняя версия объектов должна использоваться только при обнаружении частичного обновления или в случае, если новые объекты еще не являются эффективными.</span><span class="sxs-lookup"><span data-stu-id="2b5f5-111">An earlier version of objects should be used only when a partial update is detected or the new objects are not yet "effective."</span></span> <span data-ttu-id="2b5f5-112">Если что-то в приложении не работает, то это может обойти намерение администратора.</span><span class="sxs-lookup"><span data-stu-id="2b5f5-112">Falling back because something in the application "does not work" might circumvent an administrator's intent.</span></span> <span data-ttu-id="2b5f5-113">Например, на двух компьютерах, которые раньше могли обмениваться данными, могут возникнуть невозможность сделать это из-за изменения политики безопасности протокола IP (IPsec).</span><span class="sxs-lookup"><span data-stu-id="2b5f5-113">For example, two computers that formerly could communicate might find themselves unable to do so because of a change in Internet Protocol security (IPsec) policy.</span></span> <span data-ttu-id="2b5f5-114">Если это сделано намеренно от части администратора, то уязвимые системы не должны переключаться на политику, которая позволяла им взаимодействовать, так как это может привести к нарушению безопасности.</span><span class="sxs-lookup"><span data-stu-id="2b5f5-114">If this is intentional on the part of the administrator, the affected systems should not fall back to the policy that allowed them to communicate, as this would be a security breach.</span></span>

 

 




