---
title: Преобразование в JScript из JavaScript
description: Преобразование в JScript из JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104533026"
---
# <a name="translating-to-jscript-from-javascript"></a><span data-ttu-id="9e788-103">Преобразование в JScript из JavaScript</span><span class="sxs-lookup"><span data-stu-id="9e788-103">Translating to JScript from JavaScript</span></span>

<span data-ttu-id="9e788-104">JScript в значительной степени совместим с JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e788-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="9e788-105">Однако в JScript версии 5,0 есть некоторые объекты, которые в настоящее время не поддерживаются JavaScript, такие как Активексобжект, Enumerator, Error, Global и VBArray.</span><span class="sxs-lookup"><span data-stu-id="9e788-105">However, JScript version 5.0 includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="9e788-106">JScript 5,0 поддерживает обработку исключений с помощью **try**... операторы **catch** .</span><span class="sxs-lookup"><span data-stu-id="9e788-106">JScript 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="9e788-107">В настоящее время JavaScript не предоставляет механизм обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="9e788-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="9e788-108">При работе с JScript или JavaScript существуют некоторые небольшие различия между реализациями объектной модели, поддерживаемыми различными веб-браузерами.</span><span class="sxs-lookup"><span data-stu-id="9e788-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="9e788-109">Чтобы написать сценарий, выполняемый как в Internet Explorer, так и в Netscape Navigator, ограничьте функции, используемые скриптами, указанными в стандарте консорциум W3C (W3C) для HTML версии 3,2.</span><span class="sxs-lookup"><span data-stu-id="9e788-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) standard for HTML version 3.2.</span></span> <span data-ttu-id="9e788-110">Дополнительные сведения об этом стандарте см. в разделе [эталонная спецификация HTML 3,2](https://www.w3.org/TR/REC-html32.html).</span><span class="sxs-lookup"><span data-stu-id="9e788-110">For more information about this standard, see [HTML 3.2 Reference Specification](https://www.w3.org/TR/REC-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e788-111">См. также</span><span class="sxs-lookup"><span data-stu-id="9e788-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e788-112">Преобразование в JScript</span><span class="sxs-lookup"><span data-stu-id="9e788-112">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




