---
description: Когда приложение преобразует строки из ASCII или кодовой страницы Windows (ANSI) в Юникод, оно должно преобразовывать escape-последовательности, посимвольно в Юникод.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Использование escape-последовательностей и управляющих символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684607"
---
# <a name="using-escape-sequences-and-control-characters"></a><span data-ttu-id="dc425-103">Использование escape-последовательностей и управляющих символов</span><span class="sxs-lookup"><span data-stu-id="dc425-103">Using Escape Sequences and Control Characters</span></span>

<span data-ttu-id="dc425-104">Когда приложение преобразует строки из ASCII или [кодовой страницы Windows (ANSI)](code-pages.md) в Юникод, оно должно преобразовывать escape-последовательности, посимвольно в Юникод.</span><span class="sxs-lookup"><span data-stu-id="dc425-104">When an application converts strings from ASCII or from a [Windows (ANSI) code page](code-pages.md) to Unicode, it should translate escape sequences character-by-character into Unicode.</span></span> <span data-ttu-id="dc425-105">При преобразовании ASCII или другого 8-разрядного текстового файла в Юникод существует вероятность, что впоследствии он будет преобразован обратно.</span><span class="sxs-lookup"><span data-stu-id="dc425-105">When an ASCII or other 8-bit text file is converted to Unicode, there is a chance that it will subsequently be converted back.</span></span> <span data-ttu-id="dc425-106">Преобразование escape-последовательностей в Юникод на основе символьных символов вместо объединения их как одного символа Юникода позволяет выполнить обратный пересчет без необходимости распознать и проанализировать escape-последовательности.</span><span class="sxs-lookup"><span data-stu-id="dc425-106">Converting escape sequences into Unicode on a character-by-character basis, instead of combining them as a single Unicode character, makes it possible to perform the reverse conversion without needing to recognize and parse the escape sequences as such.</span></span> <span data-ttu-id="dc425-107">Например, ESC + A должно стать 0x001B (ESC), 0x0041 (A), а не 0x411B.</span><span class="sxs-lookup"><span data-stu-id="dc425-107">For example, ESC+A should become 0x001B (ESC), 0x0041 (A), instead of 0x411B.</span></span>

<span data-ttu-id="dc425-108">Первые 32 16-битные значения кода в Юникоде предназначены для управляющих символов 32.</span><span class="sxs-lookup"><span data-stu-id="dc425-108">The first 32 16-bit code values in Unicode are intended for the 32 control characters.</span></span> <span data-ttu-id="dc425-109">Эта спецификация поддерживает существующее использование управляющих символов в целях форматирования.</span><span class="sxs-lookup"><span data-stu-id="dc425-109">This specification supports the existing use of control characters for formatting purposes.</span></span> <span data-ttu-id="dc425-110">Приложения Юникода могут обрабатывать эти управляющие символы точно так же, как они обрабатывают их эквиваленты в кодировке ASCII.</span><span class="sxs-lookup"><span data-stu-id="dc425-110">Unicode applications can treat these control characters in exactly the same way as they treat their ASCII equivalents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc425-111">См. также</span><span class="sxs-lookup"><span data-stu-id="dc425-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc425-112">Использование специальных символов в Юникоде</span><span class="sxs-lookup"><span data-stu-id="dc425-112">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



