---
title: Создание скриптов для COM-объектов в пользовательских приложениях
description: Создание скриптов для COM-объектов в пользовательских приложениях
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253162"
---
# <a name="scripting-com-objects-in-custom-applications"></a><span data-ttu-id="ba72a-103">Создание скриптов для COM-объектов в пользовательских приложениях</span><span class="sxs-lookup"><span data-stu-id="ba72a-103">Scripting COM Objects in Custom Applications</span></span>

<span data-ttu-id="ba72a-104">Корпорация Майкрософт предоставляет несколько сред для написания сценариев COM-объектов: Active Server страниц, сервера сценариев Windows и т. д.</span><span class="sxs-lookup"><span data-stu-id="ba72a-104">Microsoft provides several environments for scripting COM objects: Active Server Pages, Windows Script Host, and so on.</span></span> <span data-ttu-id="ba72a-105">Независимые поставщики программного обеспечения (ISV) также могут лицензировать обработчики сценариев Майкрософт для использования в своих приложениях.</span><span class="sxs-lookup"><span data-stu-id="ba72a-105">Independent software vendors (ISVs) can also license Microsoft scripting engines for use in their applications.</span></span> <span data-ttu-id="ba72a-106">Например, ISV, создающий текстовый процессор, может добавить в приложение язык макроса, чтобы пользователи могли автоматизировать простые задачи.</span><span class="sxs-lookup"><span data-stu-id="ba72a-106">For example, an ISV creating a word processor might want to add a macro language to the application so users could automate simple tasks.</span></span> <span data-ttu-id="ba72a-107">При лицензировании обработчика сценариев независимые поставщики программного обеспечения могут использовать в качестве языка макросов приложения такой язык, как VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="ba72a-107">By licensing a scripting engine, the ISV can use a language such as VBScript or JScript as the application's macro language.</span></span>

<span data-ttu-id="ba72a-108">Помимо лицензирования VBScript и обработчиков сценариев JScript независимые поставщики программного обеспечения могут создавать собственные обработчики скриптов ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ba72a-108">In addition to licensing VBScript and JScript scripting engines, ISVs can write their own ActiveX scripting engines.</span></span> <span data-ttu-id="ba72a-109">Затем эти обработчики сценариев могут быть подключены к любой среде размещения, поддерживающей стандарт обработчика скриптов ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ba72a-109">These scripting engines can then be plugged into any host environment that supports the ActiveX scripting engine standard.</span></span> <span data-ttu-id="ba72a-110">Например, независимый поставщик программного обеспечения может написать обработчик сценариев Перлскрипт и установить его на сервере ASP, что позволит серверу ASP обрабатывать сценарии Перлскрипт.</span><span class="sxs-lookup"><span data-stu-id="ba72a-110">For example, an ISV might write a PerlScript scripting engine and install it on an ASP server, thus enabling the ASP server to process PerlScript scripts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba72a-111">См. также</span><span class="sxs-lookup"><span data-stu-id="ba72a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba72a-112">Создание сценариев с помощью COM-объектов</span><span class="sxs-lookup"><span data-stu-id="ba72a-112">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




