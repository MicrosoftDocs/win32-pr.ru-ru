---
description: Если вы решили это сделать, приложение может предоставить собственные Распознаватели. В этом разделе описываются требования к созданию пользовательского распознавателя приложений для приложения, которое можно использовать с API платформы Tablet PC.
ms.assetid: 502ef3fb-ba45-4f8b-bbd5-19c24e313439
title: Создание распознавателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc71f56dc7095c6c72d18b36c3a12caa493ec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692045"
---
# <a name="creating-a-recognizer"></a><span data-ttu-id="8d287-104">Создание распознавателя</span><span class="sxs-lookup"><span data-stu-id="8d287-104">Creating a Recognizer</span></span>

<span data-ttu-id="8d287-105">Если вы решили это сделать, приложение может предоставить собственные Распознаватели.</span><span class="sxs-lookup"><span data-stu-id="8d287-105">If you choose to do so, your application can provide its own recognizer implementations.</span></span> <span data-ttu-id="8d287-106">В этом разделе описываются требования к созданию пользовательского распознавателя приложений для приложения, которое можно использовать с API платформы Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="8d287-106">This section describes the requirements for creating a custom application recognizer for your application that you can use with the Tablet PC Platform API.</span></span>

> [!Note]  
> <span data-ttu-id="8d287-107">Распознаватели пользовательских приложений не используются в панели ввода Tablet PC или журнале Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8d287-107">Custom application recognizers are not used by the Tablet PC Input Panel or Microsoft Windows Journal.</span></span> <span data-ttu-id="8d287-108">Эти аксессуары используют только распознаватели, с которыми они были протестированы.</span><span class="sxs-lookup"><span data-stu-id="8d287-108">These accessories use only recognizers with which they have been tested.</span></span>

 

<span data-ttu-id="8d287-109">В следующих разделах подробно описана реализация пользовательского распознавателя:</span><span class="sxs-lookup"><span data-stu-id="8d287-109">The following sections detail the implementation of a custom recognizer:</span></span>

-   [<span data-ttu-id="8d287-110">Архитектура API распознавания</span><span class="sxs-lookup"><span data-stu-id="8d287-110">Recognition API Architecture</span></span>](recognition-api-architecture.md)
-   <span data-ttu-id="8d287-111">[Необходимые API-интерфейсы для распознавания](/previous-versions//ms701664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d287-111">[Required Recognition APIs](/previous-versions//ms701664(v=vs.85))</span></span>
-   [<span data-ttu-id="8d287-112">ХРЕКОГНИЗЕР и ХРЕКОКОНТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="8d287-112">HRECOGNIZER and HRECOCONTEXT</span></span>](hrecognizer-and-hrecocontext.md)
-   [<span data-ttu-id="8d287-113">Структура Lattice распознавателя</span><span class="sxs-lookup"><span data-stu-id="8d287-113">Recognizer Lattice Structure</span></span>](recognizer-lattice-structure.md)
-   [<span data-ttu-id="8d287-114">Регистрация библиотеки DLL распознавателя</span><span class="sxs-lookup"><span data-stu-id="8d287-114">Registering Your Recognizer DLL</span></span>](registering-your-recognizer-dll.md)
-   [<span data-ttu-id="8d287-115">Рекомендации по потокам распознавателя</span><span class="sxs-lookup"><span data-stu-id="8d287-115">Recognizer Threading Considerations</span></span>](recognizer-threading-considerations.md)
-   [<span data-ttu-id="8d287-116">Типичная последовательность вызовов</span><span class="sxs-lookup"><span data-stu-id="8d287-116">Typical Calling Sequence</span></span>](typical-calling-sequence.md)
-   [<span data-ttu-id="8d287-117">Пример шаблона библиотеки DLL распознавателя</span><span class="sxs-lookup"><span data-stu-id="8d287-117">Recognizer DLL Sample Template</span></span>](recognizer-dll-sample-template.md)
-   [<span data-ttu-id="8d287-118">Значения диапазона Юникода для жестов</span><span class="sxs-lookup"><span data-stu-id="8d287-118">Unicode Range Values of Gestures</span></span>](unicode-range-values-of-gestures.md)
-   [<span data-ttu-id="8d287-119">API-интерфейсы распознавателя</span><span class="sxs-lookup"><span data-stu-id="8d287-119">Recognizer APIs</span></span>](recognizer-apis.md)

 

 
