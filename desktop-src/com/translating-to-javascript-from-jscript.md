---
title: Преобразование в JavaScript из JScript
description: Преобразование в JavaScript из JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412615"
---
# <a name="translating-to-javascript-from-jscript"></a><span data-ttu-id="34e6b-103">Преобразование в JavaScript из JScript</span><span class="sxs-lookup"><span data-stu-id="34e6b-103">Translating to JavaScript from JScript</span></span>

<span data-ttu-id="34e6b-104">JScript в значительной степени совместим с JavaScript.</span><span class="sxs-lookup"><span data-stu-id="34e6b-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="34e6b-105">Однако в JScript есть некоторые объекты, которые в настоящее время не поддерживаются JavaScript, такие как Активексобжект, Enumerator, Error, Global и VBArray.</span><span class="sxs-lookup"><span data-stu-id="34e6b-105">However, JScript includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="34e6b-106">JScript версии 5,0 поддерживает обработку исключений с помощью **try**... операторы **catch** .</span><span class="sxs-lookup"><span data-stu-id="34e6b-106">JScript version 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="34e6b-107">В настоящее время JavaScript не предоставляет механизм обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="34e6b-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="34e6b-108">При работе с JScript или JavaScript существуют некоторые небольшие различия между реализациями объектной модели, поддерживаемыми различными веб-браузерами.</span><span class="sxs-lookup"><span data-stu-id="34e6b-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="34e6b-109">Чтобы написать сценарий, выполняемый как в Internet Explorer, так и в Netscape Navigator, ограничьте функции, используемые скриптами, указанными в стандарте консорциум W3C (W3C) [для HTML версии 3,2](https://www.w3.org/tr/rec-html32.html).</span><span class="sxs-lookup"><span data-stu-id="34e6b-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) [standard for HTML version 3.2](https://www.w3.org/tr/rec-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="34e6b-110">См. также</span><span class="sxs-lookup"><span data-stu-id="34e6b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34e6b-111">Преобразование в JavaScript</span><span class="sxs-lookup"><span data-stu-id="34e6b-111">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




