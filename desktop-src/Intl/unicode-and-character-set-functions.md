---
description: Для наборов символов используются следующие функции.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Функции Юникода и кодировка символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081331"
---
# <a name="unicode-and-character-set-functions"></a><span data-ttu-id="0dd30-103">Функции Юникода и кодировка символов</span><span class="sxs-lookup"><span data-stu-id="0dd30-103">Unicode and Character Set Functions</span></span>

<span data-ttu-id="0dd30-104">Для наборов символов используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="0dd30-104">The following functions are used with character sets.</span></span>



| <span data-ttu-id="0dd30-105">Функция</span><span class="sxs-lookup"><span data-stu-id="0dd30-105">Function</span></span>                                                       | <span data-ttu-id="0dd30-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0dd30-106">Description</span></span>                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dd30-107">**жеттекстчарсет**</span><span class="sxs-lookup"><span data-stu-id="0dd30-107">**GetTextCharset**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | <span data-ttu-id="0dd30-108">Извлекает идентификатор кодировки для шрифта, выбранного в данный момент в указанном контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="0dd30-108">Retrieves a character set identifier for the font that is currently selected into a specified device context.</span></span>         |
| [<span data-ttu-id="0dd30-109">**жеттекстчарсетинфо**</span><span class="sxs-lookup"><span data-stu-id="0dd30-109">**GetTextCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | <span data-ttu-id="0dd30-110">Извлекает сведения о кодировке шрифта, выбранного в данный момент в указанном контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="0dd30-110">Retrieves information about the character set of the font that is currently selected into a specified device context.</span></span> |
| [<span data-ttu-id="0dd30-111">**исдбкслеадбите**</span><span class="sxs-lookup"><span data-stu-id="0dd30-111">**IsDBCSLeadByte**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | <span data-ttu-id="0dd30-112">Определяет, является ли указанный символ старшим байтом для системной кодовой страницы Windows ANSI по умолчанию (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="0dd30-112">Determines if a specified character is a lead byte for the system default Windows ANSI code page (CP\_ACP).</span></span>           |
| [<span data-ttu-id="0dd30-113">**исдбкслеадбитикс**</span><span class="sxs-lookup"><span data-stu-id="0dd30-113">**IsDBCSLeadByteEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | <span data-ttu-id="0dd30-114">Определяет, является ли указанный символ потенциально старшим байтом.</span><span class="sxs-lookup"><span data-stu-id="0dd30-114">Determines if a specified character is potentially a lead byte.</span></span>                                                       |
| [<span data-ttu-id="0dd30-115">**истекстуникоде**</span><span class="sxs-lookup"><span data-stu-id="0dd30-115">**IsTextUnicode**</span></span>](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | <span data-ttu-id="0dd30-116">Определяет, может ли буфер содержать форму текста в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="0dd30-116">Determines if a buffer is likely to contain a form of Unicode text.</span></span>                                                   |
| [<span data-ttu-id="0dd30-117">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="0dd30-117">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | <span data-ttu-id="0dd30-118">Сопоставляет символьную строку со строкой UTF-16 (расширенная символьная).</span><span class="sxs-lookup"><span data-stu-id="0dd30-118">Maps a character string to a UTF-16 (wide character) string.</span></span>                                                          |
| [<span data-ttu-id="0dd30-119">**транслатечарсетинфо**</span><span class="sxs-lookup"><span data-stu-id="0dd30-119">**TranslateCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | <span data-ttu-id="0dd30-120">Преобразует сведения о кодировке и задает соответствующие значения для всех элементов целевой структуры.</span><span class="sxs-lookup"><span data-stu-id="0dd30-120">Translates character set information and sets all members of a destination structure to appropriate values.</span></span>           |
| [<span data-ttu-id="0dd30-121">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="0dd30-121">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | <span data-ttu-id="0dd30-122">Сопоставляет строку UTF-16 (расширенных символов) с новой символьной строкой.</span><span class="sxs-lookup"><span data-stu-id="0dd30-122">Maps a UTF-16 (wide character) string to a new character string.</span></span>                                                      |
| <span data-ttu-id="0dd30-123">[**битестауникоде**](/previous-versions/dd317724(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0dd30-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span></span>                       | <span data-ttu-id="0dd30-124">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="0dd30-124">Do not use.</span></span>                                                                                                           |
| [<span data-ttu-id="0dd30-125">**нлсдллкодепажетранслатион**</span><span class="sxs-lookup"><span data-stu-id="0dd30-125">**NlsDllCodePageTranslation**</span></span>](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | <span data-ttu-id="0dd30-126">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="0dd30-126">Do not use.</span></span>                                                                                                           |
| <span data-ttu-id="0dd30-127">[**уникодетобитес**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0dd30-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span></span>                       | <span data-ttu-id="0dd30-128">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0dd30-128">Do not use.</span></span>                                                                                                           |



 

 

 
