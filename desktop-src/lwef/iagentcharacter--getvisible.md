---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133719"
---
# <a name="iagentcharactergetvisible"></a><span data-ttu-id="4b88a-103">Иажентчарактер:: Visible</span><span class="sxs-lookup"><span data-stu-id="4b88a-103">IAgentCharacter::GetVisible</span></span>

<span data-ttu-id="4b88a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b88a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

<span data-ttu-id="4b88a-105">Определяет, видима ли в данный момент кадр анимации символа.</span><span class="sxs-lookup"><span data-stu-id="4b88a-105">Determines whether the character's animation frame is currently visible.</span></span>

-   <span data-ttu-id="4b88a-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4b88a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4b88a-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*</span><span class="sxs-lookup"><span data-stu-id="4b88a-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="4b88a-108">Адрес переменной, принимающей **значение true** , если фрейм символа является видимым, и **false** , если он скрыт.</span><span class="sxs-lookup"><span data-stu-id="4b88a-108">Address of a variable that receives **True** if the character's frame is visible and **False** if hidden.</span></span>

</dd> </dl>

<span data-ttu-id="4b88a-109">С помощью этого метода можно определить, видима ли в данный момент рамка символа.</span><span class="sxs-lookup"><span data-stu-id="4b88a-109">You can use this method to determine whether the character's frame is currently visible.</span></span> <span data-ttu-id="4b88a-110">Чтобы сделать символ видимым, используйте метод [**Показать**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="4b88a-110">To make a character visible, use the [**Show**](/windows/desktop/lwef/iagentcharacter--show) method.</span></span> <span data-ttu-id="4b88a-111">Чтобы скрыть символ, используйте метод [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .</span><span class="sxs-lookup"><span data-stu-id="4b88a-111">To hide a character, use the [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) method.</span></span>

 

 