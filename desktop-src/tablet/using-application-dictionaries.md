---
description: По умолчанию распознаватель использует системный словарь, содержащий все часто написанные слова на языке.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Использование словарей приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497343"
---
# <a name="using-application-dictionaries"></a><span data-ttu-id="1ce79-103">Использование словарей приложений</span><span class="sxs-lookup"><span data-stu-id="1ce79-103">Using Application Dictionaries</span></span>

<span data-ttu-id="1ce79-104">По умолчанию распознаватель использует системный словарь, содержащий все часто написанные слова на языке.</span><span class="sxs-lookup"><span data-stu-id="1ce79-104">By default, the recognizer uses a system dictionary that contains all of the commonly written words in a language.</span></span> <span data-ttu-id="1ce79-105">Кроме того, распознаватель имеет пользовательский словарь, содержащий слова, добавленные пользователем в словарь.</span><span class="sxs-lookup"><span data-stu-id="1ce79-105">In addition, the recognizer has a user dictionary that contains words that the user has added to the dictionary.</span></span> <span data-ttu-id="1ce79-106">Пользователи добавляют слово в пользовательский словарь с помощью панели ввода Tablet PC с помощью элементов выбора в:</span><span class="sxs-lookup"><span data-stu-id="1ce79-106">Users add a word to the user dictionary through Tablet PC Input Panel through selections in:</span></span>

-   <span data-ttu-id="1ce79-107">Список альтернатив (при записи).</span><span class="sxs-lookup"><span data-stu-id="1ce79-107">The alternate list (when writing).</span></span>
-   <span data-ttu-id="1ce79-108">Меню «средства речи» (при разговоре).</span><span class="sxs-lookup"><span data-stu-id="1ce79-108">The Speech Tools menu (when speaking).</span></span>

<span data-ttu-id="1ce79-109">При разработке приложения, в котором предполагается, что пользователь будет писать слова, отсутствующие в системном словаре или пользовательском словаре, создайте словарь приложений.</span><span class="sxs-lookup"><span data-stu-id="1ce79-109">If you are designing an application into which you anticipate the user will write words that are not found in either the system dictionary or the user dictionary, create an application dictionary.</span></span> <span data-ttu-id="1ce79-110">Словарь приложений улучшает точность распознавания, предоставляя распознавателю дополнительный настраиваемый список слов, которые, скорее всего, будут вводиться в приложение в качестве рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="1ce79-110">An application dictionary further improves recognition accuracy by providing the recognizer with an additional customized list of words likely to be entered as handwriting into an application.</span></span>

<span data-ttu-id="1ce79-111">Словарь приложений создается с помощью объекта [**список слов**](inkwordlist-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1ce79-111">You create an application dictionary by using the [**WordList**](inkwordlist-class.md) object.</span></span> <span data-ttu-id="1ce79-112">Словарь пошагового приложения увеличивает точность распознавания, предоставляя распознавателю список ожидаемых слов.</span><span class="sxs-lookup"><span data-stu-id="1ce79-112">The ensuing application dictionary increases recognition accuracy by providing the recognizer with a list of expected words.</span></span> <span data-ttu-id="1ce79-113">Например, словарь приложений, содержащий медицинскую терминологию, повышает точность распознавания в рамках приложения, разработанного для медицинской отраслей, в которой эти термины, скорее всего, будут написаны.</span><span class="sxs-lookup"><span data-stu-id="1ce79-113">For example, an application dictionary that contains medical terminology increases recognition accuracy within an application developed for the medical industry into which the terms are likely to be written.</span></span>

<span data-ttu-id="1ce79-114">Другой пример: при проектировании формы для того, чтобы заказать музыкальные инструменты, создайте объект [**список слов**](inkwordlist-class.md) , содержащий имена наиболее распространенных производителей инструментов.</span><span class="sxs-lookup"><span data-stu-id="1ce79-114">As another example, when designing a form for someone to order musical instruments, create a [**WordList**](inkwordlist-class.md) object that contains the names of the most common instrument manufacturers.</span></span> <span data-ttu-id="1ce79-115">Задайте для свойства список [**слов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) объекта [**Рекогнизерконтекст**](inkrecognizercontext-class.md) созданный объект **список слов** .</span><span class="sxs-lookup"><span data-stu-id="1ce79-115">Set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object to the **WordList** object you created.</span></span> <span data-ttu-id="1ce79-116">Этот список слов затем передается распознавателю объекту **рекогнизерконтекст** .</span><span class="sxs-lookup"><span data-stu-id="1ce79-116">This list of words is then passed to the recognizer by the **RecognizerContext** object.</span></span> <span data-ttu-id="1ce79-117">Словарь приложений увеличивает точность распознавания, когда эти имена записываются в поле приложения.</span><span class="sxs-lookup"><span data-stu-id="1ce79-117">The application dictionary increases recognition accuracy when those names are written in a field in the application.</span></span>

<span data-ttu-id="1ce79-118">В следующих разделах описывается использование словарей приложений.</span><span class="sxs-lookup"><span data-stu-id="1ce79-118">The following topics describe how to use application dictionaries.</span></span>

-   [<span data-ttu-id="1ce79-119">Общие сведения о списках слов, контексте распознавателя и Фактоидс</span><span class="sxs-lookup"><span data-stu-id="1ce79-119">Understanding Word Lists, Recognizer Context, and Factoids</span></span>](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [<span data-ttu-id="1ce79-120">Использование словарей приложений с интерфейсами API платформы Tablet PC</span><span class="sxs-lookup"><span data-stu-id="1ce79-120">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [<span data-ttu-id="1ce79-121">Создание пользовательских словарей для распознавания рукописного текста</span><span class="sxs-lookup"><span data-stu-id="1ce79-121">Creating Custom Dictionaries for Handwriting Recognition</span></span>](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



