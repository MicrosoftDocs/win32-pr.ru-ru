---
title: Иаженткоммандсекс Жетдефаултид
description: Иаженткоммандсекс Жетдефаултид
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412961"
---
# <a name="iagentcommandsexgetdefaultid"></a><span data-ttu-id="7e350-103">Иаженткоммандсекс:: Жетдефаултид</span><span class="sxs-lookup"><span data-stu-id="7e350-103">IAgentCommandsEx::GetDefaultID</span></span>

<span data-ttu-id="7e350-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7e350-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

<span data-ttu-id="7e350-105">Возвращает идентификатор команды по умолчанию в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="7e350-105">Retrieves the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="7e350-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7e350-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7e350-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*пдвид*</span><span class="sxs-lookup"><span data-stu-id="7e350-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="7e350-108">Адрес переменной, которая получает идентификатор набора [**команд**](/windows/desktop/lwef/the-command-object) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e350-108">Address of a variable that receives the ID of the [**Command**](/windows/desktop/lwef/the-command-object) set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="7e350-109">Это свойство возвращает текущий объект [**команды**](/windows/desktop/lwef/the-command-object) по умолчанию в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="7e350-109">This property returns the current default [**Command**](/windows/desktop/lwef/the-command-object) object in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="7e350-110">Команда по умолчанию выделяется полужирным шрифтом во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="7e350-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="7e350-111">Однако при установке команды по умолчанию обработка команд или события двойного щелчка не меняются.</span><span class="sxs-lookup"><span data-stu-id="7e350-111">However, setting the default command does not change command handling or double-click events.</span></span>

<span data-ttu-id="7e350-112">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="7e350-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e350-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="7e350-113">See Also</span></span>

[<span data-ttu-id="7e350-114">**Иаженткоммандсекс:: Сетдефаултид**</span><span class="sxs-lookup"><span data-stu-id="7e350-114">**IAgentCommandsEx::SetDefaultID**</span></span>](iagentcommandsex--setdefaultid.md)


 

 