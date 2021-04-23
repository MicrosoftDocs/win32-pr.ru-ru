---
title: Дефаулткомманд, свойство
description: Дефаулткомманд, свойство
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069929"
---
# <a name="defaultcommand-property"></a><span data-ttu-id="e9f44-103">Дефаулткомманд, свойство</span><span class="sxs-lookup"><span data-stu-id="e9f44-103">DefaultCommand Property</span></span>

<span data-ttu-id="e9f44-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9f44-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e9f44-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="e9f44-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e9f44-106">Возвращает или задает команду по умолчанию для объекта [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e9f44-106">Returns or sets the default command of the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span>

</dd> <dt>

<span data-ttu-id="e9f44-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e9f44-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e9f44-108">Символы агента. \*\* \* \*\* \*  **("***Чарактерид***"). Строка Commands. дефаулткомманд** \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="e9f44-108">*agent.\*\*\*Characters*\* **("***CharacterID***").Commands.DefaultCommand** \[ = *string*\]</span></span>



| <span data-ttu-id="e9f44-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="e9f44-109">Part</span></span>     | <span data-ttu-id="e9f44-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e9f44-110">Description</span></span>                                                                         |
|----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f44-111">*string*</span><span class="sxs-lookup"><span data-stu-id="e9f44-111">*string*</span></span> | <span data-ttu-id="e9f44-112">Строковое значение, определяющее имя (идентификатор) [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="e9f44-112">A string value identifying the name (ID) of the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9f44-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9f44-113">Remarks</span></span>

<span data-ttu-id="e9f44-114">Это свойство позволяет задать [**команду**](/windows/desktop/lwef/the-command-object) в коллекции Commands в [**качестве команды по**](/windows/desktop/lwef/the-commands-collection-object) умолчанию, выводит полужирный шрифт.</span><span class="sxs-lookup"><span data-stu-id="e9f44-114">This property enables you to set a [**Command**](/windows/desktop/lwef/the-command-object) in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection as the default command, rendering it bold.</span></span> <span data-ttu-id="e9f44-115">Это не приводит к изменению обработки команд или двойного щелчка.</span><span class="sxs-lookup"><span data-stu-id="e9f44-115">This does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="e9f44-116">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e9f44-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 