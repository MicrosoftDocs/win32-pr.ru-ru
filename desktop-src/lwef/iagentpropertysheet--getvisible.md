---
title: Иажентпропертишит
description: Иажентпропертишит
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330347"
---
# <a name="iagentpropertysheetgetvisible"></a><span data-ttu-id="cf178-103">Иажентпропертишит:: Visible</span><span class="sxs-lookup"><span data-stu-id="cf178-103">IAgentPropertySheet::GetVisible</span></span>

<span data-ttu-id="cf178-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cf178-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

<span data-ttu-id="cf178-105">Определяет, является ли страница свойств Microsoft Agent видимой или скрытой.</span><span class="sxs-lookup"><span data-stu-id="cf178-105">Determines whether the Microsoft Agent property sheet is visible or hidden.</span></span>

-   <span data-ttu-id="cf178-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cf178-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cf178-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*</span><span class="sxs-lookup"><span data-stu-id="cf178-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="cf178-108">Адрес переменной, которая получает **значение true** , если страница свойств является видимой, и **false** , если она скрыта.</span><span class="sxs-lookup"><span data-stu-id="cf178-108">Address of a variable that receives **True** if the property sheet is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="cf178-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="cf178-109">See Also</span></span>

[<span data-ttu-id="cf178-110">**Иажентпропертишит:: Сетвисибле**</span><span class="sxs-lookup"><span data-stu-id="cf178-110">**IAgentPropertySheet::SetVisible**</span></span>](iagentpropertysheet--setvisible.md)


 

 




