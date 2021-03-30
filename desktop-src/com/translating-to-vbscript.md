---
title: Преобразование в VBScript
description: Преобразование в VBScript
ms.assetid: 12eac4bd-06d9-45db-81c2-0591200cbacc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b9f64e25a22ffe83c148c1fd1b7a7603b8f3f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253072"
---
# <a name="translating-to-vbscript"></a><span data-ttu-id="9846f-103">Преобразование в VBScript</span><span class="sxs-lookup"><span data-stu-id="9846f-103">Translating to VBScript</span></span>

<span data-ttu-id="9846f-104">VBScript — это подмножество языка Microsoft Visual Basic для приложений.</span><span class="sxs-lookup"><span data-stu-id="9846f-104">VBScript is a subset of the Microsoft Visual Basic for Applications language.</span></span> <span data-ttu-id="9846f-105">Поскольку VBScript предназначен для безопасного использования в клиентских приложениях, таких как веб-страницы, он не предоставляет входные и выходные данные файлов или прямой доступ к базовой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="9846f-105">Because VBScript is intended to be safe for use in client-side applications such as webpages, it does not provide file input and output or direct access to the underlying operating system.</span></span> <span data-ttu-id="9846f-106">Это предотвращает удаление или изменение файлов на компьютере с помощью веб-скрипта.</span><span class="sxs-lookup"><span data-stu-id="9846f-106">This prevents a Web-based script from deleting or altering files on your computer.</span></span> <span data-ttu-id="9846f-107">Полный список функций Visual Basic, которые не поддерживаются в VBScript, см. в документации по Visual Basic для приложений.</span><span class="sxs-lookup"><span data-stu-id="9846f-107">For a complete list of Visual Basic features that are not supported in VBScript, see the Visual Basic for Applications documentation.</span></span>

<span data-ttu-id="9846f-108">Помимо языковых возможностей, предоставляемых VBScript, сервер сценариев может также предоставлять объектную модель VBScript, к которой может обращаться ваш скрипт.</span><span class="sxs-lookup"><span data-stu-id="9846f-108">In addition to the language features provided by VBScript, the scripting host may also expose a VBScript object model that your script can access.</span></span> <span data-ttu-id="9846f-109">Например, Internet Explorer предоставляет объектную модель, позволяющую сценариям взаимодействовать с браузером и программно управлять им.</span><span class="sxs-lookup"><span data-stu-id="9846f-109">For example, Internet Explorer exposes an object model that enables scripts to interact with and programmatically control the browser.</span></span> <span data-ttu-id="9846f-110">Дополнительные сведения о работе с такими объектными моделями см. в документации на сервере сценариев.</span><span class="sxs-lookup"><span data-stu-id="9846f-110">For more information about working with such object models, see the documentation on your scripting host.</span></span>

<span data-ttu-id="9846f-111">В следующих разделах описываются проблемы, которые следует учитывать при преобразовании сценария в VBScript из JavaScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="9846f-111">The following topics describe issues you should consider when translating a script to VBScript from JavaScript or JScript:</span></span>

-   [<span data-ttu-id="9846f-112">Преобразование в VBScript из JScript</span><span class="sxs-lookup"><span data-stu-id="9846f-112">Translating to VBScript from JScript</span></span>](translating-to-vbscript-from-jscript.md)
-   [<span data-ttu-id="9846f-113">Преобразование в VBScript из JavaScript</span><span class="sxs-lookup"><span data-stu-id="9846f-113">Translating to VBScript from JavaScript</span></span>](translating-to-vbscript-from-javascript.md)

## <a name="related-topics"></a><span data-ttu-id="9846f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="9846f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9846f-115">Преобразование в JavaScript</span><span class="sxs-lookup"><span data-stu-id="9846f-115">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> <dt>

[<span data-ttu-id="9846f-116">Преобразование в JScript</span><span class="sxs-lookup"><span data-stu-id="9846f-116">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




