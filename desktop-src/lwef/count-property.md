---
title: Count, свойство
description: Count, свойство
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890517"
---
# <a name="count-property"></a><span data-ttu-id="f07d2-103">Count, свойство</span><span class="sxs-lookup"><span data-stu-id="f07d2-103">Count Property</span></span>

<span data-ttu-id="f07d2-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f07d2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f07d2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f07d2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f07d2-106">Возвращает длинное целое число (свойство только для чтения), которое указывает количество объектов [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f07d2-106">Returns a Long integer (read-only property) that specifies the count of [**Command**](/windows/desktop/lwef/the-command-object) objects in the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="f07d2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f07d2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f07d2-108">*Агент ***. Символы ("*** чарактерид \* \* *"). Команды. Count**</span><span class="sxs-lookup"><span data-stu-id="f07d2-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Count*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f07d2-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f07d2-109">Remarks</span></span>

<span data-ttu-id="f07d2-110">**Count** включает только число объектов [**Command**](/windows/desktop/lwef/the-command-object) , определенных в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f07d2-110">**Count** includes only the number of [**Command**](/windows/desktop/lwef/the-command-object) objects you define in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="f07d2-111">Сервер или другие записи клиента не включены.</span><span class="sxs-lookup"><span data-stu-id="f07d2-111">Server or other client entries are not included.</span></span>

 

 