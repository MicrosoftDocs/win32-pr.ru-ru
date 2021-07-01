---
title: Иажентбаллун Жетфонтчарсет
description: Иажентбаллун Жетфонтчарсет
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120409"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="e256c-103">Иажентбаллун:: Жетфонтчарсет</span><span class="sxs-lookup"><span data-stu-id="e256c-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="e256c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e256c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="e256c-105">Указывает кодировку шрифта, отображаемого в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="e256c-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="e256c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e256c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e256c-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*псфонтчарсет*</span><span class="sxs-lookup"><span data-stu-id="e256c-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="e256c-108">Адрес значения, получающего набор символов шрифта.</span><span class="sxs-lookup"><span data-stu-id="e256c-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="e256c-109">Ниже приведены некоторые общие параметры для значения.</span><span class="sxs-lookup"><span data-stu-id="e256c-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="e256c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e256c-110">Value</span></span>    | <span data-ttu-id="e256c-111">Набор знаков</span><span class="sxs-lookup"><span data-stu-id="e256c-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e256c-112">0</span><span class="sxs-lookup"><span data-stu-id="e256c-112">0</span></span>   | <span data-ttu-id="e256c-113">Стандартные символы Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e256c-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="e256c-114">1</span><span class="sxs-lookup"><span data-stu-id="e256c-114">1</span></span>   | <span data-ttu-id="e256c-115">Набор символов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e256c-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="e256c-116">2</span><span class="sxs-lookup"><span data-stu-id="e256c-116">2</span></span>   | <span data-ttu-id="e256c-117">Кодировка символов.</span><span class="sxs-lookup"><span data-stu-id="e256c-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="e256c-118">128</span><span class="sxs-lookup"><span data-stu-id="e256c-118">128</span></span> | <span data-ttu-id="e256c-119">Двухбайтовая кодировка (DBCS), уникальная для японской версии Windows.</span><span class="sxs-lookup"><span data-stu-id="e256c-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="e256c-120">129</span><span class="sxs-lookup"><span data-stu-id="e256c-120">129</span></span> | <span data-ttu-id="e256c-121">Двухбайтовая кодировка (DBCS), уникальная для корейской версии Windows.</span><span class="sxs-lookup"><span data-stu-id="e256c-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="e256c-122">134</span><span class="sxs-lookup"><span data-stu-id="e256c-122">134</span></span> | <span data-ttu-id="e256c-123">Двухбайтовая кодировка (DBCS), уникальная для упрощенной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="e256c-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="e256c-124">136</span><span class="sxs-lookup"><span data-stu-id="e256c-124">136</span></span> | <span data-ttu-id="e256c-125">Двухбайтовая кодировка (DBCS), уникальная для версии Windows для китайского языка (традиционное письмо).</span><span class="sxs-lookup"><span data-stu-id="e256c-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="e256c-126">255</span><span class="sxs-lookup"><span data-stu-id="e256c-126">255</span></span> | <span data-ttu-id="e256c-127">Расширенные символы, обычно отображаемые приложениями MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="e256c-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="e256c-128">Дополнительные сведения о других значениях наборов символов см. в документации по пакету SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="e256c-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="e256c-129">Кодировка по умолчанию, используемая в текстовой подсказке для символа, определяется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e256c-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e256c-130">Его можно изменить с помощью [**иажентбаллун:: сетфонтчарсет**](iagentballoon--setfontcharset.md).</span><span class="sxs-lookup"><span data-stu-id="e256c-130">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="e256c-131">Однако пользователь может переопределить параметр кодировки для всех символов с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e256c-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="e256c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e256c-132">See Also</span></span>

[<span data-ttu-id="e256c-133">**Иажентбаллун:: Сетфонтчарсет**</span><span class="sxs-lookup"><span data-stu-id="e256c-133">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




