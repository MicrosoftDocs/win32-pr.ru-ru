---
title: Иажентчарактерекс
description: Иажентчарактерекс
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986679"
---
# <a name="iagentcharacterexgetguid"></a><span data-ttu-id="ec102-103">Иажентчарактерекс:: a GUID</span><span class="sxs-lookup"><span data-stu-id="ec102-103">IAgentCharacterEx::GetGUID</span></span>

<span data-ttu-id="ec102-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ec102-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

<span data-ttu-id="ec102-105">Возвращает уникальный идентификатор для символа.</span><span class="sxs-lookup"><span data-stu-id="ec102-105">Retrieves the unique ID for the character.</span></span>

-   <span data-ttu-id="ec102-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ec102-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ec102-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*пбсзгуид*</span><span class="sxs-lookup"><span data-stu-id="ec102-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="ec102-108">Адрес объекта BSTR, который получает идентификатор для символа.</span><span class="sxs-lookup"><span data-stu-id="ec102-108">Address of a BSTR that receives the ID for the character.</span></span>

</dd> </dl>

<span data-ttu-id="ec102-109">Свойство возвращает строковое представление GUID (в формате, заключенном в фигурные скобки и тире), которое используется сервером для уникальной идентификации символа.</span><span class="sxs-lookup"><span data-stu-id="ec102-109">The property returns a string representation of the GUID (formatted with braces and dashes) that the server uses to uniquely identify the character.</span></span> <span data-ttu-id="ec102-110">Идентификатор символа задается при компиляции с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ec102-110">A character identifier is set when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="ec102-111">свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ec102-111">The property is read-only.</span></span>

 

 




