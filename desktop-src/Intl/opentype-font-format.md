---
description: Формат шрифта OpenType на основе Юникода расширяет формат файла шрифта TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Формат шрифта OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651178"
---
# <a name="opentype-font-format"></a><span data-ttu-id="2aca7-103">Формат шрифта OpenType</span><span class="sxs-lookup"><span data-stu-id="2aca7-103">OpenType Font Format</span></span>

<span data-ttu-id="2aca7-104">Формат шрифта OpenType на основе Юникода расширяет формат файла шрифта TrueType.</span><span class="sxs-lookup"><span data-stu-id="2aca7-104">The Unicode-based OpenType font format extends the TrueType font file format.</span></span> <span data-ttu-id="2aca7-105">Шрифты OpenType позволяют сопоставлять символы и [глифы](uniscribe-glossary.md), обеспечивая поддержку лигатур, позиционированных форм, альтернатив и других подстановок.</span><span class="sxs-lookup"><span data-stu-id="2aca7-105">OpenType fonts allow mapping between characters and [glyphs](uniscribe-glossary.md), enabling support for ligatures, positional forms, alternates, and other substitutions.</span></span> <span data-ttu-id="2aca7-106">Шрифты OpenType также могут содержать сведения, поддерживающие позиционирование двумерного глифа и вложение глифов, и могут состоять из шрифтов TrueType или PostScript.</span><span class="sxs-lookup"><span data-stu-id="2aca7-106">OpenType fonts can also include information that supports two-dimensional glyph positioning and glyph attachment, and can contain either TrueType or PostScript outlines.</span></span>

<span data-ttu-id="2aca7-107">Функции макета в шрифтах OpenType упорядочены по сценариям и языкам, что позволяет одному шрифту поддерживать несколько систем записи, даже в рамках одного сценария.</span><span class="sxs-lookup"><span data-stu-id="2aca7-107">Layout features within OpenType fonts are organized by scripts and languages, allowing a single font to support multiple writing systems, even within the same script.</span></span> <span data-ttu-id="2aca7-108">Чтобы обеспечить согласованность операций разметки текста и избежать ненужных затрат в файлах шрифтов или приложениях, многие из макетов текста и семантических алгоритмов языка включены в Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="2aca7-108">To ensure consistency in text layout operations and to avoid unnecessary overhead in font files or applications, many of the text layout and language semantic algorithms are included in Uniscribe.</span></span> <span data-ttu-id="2aca7-109">Это освобождает разработчика шрифта от необходимости определять обобщенные правила сценариев в шрифте.</span><span class="sxs-lookup"><span data-stu-id="2aca7-109">This relieves the font developer from having to define generalized script rules within a font.</span></span>

<span data-ttu-id="2aca7-110">Приложения могут добавлять определенные знания или предпочтения, касающиеся макета сценариев.</span><span class="sxs-lookup"><span data-stu-id="2aca7-110">Applications can introduce specific knowledge or preferences regarding script layout.</span></span> <span data-ttu-id="2aca7-111">Шрифты макета OpenType могут даже содержать правила макета, которые дублируют или заменяют значения, применяемые службами операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2aca7-111">OpenType layout fonts might even contain layout rules that duplicate or supersede those applied by operating system services.</span></span> <span data-ttu-id="2aca7-112">Многоуровневая структура служб операционной системы, поддерживающая макет текста, позволяет приложению выбрать сведения о макете для использования и выбрать способ применения.</span><span class="sxs-lookup"><span data-stu-id="2aca7-112">The layered structure of operating system services supporting text layout allows an application to choose the layout information to use, and select how to apply it.</span></span> <span data-ttu-id="2aca7-113">Дополнительные сведения см. в [обзоре типографских спецификаций Майкрософт](https://www.microsoft.com/typography/SpecificationsOverview.mspx) или [спецификации OpenType](https://www.microsoft.com/typography/otspec/).</span><span class="sxs-lookup"><span data-stu-id="2aca7-113">For additional information, see the [Microsoft Typography Specifications overview](https://www.microsoft.com/typography/SpecificationsOverview.mspx) or the [OpenType Specification](https://www.microsoft.com/typography/otspec/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2aca7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="2aca7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aca7-115">О Uniscribe</span><span class="sxs-lookup"><span data-stu-id="2aca7-115">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



