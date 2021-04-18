---
description: илангуаже ЛОКАЛи \_
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682400"
---
# <a name="locale_ilanguage"></a><span data-ttu-id="9fb40-103">илангуаже ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="9fb40-103">LOCALE\_ILANGUAGE</span></span>

<span data-ttu-id="9fb40-104">[Идентификатор языка](language-identifiers.md) с шестнадцатеричным значением.</span><span class="sxs-lookup"><span data-stu-id="9fb40-104">[Language identifier](language-identifiers.md) with a hexadecimal value.</span></span> <span data-ttu-id="9fb40-105">Например, Английский (США) имеет значение 0409, которое указывает на шестнадцатеричное число и эквивалентно 1033 десятичному.</span><span class="sxs-lookup"><span data-stu-id="9fb40-105">For example, English (United States) has the value 0409, which indicates 0x0409 hexadecimal, and is equivalent to 1033 decimal.</span></span> <span data-ttu-id="9fb40-106">Максимально допустимое число символов для этой строки равно пяти, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="9fb40-106">The maximum number of characters allowed for this string is five, including a terminating null character.</span></span>

<span data-ttu-id="9fb40-107">**Windows Vista и более поздние версии:** Использование этой константы может привести к тому, что [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) возвратит недопустимый идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="9fb40-107">**Windows Vista and later:** Use of this constant can cause [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) to return an invalid locale identifier.</span></span> <span data-ttu-id="9fb40-108">При вызове этой функции приложение должно использовать константу [ \_ SNAME локали](locale-sname.md) .</span><span class="sxs-lookup"><span data-stu-id="9fb40-108">Your application should use the [LOCALE\_SNAME](locale-sname.md) constant when calling this function.</span></span>

 

 



