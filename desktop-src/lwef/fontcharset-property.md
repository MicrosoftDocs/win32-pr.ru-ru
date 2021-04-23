---
title: Фонтчарсет, свойство
description: Фонтчарсет, свойство
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331952"
---
# <a name="fontcharset-property"></a><span data-ttu-id="49e7b-103">Фонтчарсет, свойство</span><span class="sxs-lookup"><span data-stu-id="49e7b-103">FontCharSet Property</span></span>

<span data-ttu-id="49e7b-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49e7b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="49e7b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="49e7b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="49e7b-106">Возвращает или задает кодировку для шрифта, отображаемого в тексте всплывающего окна указанного символа.</span><span class="sxs-lookup"><span data-stu-id="49e7b-106">Returns or sets the character set for the font displayed in the specified character's word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="49e7b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="49e7b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="49e7b-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Значение всплывающего окна. фонтчарсет* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="49e7b-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontCharSet*\* \[ = *value*\]</span></span>



| <span data-ttu-id="49e7b-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="49e7b-109">Part</span></span>    | <span data-ttu-id="49e7b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="49e7b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e7b-111">*value*</span><span class="sxs-lookup"><span data-stu-id="49e7b-111">*value*</span></span> | <span data-ttu-id="49e7b-112">Целочисленное значение, указывающее кодировку, используемую шрифтом.</span><span class="sxs-lookup"><span data-stu-id="49e7b-112">An integer value that specifies the character set used by the font.</span></span> <span data-ttu-id="49e7b-113">Ниже приведены некоторые общие параметры для значения: 0 стандартных символов Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="49e7b-113">The following are some common settings for value: 0 Standard Windows characters (ANSI).</span></span><br/> <span data-ttu-id="49e7b-114">1 набор символов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49e7b-114">1 Default character set.</span></span><br/> <span data-ttu-id="49e7b-115">2. кодировка символов.</span><span class="sxs-lookup"><span data-stu-id="49e7b-115">2 The symbol character set.</span></span><br/> <span data-ttu-id="49e7b-116">128. двухбайтовая кодировка (DBCS), уникальная для японской версии Windows.</span><span class="sxs-lookup"><span data-stu-id="49e7b-116">128 Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span><br/> <span data-ttu-id="49e7b-117">129. двухбайтовая кодировка (DBCS), уникальная для корейской версии Windows.</span><span class="sxs-lookup"><span data-stu-id="49e7b-117">129 Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span><br/> <span data-ttu-id="49e7b-118">134. двухбайтовая кодировка (DBCS), уникальная для китайского языка Windows (упрощенная версия).</span><span class="sxs-lookup"><span data-stu-id="49e7b-118">134 Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span><br/> <span data-ttu-id="49e7b-119">136. двухбайтовая кодировка (DBCS), уникальная для версии Windows для китайского языка (традиционное письмо).</span><span class="sxs-lookup"><span data-stu-id="49e7b-119">136 Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span><br/> <span data-ttu-id="49e7b-120">255. Расширенные символы обычно отображаются приложениями Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="49e7b-120">255 Extended characters normally displayed by Microsoft MS-DOS applications.</span></span><br/> <span data-ttu-id="49e7b-121">Дополнительные сведения о других значениях наборов символов см. в документации по пакету SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="49e7b-121">For other character set values, consult the Platform SDK documentation.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49e7b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49e7b-122">Remarks</span></span>

<span data-ttu-id="49e7b-123">Значение по умолчанию для набора символов всплывающего слова символа задается в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="49e7b-123">The default value for the character set of a character's word balloon is set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="49e7b-124">Кроме того, пользователь может переопределить параметры набора символов для всех символов на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="49e7b-124">In addition, the user can override the character-set settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="49e7b-125">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="49e7b-125">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="49e7b-126">Если вы используете некомпилированный символ, проверьте свойства [**FontName**](fontname-property.md) и **фонтчарсет** для символа, чтобы определить, подходит ли он для вашего языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="49e7b-126">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and **FontCharSet** properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="49e7b-127">Возможно, потребуется задать эти значения перед использованием метода [**говорите**](speak-method.md) , чтобы обеспечить отображение текста в выноске слова.</span><span class="sxs-lookup"><span data-stu-id="49e7b-127">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="49e7b-128">См. также:</span><span class="sxs-lookup"><span data-stu-id="49e7b-128">See Also</span></span>

[<span data-ttu-id="49e7b-129">**FontName, свойство**</span><span class="sxs-lookup"><span data-stu-id="49e7b-129">**FontName property**</span></span>](fontname-property.md)


 

 





