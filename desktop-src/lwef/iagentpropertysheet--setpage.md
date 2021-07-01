---
title: Иажентпропертишит Сетпаже
description: Иажентпропертишит Сетпаже
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120749"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="cffc1-103">Иажентпропертишит:: Сетпаже</span><span class="sxs-lookup"><span data-stu-id="cffc1-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="cffc1-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cffc1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="cffc1-105">Задает текущую страницу страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="cffc1-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="cffc1-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cffc1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cffc1-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*бсзпаже*</span><span class="sxs-lookup"><span data-stu-id="cffc1-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="cffc1-108">Объект BSTR, задающий текущую страницу Свойства.</span><span class="sxs-lookup"><span data-stu-id="cffc1-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="cffc1-109">Параметр может принимать одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="cffc1-109">The parameter can be one of the following.</span></span>



|                 | <span data-ttu-id="cffc1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cffc1-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="cffc1-111">**Речи**</span><span class="sxs-lookup"><span data-stu-id="cffc1-111">**"Speech"**</span></span>    | <span data-ttu-id="cffc1-112">Страница речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="cffc1-112">The Speech Input page.</span></span> |
| <span data-ttu-id="cffc1-113">**Проверки**</span><span class="sxs-lookup"><span data-stu-id="cffc1-113">**"Output"**</span></span>    | <span data-ttu-id="cffc1-114">Страница выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cffc1-114">The Output page.</span></span>       |
| <span data-ttu-id="cffc1-115">**Информация**</span><span class="sxs-lookup"><span data-stu-id="cffc1-115">**"Copyright"**</span></span> | <span data-ttu-id="cffc1-116">Страница авторских прав.</span><span class="sxs-lookup"><span data-stu-id="cffc1-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="cffc1-117">См. также</span><span class="sxs-lookup"><span data-stu-id="cffc1-117">See Also</span></span>

[<span data-ttu-id="cffc1-118">**Иажентпропертишит:: @ Page**</span><span class="sxs-lookup"><span data-stu-id="cffc1-118">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




