---
title: Иажентбаллун Сетфонтчарсет
description: Иажентбаллун Сетфонтчарсет
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cc462895ff9f19f7e722660608a268af13446f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120209"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="12930-103">Иажентбаллун:: Сетфонтчарсет</span><span class="sxs-lookup"><span data-stu-id="12930-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="12930-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12930-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="12930-105">Задает кодировку шрифта, отображаемого в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="12930-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="12930-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="12930-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="12930-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*сфонтчарсет*</span><span class="sxs-lookup"><span data-stu-id="12930-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="12930-108">Кодировка шрифта.</span><span class="sxs-lookup"><span data-stu-id="12930-108">The character set of the font.</span></span> <span data-ttu-id="12930-109">Ниже приведены некоторые общие параметры для значения.</span><span class="sxs-lookup"><span data-stu-id="12930-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="12930-110">Значение</span><span class="sxs-lookup"><span data-stu-id="12930-110">Value</span></span>    | <span data-ttu-id="12930-111">Набор знаков</span><span class="sxs-lookup"><span data-stu-id="12930-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12930-112">0</span><span class="sxs-lookup"><span data-stu-id="12930-112">0</span></span>   | <span data-ttu-id="12930-113">Стандартные символы Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="12930-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="12930-114">1</span><span class="sxs-lookup"><span data-stu-id="12930-114">1</span></span>   | <span data-ttu-id="12930-115">Набор символов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="12930-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="12930-116">2</span><span class="sxs-lookup"><span data-stu-id="12930-116">2</span></span>   | <span data-ttu-id="12930-117">Кодировка символов.</span><span class="sxs-lookup"><span data-stu-id="12930-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="12930-118">128</span><span class="sxs-lookup"><span data-stu-id="12930-118">128</span></span> | <span data-ttu-id="12930-119">Двухбайтовая кодировка (DBCS), уникальная для японской версии Windows.</span><span class="sxs-lookup"><span data-stu-id="12930-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="12930-120">129</span><span class="sxs-lookup"><span data-stu-id="12930-120">129</span></span> | <span data-ttu-id="12930-121">Двухбайтовая кодировка (DBCS), уникальная для корейской версии Windows.</span><span class="sxs-lookup"><span data-stu-id="12930-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="12930-122">134</span><span class="sxs-lookup"><span data-stu-id="12930-122">134</span></span> | <span data-ttu-id="12930-123">Двухбайтовая кодировка (DBCS), уникальная для упрощенной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="12930-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="12930-124">136</span><span class="sxs-lookup"><span data-stu-id="12930-124">136</span></span> | <span data-ttu-id="12930-125">Двухбайтовая кодировка (DBCS), уникальная для версии Windows для китайского языка (традиционное письмо).</span><span class="sxs-lookup"><span data-stu-id="12930-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="12930-126">255</span><span class="sxs-lookup"><span data-stu-id="12930-126">255</span></span> | <span data-ttu-id="12930-127">Расширенные символы, обычно отображаемые приложениями MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="12930-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="12930-128">Дополнительные сведения о других значениях наборов символов см. в документации по пакету SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="12930-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="12930-129">Кодировка по умолчанию, используемая в текстовой подсказке для символа, определяется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="12930-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="12930-130">Его можно изменить с помощью [**иажентбаллун:: сетфонтчарсет**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span><span class="sxs-lookup"><span data-stu-id="12930-130">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="12930-131">Однако пользователь может переопределить параметр кодировки для всех символов с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="12930-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="12930-132">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="12930-132">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="12930-133">См. также</span><span class="sxs-lookup"><span data-stu-id="12930-133">See Also</span></span>

[<span data-ttu-id="12930-134">**Иажентбаллун:: Жетфонтчарсет**</span><span class="sxs-lookup"><span data-stu-id="12930-134">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




