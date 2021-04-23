---
title: Иажентчарактер Жетмовекаусе
description: Иажентчарактер Жетмовекаусе
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411454"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="8166e-103">Иажентчарактер:: Жетмовекаусе</span><span class="sxs-lookup"><span data-stu-id="8166e-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="8166e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8166e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="8166e-105">Извлекает причину последнего перемещения символа.</span><span class="sxs-lookup"><span data-stu-id="8166e-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="8166e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8166e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8166e-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*пдвкаусе*</span><span class="sxs-lookup"><span data-stu-id="8166e-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="8166e-108">Адрес переменной, которая получает причину последнего перемещения символа, и будет иметь одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="8166e-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8166e-109">**const без знака Short** **невермовед = 0;**</span><span class="sxs-lookup"><span data-stu-id="8166e-109">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="8166e-110">Символ не был перемещен.</span><span class="sxs-lookup"><span data-stu-id="8166e-110">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="8166e-111">**const без знака Short** **усермовед = 1;**</span><span class="sxs-lookup"><span data-stu-id="8166e-111">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="8166e-112">Пользователь переместил символ.</span><span class="sxs-lookup"><span data-stu-id="8166e-112">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="8166e-113">**const без знака Short** **программовед = 2;**</span><span class="sxs-lookup"><span data-stu-id="8166e-113">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="8166e-114">Приложение переместило символ.</span><span class="sxs-lookup"><span data-stu-id="8166e-114">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="8166e-115">**const без знака Short** **осерпрограммовед = 3;**</span><span class="sxs-lookup"><span data-stu-id="8166e-115">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="8166e-116">Символ был перемещен другим приложением.</span><span class="sxs-lookup"><span data-stu-id="8166e-116">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="8166e-117">**const без знака Short** **системмовед = 4**</span><span class="sxs-lookup"><span data-stu-id="8166e-117">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="8166e-118">Сервер переместил символ, чтобы он оставался на экране после изменения разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="8166e-118">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="8166e-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="8166e-119">See Also</span></span>

[<span data-ttu-id="8166e-120">**Иажентнотифисинк:: Move**</span><span class="sxs-lookup"><span data-stu-id="8166e-120">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





