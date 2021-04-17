---
description: В редакторе IME реализована функция, которая называется &\# 0034; повторное преобразование&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Использование повторного преобразования с IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673168"
---
# <a name="using-reconversion-with-an-ime"></a><span data-ttu-id="c7a73-103">Использование повторного преобразования с IME</span><span class="sxs-lookup"><span data-stu-id="c7a73-103">Using Reconversion with an IME</span></span>

<span data-ttu-id="c7a73-104">Редактор IME реализует функцию, которая называется повторное преобразование.</span><span class="sxs-lookup"><span data-stu-id="c7a73-104">An IME implements a feature called "reconversion".</span></span> <span data-ttu-id="c7a73-105">Обычно IMM определяет списки кандидатов на основе только тех записей, которые введены пользователем.</span><span class="sxs-lookup"><span data-stu-id="c7a73-105">Normally the IMM determines the lists of candidates based only on entries typed by the user.</span></span> <span data-ttu-id="c7a73-106">Повторное преобразование позволяет IMM определить один или несколько кандидатов на основе содержащего его предложения (контекст).</span><span class="sxs-lookup"><span data-stu-id="c7a73-106">Reconversion allows the IMM to determine one or more candidates based on the containing sentence (the context).</span></span> <span data-ttu-id="c7a73-107">Определенные типы перепреобразования являются простыми, нормальными и расширенными.</span><span class="sxs-lookup"><span data-stu-id="c7a73-107">The defined reconversion types are simple, normal, and enhanced.</span></span>

<span data-ttu-id="c7a73-108">Повторное преобразование полезно, когда пользователь замечает ошибку композиции в документе.</span><span class="sxs-lookup"><span data-stu-id="c7a73-108">Reconversion is useful when a user notices a composition error in a document.</span></span> <span data-ttu-id="c7a73-109">Пользователь может выбрать ошибку и выбрать команду Повторное преобразование из меню.</span><span class="sxs-lookup"><span data-stu-id="c7a73-109">The user can select the error and choose reconversion from a menu.</span></span> <span data-ttu-id="c7a73-110">Редактор IME использует контекст для определения наиболее подходящей замены.</span><span class="sxs-lookup"><span data-stu-id="c7a73-110">The IME uses the context to determine the best replacement.</span></span> <span data-ttu-id="c7a73-111">Приложение может использовать [**иммсеткомпоситионстринг**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) для поддержки повторного преобразования.</span><span class="sxs-lookup"><span data-stu-id="c7a73-111">The application can use [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) to support reconversion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7a73-112">См. также</span><span class="sxs-lookup"><span data-stu-id="c7a73-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7a73-113">Использование диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="c7a73-113">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 



