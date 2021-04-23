---
description: Тип данных Language — это текстовая строка, содержащая один или несколько допустимых числовых идентификаторов языка. При наличии двух или более идентификаторов языков их необходимо разделять запятыми.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Язык
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263109"
---
# <a name="language"></a><span data-ttu-id="4e5a9-104">Язык</span><span class="sxs-lookup"><span data-stu-id="4e5a9-104">Language</span></span>

<span data-ttu-id="4e5a9-105">Тип данных Language — это текстовая строка, содержащая один или несколько допустимых числовых идентификаторов языка.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-105">The Language data type is a text string containing one or more valid numeric language IDs.</span></span> <span data-ttu-id="4e5a9-106">При наличии двух или более идентификаторов языков их необходимо разделять запятыми.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-106">If there are two or more language IDs, they must be separated by commas.</span></span>

<span data-ttu-id="4e5a9-107">Тип данных Language — это 16-разрядное значение, которое представляет собой сочетание числовых идентификаторов первичного и языкового языка.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-107">The Language data type is a 16-bit value that is the combination of a primary and sublanguage numeric IDs.</span></span> <span data-ttu-id="4e5a9-108">Первичный LANGID состоит из битов от 0 до 9, а идентификатор подязыка — от 10 до 15.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-108">The Primary LANGID comprises bits 0 through 9 while the subLanguage ID is bits 10 through 15.</span></span> <span data-ttu-id="4e5a9-109">Список числовых идентификаторов основного и вспомогательного языков см. в разделе [константы и строки идентификатора языка](../intl/language-identifier-constants-and-strings.md) .</span><span class="sxs-lookup"><span data-stu-id="4e5a9-109">For a list of primary and sub language numeric identifiers, see the [Language Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md) topic.</span></span>

<span data-ttu-id="4e5a9-110">Для основных идентификаторов языка значение Range 0x200 to 0x3ff определяется пользователем.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-110">For primary language IDs, the range 0x200 to 0x3ff is user definable.</span></span> <span data-ttu-id="4e5a9-111">Диапазон 0x000 to 0x1ff зарезервирован для использования системой.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-111">The range 0x000 to 0x1ff is reserved for system use.</span></span> <span data-ttu-id="4e5a9-112">Для идентификаторов языков, диапазон 0x20 — 0x3F, определяемый пользователем.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-112">For sublanguage IDs, the range 0x20 to 0x3f is user definable.</span></span> <span data-ttu-id="4e5a9-113">Диапазон 0x00 до 0x1F зарезервирован для использования системой.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-113">The range 0x00 to 0x1f is reserved for system use.</span></span>

 

 
