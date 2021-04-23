---
description: Настраиваемые действия, предназначенные для изменения состояния системы, должны быть отложенными настраиваемыми действиями выполнения.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Изменение состояния системы с помощью настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662909"
---
# <a name="changing-the-system-state-using-a-custom-action"></a><span data-ttu-id="33b6c-103">Изменение состояния системы с помощью настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="33b6c-103">Changing the System State Using a Custom Action</span></span>

<span data-ttu-id="33b6c-104">Настраиваемые действия, предназначенные для изменения состояния системы, должны быть отложенными настраиваемыми действиями выполнения.</span><span class="sxs-lookup"><span data-stu-id="33b6c-104">Custom actions intended to change the system state must be deferred execution custom actions.</span></span> <span data-ttu-id="33b6c-105">Настраиваемые действия, которые задают свойства, состояния компонентов, состояния компонентов или целевые каталоги, или запланируют системные операции путем вставки строк в таблицы последовательности, могут безопасно использовать немедленное выполнение.</span><span class="sxs-lookup"><span data-stu-id="33b6c-105">Custom actions that set properties, feature states, component states, or target directories, or schedule system operations by inserting rows into sequence tables can use immediate execution safely.</span></span> <span data-ttu-id="33b6c-106">Однако пользовательские действия, которые изменяют систему напрямую или вызывают другую системную службу, должны быть отложены до момента выполнения сценария установки.</span><span class="sxs-lookup"><span data-stu-id="33b6c-106">However, custom actions that change the system directly or call another system service must be deferred to the time when the installation script is executed.</span></span> <span data-ttu-id="33b6c-107">Дополнительные сведения см. в разделе [Отложенное выполнение настраиваемых действий](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="33b6c-107">For more information, see [Deferred Execution Custom Actions](deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="33b6c-108">Не следует пытаться использовать немедленную настраиваемую операцию выполнения для изменения состояния системы, так как каждое настраиваемое действие, которое изменяет состояние, должно иметь соответствующее настраиваемое действие отката для отмены изменения состояния системы при откате установки.</span><span class="sxs-lookup"><span data-stu-id="33b6c-108">You should not attempt to use an immediate execution custom action to change the system state, because every custom action that changes the state needs to have a corresponding rollback custom action to undo the system state change on an installation rollback.</span></span> <span data-ttu-id="33b6c-109">Все настраиваемые действия отката также являются отложенными пользовательскими действиями и должны предшествовать их отмененному действию.</span><span class="sxs-lookup"><span data-stu-id="33b6c-109">All rollback custom actions are also deferred custom actions and must precede the action they undo.</span></span> <span data-ttu-id="33b6c-110">Дополнительные сведения см. в разделе [ROLLBACK Custom Actions](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="33b6c-110">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



