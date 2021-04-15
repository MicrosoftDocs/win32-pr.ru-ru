---
description: Расширенное редактирование 3,0 поддерживает редактор IME для Хекстауникоде, позволяющий пользователю выполнять преобразование между шестнадцатеричными и символами Юникода с помощью горячих клавиш одним из двух способов.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: Хекстауникоде IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547111"
---
# <a name="hextounicode-ime"></a><span data-ttu-id="b9ebf-103">Хекстауникоде IME</span><span class="sxs-lookup"><span data-stu-id="b9ebf-103">HexToUnicode IME</span></span>

<span data-ttu-id="b9ebf-104">Расширенное редактирование 3,0 поддерживает редактор IME для Хекстауникоде, позволяющий пользователю выполнять преобразование между шестнадцатеричными и символами Юникода с помощью горячих клавиш одним из двух способов.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-104">Rich Edit 3.0 supports the HexToUnicode IME, which allows a user to convert between hexadecimal and Unicode characters by using hot keys in one of two ways.</span></span>

<span data-ttu-id="b9ebf-105">При использовании первого метода преобразования пользователь вводит код символа в шестнадцатеричном виде, а затем вводит ALT + X.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-105">Using the first conversion method, the user types the character code in hexadecimal and then enters ALT+X.</span></span> <span data-ttu-id="b9ebf-106">Редактор IME заменяет шестнадцатеричные цифры перед точкой вставки символом Юникода.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-106">The IME replaces the hexadecimal digits preceding the insertion point with the Unicode character.</span></span> <span data-ttu-id="b9ebf-107">Если текущий шрифт не поддерживает код символа, выбирается подходящий шрифт, который поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-107">If the current font does not support the character code, an appropriate font is chosen that does support it.</span></span> <span data-ttu-id="b9ebf-108">Для преобразования из Юникода в шестнадцатеричный формат пользователь вводит SHIFT + ALT + X.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-108">To convert from Unicode to hexadecimal, the user enters SHIFT+ALT+X.</span></span> <span data-ttu-id="b9ebf-109">Эта запись заменяет символ Юникода, предшествующий точке вставки, шестнадцатеричными цифрами.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-109">This entry replaces the Unicode character that precedes the insertion point with the hexadecimal digits.</span></span> <span data-ttu-id="b9ebf-110">В частности, этот метод позволяет пользователю определить символ, обозначенный индикатором "отсутствующий глиф".</span><span class="sxs-lookup"><span data-stu-id="b9ebf-110">In particular, this method allows the user to determine the character that is indicated by a "missing glyph" indicator.</span></span> <span data-ttu-id="b9ebf-111">Если шестнадцатеричный код символа следует сразу за определенными шестнадцатеричными символами (несимвольными), пользователь выбирает конкретные цифры для преобразования перед вводом ALT + X.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-111">If the hexadecimal character code immediately follows some legitimate (noncharacter) hexadecimal characters, the user selects the specific digits to convert before typing ALT+X.</span></span> <span data-ttu-id="b9ebf-112">Проблема с этим первым методом заключается в том, что ALT + X иногда используется как сочетание клавиш для команды Exit (то есть выход).</span><span class="sxs-lookup"><span data-stu-id="b9ebf-112">A problem with this first method is that ALT+X is sometimes used as a key combination for the exit command (that is, eXit).</span></span> <span data-ttu-id="b9ebf-113">Например, в Microsoft Office эта команда отображается в меню " **файл** " только как вариант.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-113">For example, in Microsoft Office, this command only appears as an option of the **File** menu.</span></span>

<span data-ttu-id="b9ebf-114">Второй способ преобразования между шестнадцатеричными и символами Юникода включает цифровую панель.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-114">The second method of converting between hexadecimal and Unicode characters involves the number pad.</span></span> <span data-ttu-id="b9ebf-115">С помощью этого метода пользователь вводит ALT + Нумпад Numbers (со значениями больше 255), чтобы вводить символы Юникода с помощью десятичных значений.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-115">Using this method, the user types ALT+NumPad numbers (with values greater than 255) to enter Unicode characters using decimal values.</span></span> <span data-ttu-id="b9ebf-116">Этот метод не так удобен, как первый, поскольку пользователь не может видеть введенные шестнадцатеричные цифры.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-116">This method is not as useful as the first because the user cannot see what hexadecimal digits have been typed.</span></span> <span data-ttu-id="b9ebf-117">Кроме того, пользователь не может исправить шестнадцатеричные цифры, за исключением повторного ввода всех цифр.</span><span class="sxs-lookup"><span data-stu-id="b9ebf-117">Also, the user cannot correct the hexadecimal digits except by re-entering all the digits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9ebf-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b9ebf-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9ebf-119">О диспетчере методов ввода</span><span class="sxs-lookup"><span data-stu-id="b9ebf-119">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 



