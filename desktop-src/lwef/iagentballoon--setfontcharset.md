---
title: Иажентбаллун Сетфонтчарсет
description: Иажентбаллун Сетфонтчарсет
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700691"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="9fc26-103">Иажентбаллун:: Сетфонтчарсет</span><span class="sxs-lookup"><span data-stu-id="9fc26-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="9fc26-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9fc26-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="9fc26-105">Задает кодировку шрифта, отображаемого в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="9fc26-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="9fc26-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9fc26-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9fc26-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*сфонтчарсет*</span><span class="sxs-lookup"><span data-stu-id="9fc26-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="9fc26-108">Кодировка шрифта.</span><span class="sxs-lookup"><span data-stu-id="9fc26-108">The character set of the font.</span></span> <span data-ttu-id="9fc26-109">Ниже приведены некоторые общие параметры для значения.</span><span class="sxs-lookup"><span data-stu-id="9fc26-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc26-110">0</span><span class="sxs-lookup"><span data-stu-id="9fc26-110">0</span></span>   | <span data-ttu-id="9fc26-111">Стандартные символы Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9fc26-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="9fc26-112">1</span><span class="sxs-lookup"><span data-stu-id="9fc26-112">1</span></span>   | <span data-ttu-id="9fc26-113">Набор символов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9fc26-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="9fc26-114">2</span><span class="sxs-lookup"><span data-stu-id="9fc26-114">2</span></span>   | <span data-ttu-id="9fc26-115">Кодировка символов.</span><span class="sxs-lookup"><span data-stu-id="9fc26-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="9fc26-116">128</span><span class="sxs-lookup"><span data-stu-id="9fc26-116">128</span></span> | <span data-ttu-id="9fc26-117">Двухбайтовая кодировка (DBCS), уникальная для японской версии Windows.</span><span class="sxs-lookup"><span data-stu-id="9fc26-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="9fc26-118">129</span><span class="sxs-lookup"><span data-stu-id="9fc26-118">129</span></span> | <span data-ttu-id="9fc26-119">Двухбайтовая кодировка (DBCS), уникальная для корейской версии Windows.</span><span class="sxs-lookup"><span data-stu-id="9fc26-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="9fc26-120">134</span><span class="sxs-lookup"><span data-stu-id="9fc26-120">134</span></span> | <span data-ttu-id="9fc26-121">Двухбайтовая кодировка (DBCS), уникальная для упрощенной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="9fc26-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="9fc26-122">136</span><span class="sxs-lookup"><span data-stu-id="9fc26-122">136</span></span> | <span data-ttu-id="9fc26-123">Двухбайтовая кодировка (DBCS), уникальная для версии Windows для китайского языка (традиционное письмо).</span><span class="sxs-lookup"><span data-stu-id="9fc26-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="9fc26-124">255</span><span class="sxs-lookup"><span data-stu-id="9fc26-124">255</span></span> | <span data-ttu-id="9fc26-125">Расширенные символы, обычно отображаемые приложениями MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="9fc26-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="9fc26-126">Дополнительные сведения о других значениях наборов символов см. в документации по пакету SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="9fc26-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="9fc26-127">Кодировка по умолчанию, используемая в текстовой подсказке для символа, определяется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9fc26-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="9fc26-128">Его можно изменить с помощью [**иажентбаллун:: сетфонтчарсет**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span><span class="sxs-lookup"><span data-stu-id="9fc26-128">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="9fc26-129">Однако пользователь может переопределить параметр кодировки для всех символов с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9fc26-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="9fc26-130">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="9fc26-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fc26-131">См. также:</span><span class="sxs-lookup"><span data-stu-id="9fc26-131">See Also</span></span>

[<span data-ttu-id="9fc26-132">**Иажентбаллун:: Жетфонтчарсет**</span><span class="sxs-lookup"><span data-stu-id="9fc26-132">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




