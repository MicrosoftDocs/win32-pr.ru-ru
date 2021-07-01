---
title: Иажентчарактер Жетмовекаусе
description: Иажентчарактер Жетмовекаусе
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119688"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="f90b6-103">Иажентчарактер:: Жетмовекаусе</span><span class="sxs-lookup"><span data-stu-id="f90b6-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="f90b6-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f90b6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="f90b6-105">Извлекает причину последнего перемещения символа.</span><span class="sxs-lookup"><span data-stu-id="f90b6-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="f90b6-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f90b6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f90b6-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*пдвкаусе*</span><span class="sxs-lookup"><span data-stu-id="f90b6-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="f90b6-108">Адрес переменной, которая получает причину последнего перемещения символа, и будет иметь одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="f90b6-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



| <span data-ttu-id="f90b6-109">Значение</span><span class="sxs-lookup"><span data-stu-id="f90b6-109">Value</span></span>                                                               | <span data-ttu-id="f90b6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f90b6-110">Description</span></span>                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f90b6-111">**const без знака Short** **невермовед = 0;**</span><span class="sxs-lookup"><span data-stu-id="f90b6-111">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="f90b6-112">Символ не был перемещен.</span><span class="sxs-lookup"><span data-stu-id="f90b6-112">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="f90b6-113">**const без знака Short** **усермовед = 1;**</span><span class="sxs-lookup"><span data-stu-id="f90b6-113">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="f90b6-114">Пользователь переместил символ.</span><span class="sxs-lookup"><span data-stu-id="f90b6-114">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="f90b6-115">**const без знака Short** **программовед = 2;**</span><span class="sxs-lookup"><span data-stu-id="f90b6-115">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="f90b6-116">Приложение переместило символ.</span><span class="sxs-lookup"><span data-stu-id="f90b6-116">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="f90b6-117">**const без знака Short** **осерпрограммовед = 3;**</span><span class="sxs-lookup"><span data-stu-id="f90b6-117">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="f90b6-118">Символ был перемещен другим приложением.</span><span class="sxs-lookup"><span data-stu-id="f90b6-118">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="f90b6-119">**const без знака Short** **системмовед = 4**</span><span class="sxs-lookup"><span data-stu-id="f90b6-119">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="f90b6-120">Сервер переместил символ, чтобы он оставался на экране после изменения разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="f90b6-120">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="f90b6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="f90b6-121">See Also</span></span>

[<span data-ttu-id="f90b6-122">**Иажентнотифисинк:: Move**</span><span class="sxs-lookup"><span data-stu-id="f90b6-122">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





