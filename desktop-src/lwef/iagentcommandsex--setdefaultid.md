---
title: Иаженткоммандсекс Сетдефаултид
description: Иаженткоммандсекс Сетдефаултид
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412864"
---
# <a name="iagentcommandsexsetdefaultid"></a><span data-ttu-id="04309-103">Иаженткоммандсекс:: Сетдефаултид</span><span class="sxs-lookup"><span data-stu-id="04309-103">IAgentCommandsEx::SetDefaultID</span></span>

<span data-ttu-id="04309-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04309-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

<span data-ttu-id="04309-105">Задает идентификатор команды по умолчанию в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="04309-105">Sets the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="04309-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="04309-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="04309-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*двид*</span><span class="sxs-lookup"><span data-stu-id="04309-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="04309-108">Идентификатор для [**команды**](/windows/desktop/lwef/the-command-object) , которая должна быть задана в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04309-108">The ID for the [**Command**](/windows/desktop/lwef/the-command-object) to be set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="04309-109">Это свойство задает объект [**команды**](/windows/desktop/lwef/the-command-object) по умолчанию, заданный в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="04309-109">This property sets the default [**Command**](/windows/desktop/lwef/the-command-object) object set in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="04309-110">Команда по умолчанию выделяется полужирным шрифтом во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="04309-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="04309-111">Однако установка команды по умолчанию не изменяет обработку команд или события двойного щелчка.</span><span class="sxs-lookup"><span data-stu-id="04309-111">However, setting the default command does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="04309-112">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="04309-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="04309-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="04309-113">See Also</span></span>

[<span data-ttu-id="04309-114">**Иаженткоммандсекс:: Жетдефаултид**</span><span class="sxs-lookup"><span data-stu-id="04309-114">**IAgentCommandsEx::GetDefaultID**</span></span>](iagentcommandsex--getdefaultid.md)


 

 