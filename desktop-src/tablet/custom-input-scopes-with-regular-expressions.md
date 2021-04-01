---
description: Пользовательские области ввода можно определить с помощью языковых моделей, состоящих из регулярных выражений для рукописного ввода и присвоения их полям. Например, если вы создаете приложение базы данных для частей склада и хотите, чтобы пользователи могли вводить номера частей с помощью панели рукописного ввода планшетного ПК. Если синтаксис номера части состоит из трех букв, за которыми следуют четыре цифры, за которыми следует другая буква (например, ABC1234D), распознаватель рукописного ввода будет иметь трудное время распознавания таких входных данных, так как оно не определено в языковой модели. Нет предопределенных фактоид, соответствующих такому синтаксису, и не может включать в Майкрософт синтаксис для каждого возможного поля, которое может потребоваться приложению. Регулярные выражения для рукописного ввода предоставляют приложениям простой способ определения собственной языковой модели для конкретного поля специального использования. Примечание. при работе в приложении с поддержкой рукописного ввода, которое использует свойство фактоид объекта Рекогнизерконтекст, нельзя использовать фактоидс версии 1 в регулярном выражении.
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Пользовательские области ввода с регулярными выражениями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072554"
---
# <a name="custom-input-scopes-with-regular-expressions"></a><span data-ttu-id="1ddc6-106">Пользовательские области ввода с регулярными выражениями</span><span class="sxs-lookup"><span data-stu-id="1ddc6-106">Custom Input Scopes with Regular Expressions</span></span>

<span data-ttu-id="1ddc6-107">Пользовательские области ввода можно определить с помощью языковых моделей, состоящих из регулярных выражений для рукописного ввода и присвоения их полям.</span><span class="sxs-lookup"><span data-stu-id="1ddc6-107">You can define custom input scopes by using language models composed of regular expressions for handwriting and assigning them to fields.</span></span>

<span data-ttu-id="1ddc6-108">Например, если вы создаете приложение базы данных для частей склада и хотите, чтобы пользователи могли вводить номера частей с помощью панели рукописного ввода планшетного ПК.</span><span class="sxs-lookup"><span data-stu-id="1ddc6-108">For example, if you are creating a database application for warehouse parts and want users to be able to enter part numbers using the Tablet PC Input Panel's writing pad.</span></span> <span data-ttu-id="1ddc6-109">Если синтаксис номера части состоит из трех букв, за которыми следуют четыре цифры, за которыми следует другая буква (например, ABC1234D), распознаватель рукописного ввода будет иметь трудное время распознавания таких входных данных, так как оно не определено в языковой модели.</span><span class="sxs-lookup"><span data-stu-id="1ddc6-109">If the part number syntax consists of three letters followed by four numbers followed by another letter (for example, ABC1234D), the handwriting recognizer would have a difficult time recognizing such input because it is not defined in the language model.</span></span> <span data-ttu-id="1ddc6-110">Нет предопределенных фактоид, соответствующих такому синтаксису, и не может включать в Майкрософт синтаксис для каждого возможного поля, которое может потребоваться приложению.</span><span class="sxs-lookup"><span data-stu-id="1ddc6-110">There is no predefined factoid that corresponds to such syntax, nor can Microsoft include the syntax for every possible field an application might need.</span></span> <span data-ttu-id="1ddc6-111">Регулярные выражения для рукописного ввода предоставляют приложениям простой способ определения собственной языковой модели для конкретного поля специального использования.</span><span class="sxs-lookup"><span data-stu-id="1ddc6-111">Handwriting regular expressions provide an easy way for applications to define their own language model for a particular special-use field.</span></span>

> [!Note]  
> <span data-ttu-id="1ddc6-112">При работе в приложении с поддержкой рукописного ввода, которое использует свойство [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) , нельзя использовать фактоидс версии 1 в регулярном выражении.</span><span class="sxs-lookup"><span data-stu-id="1ddc6-112">When working in an ink-enabled application that uses the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object, you cannot use version 1 factoids in a regular expression.</span></span>

 

 

 



