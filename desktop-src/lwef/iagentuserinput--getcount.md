---
title: Иажентусеринпут вычислить
description: Иажентусеринпут вычислить
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252700"
---
# <a name="iagentuserinputgetcount"></a><span data-ttu-id="15163-103">Иажентусеринпут:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="15163-103">IAgentUserInput::GetCount</span></span>

<span data-ttu-id="15163-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15163-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="15163-105">Возвращает число вариантов [**команд**](command-event.md) , передаваемых обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="15163-105">Retrieves the number of [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="15163-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="15163-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="15163-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*пдвкаунт*</span><span class="sxs-lookup"><span data-stu-id="15163-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span></span>
</dt> <dd>

<span data-ttu-id="15163-108">Адрес переменной, которая получает количество вариантов [**команд**](command-event.md) , идентифицируемых сервером.</span><span class="sxs-lookup"><span data-stu-id="15163-108">Address of a variable that receives the count of [**Commands**](command-event.md) alternatives identified by the server.</span></span>

</dd> </dl>

<span data-ttu-id="15163-109">Если речевой ввод не является источником команды, например, если пользователь выбрал команду во всплывающем меню символа, функция **NOCOUNT** возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="15163-109">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, **GetCount** returns 1.</span></span> <span data-ttu-id="15163-110">Если функция **NOCOUNT** возвращает ноль (0), подсистема распознавания речи обнаружила речевой ввод, но определила, что соответствующей команды не было.</span><span class="sxs-lookup"><span data-stu-id="15163-110">If **GetCount** returns zero (0), the speech recognition engine detected spoken input but determined that there was no matching command.</span></span>

 

 




