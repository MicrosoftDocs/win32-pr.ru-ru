---
description: При использовании строк, заканчивающихся символом NULL, приложения Юникода всегда должны приводить к типу TCHAR ноль.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Использование строк, заканчивающихся символом NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272951"
---
# <a name="using-null-terminated-strings"></a><span data-ttu-id="b6883-103">Использование строк, заканчивающихся символом NULL</span><span class="sxs-lookup"><span data-stu-id="b6883-103">Using Null-terminated Strings</span></span>

<span data-ttu-id="b6883-104">При использовании строк, заканчивающихся символом NULL, приложения Юникода всегда должны приводить к типу TCHAR ноль.</span><span class="sxs-lookup"><span data-stu-id="b6883-104">Your Unicode applications should always cast zero to TCHAR when using null-terminated strings.</span></span> <span data-ttu-id="b6883-105">Код Символ 0x0000 — признак конца строки Юникода для строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="b6883-105">The code 0x0000 is the Unicode string terminator for a null-terminated string.</span></span> <span data-ttu-id="b6883-106">Для этого кода недостаточно одного байта, так как многие символы Юникода содержат нулевые байты как старший или младший байт.</span><span class="sxs-lookup"><span data-stu-id="b6883-106">A single null byte is not sufficient for this code, because many Unicode characters contain null bytes as either the high or the low byte.</span></span> <span data-ttu-id="b6883-107">Примером является буква A, для которой код символа — 0x0041.</span><span class="sxs-lookup"><span data-stu-id="b6883-107">An example is the letter A, for which the character code is 0x0041.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6883-108">См. также</span><span class="sxs-lookup"><span data-stu-id="b6883-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6883-109">Использование специальных символов в Юникоде</span><span class="sxs-lookup"><span data-stu-id="b6883-109">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



