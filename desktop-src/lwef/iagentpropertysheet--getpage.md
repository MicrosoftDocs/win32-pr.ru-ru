---
title: Иажентпропертишитная страница
description: Иажентпропертишитная страница
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119869"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="5667a-103">Иажентпропертишит:: @ Page</span><span class="sxs-lookup"><span data-stu-id="5667a-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="5667a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5667a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="5667a-105">Извлекает текущую страницу страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5667a-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="5667a-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5667a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5667a-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*пбсзпаже*</span><span class="sxs-lookup"><span data-stu-id="5667a-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="5667a-108">Адрес переменной, которая получает текущую страницу страницы свойств (последняя просмотренная страница, если окно не открыто).</span><span class="sxs-lookup"><span data-stu-id="5667a-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="5667a-109">Параметр может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="5667a-109">The parameter can be one of the following:</span></span>



|                 | <span data-ttu-id="5667a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5667a-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="5667a-111">**Речи**</span><span class="sxs-lookup"><span data-stu-id="5667a-111">**"Speech"**</span></span>    | <span data-ttu-id="5667a-112">Страница речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="5667a-112">The Speech Input page.</span></span> |
| <span data-ttu-id="5667a-113">**Проверки**</span><span class="sxs-lookup"><span data-stu-id="5667a-113">**"Output"**</span></span>    | <span data-ttu-id="5667a-114">Страница выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5667a-114">The Output page.</span></span>       |
| <span data-ttu-id="5667a-115">**Информация**</span><span class="sxs-lookup"><span data-stu-id="5667a-115">**"Copyright"**</span></span> | <span data-ttu-id="5667a-116">Страница авторских прав.</span><span class="sxs-lookup"><span data-stu-id="5667a-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="5667a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="5667a-117">See Also</span></span>

[<span data-ttu-id="5667a-118">**Иажентпропертишит:: Сетпаже**</span><span class="sxs-lookup"><span data-stu-id="5667a-118">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




