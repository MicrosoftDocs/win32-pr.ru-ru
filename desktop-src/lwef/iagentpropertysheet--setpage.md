---
title: Иажентпропертишит Сетпаже
description: Иажентпропертишит Сетпаже
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776889"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="ba90c-103">Иажентпропертишит:: Сетпаже</span><span class="sxs-lookup"><span data-stu-id="ba90c-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="ba90c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ba90c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="ba90c-105">Задает текущую страницу страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ba90c-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="ba90c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ba90c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ba90c-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*бсзпаже*</span><span class="sxs-lookup"><span data-stu-id="ba90c-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="ba90c-108">Объект BSTR, задающий текущую страницу Свойства.</span><span class="sxs-lookup"><span data-stu-id="ba90c-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="ba90c-109">Параметр может принимать одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="ba90c-109">The parameter can be one of the following.</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="ba90c-110">**Речи**</span><span class="sxs-lookup"><span data-stu-id="ba90c-110">**"Speech"**</span></span>    | <span data-ttu-id="ba90c-111">Страница речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="ba90c-111">The Speech Input page.</span></span> |
| <span data-ttu-id="ba90c-112">**Проверки**</span><span class="sxs-lookup"><span data-stu-id="ba90c-112">**"Output"**</span></span>    | <span data-ttu-id="ba90c-113">Страница выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ba90c-113">The Output page.</span></span>       |
| <span data-ttu-id="ba90c-114">**Информация**</span><span class="sxs-lookup"><span data-stu-id="ba90c-114">**"Copyright"**</span></span> | <span data-ttu-id="ba90c-115">Страница авторских прав.</span><span class="sxs-lookup"><span data-stu-id="ba90c-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ba90c-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="ba90c-116">See Also</span></span>

[<span data-ttu-id="ba90c-117">**Иажентпропертишит:: @ Page**</span><span class="sxs-lookup"><span data-stu-id="ba90c-117">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




