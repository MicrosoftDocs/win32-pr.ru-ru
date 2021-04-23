---
title: Иажентпропертишитная страница
description: Иажентпропертишитная страница
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411021"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="e56fc-103">Иажентпропертишит:: @ Page</span><span class="sxs-lookup"><span data-stu-id="e56fc-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="e56fc-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e56fc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="e56fc-105">Извлекает текущую страницу страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e56fc-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="e56fc-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e56fc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e56fc-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*пбсзпаже*</span><span class="sxs-lookup"><span data-stu-id="e56fc-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="e56fc-108">Адрес переменной, которая получает текущую страницу страницы свойств (последняя просмотренная страница, если окно не открыто).</span><span class="sxs-lookup"><span data-stu-id="e56fc-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="e56fc-109">Параметр может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="e56fc-109">The parameter can be one of the following:</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="e56fc-110">**Речи**</span><span class="sxs-lookup"><span data-stu-id="e56fc-110">**"Speech"**</span></span>    | <span data-ttu-id="e56fc-111">Страница речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="e56fc-111">The Speech Input page.</span></span> |
| <span data-ttu-id="e56fc-112">**Проверки**</span><span class="sxs-lookup"><span data-stu-id="e56fc-112">**"Output"**</span></span>    | <span data-ttu-id="e56fc-113">Страница выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e56fc-113">The Output page.</span></span>       |
| <span data-ttu-id="e56fc-114">**Информация**</span><span class="sxs-lookup"><span data-stu-id="e56fc-114">**"Copyright"**</span></span> | <span data-ttu-id="e56fc-115">Страница авторских прав.</span><span class="sxs-lookup"><span data-stu-id="e56fc-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="e56fc-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="e56fc-116">See Also</span></span>

[<span data-ttu-id="e56fc-117">**Иажентпропертишит:: Сетпаже**</span><span class="sxs-lookup"><span data-stu-id="e56fc-117">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




