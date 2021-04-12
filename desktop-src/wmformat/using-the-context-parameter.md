---
title: Использование параметра context
description: Использование параметра context
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Media Format SDK, параметр контекста
- Windows Media Format SDK, параметр Пвконтекст
- Пвконтекст, параметр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133475"
---
# <a name="using-the-context-parameter"></a><span data-ttu-id="a01aa-106">Использование параметра context</span><span class="sxs-lookup"><span data-stu-id="a01aa-106">Using the Context Parameter</span></span>

<span data-ttu-id="a01aa-107">Некоторые обратные вызовы, используемые пакетом SDK для формата Windows Media, принимают параметр с именем *пвконтекст*.</span><span class="sxs-lookup"><span data-stu-id="a01aa-107">Some of the callbacks used by the Windows Media Format SDK take a parameter called *pvContext*.</span></span> <span data-ttu-id="a01aa-108">Вызывающие объекты проходят по значению, указанному в методе, который начал асинхронного действия.</span><span class="sxs-lookup"><span data-stu-id="a01aa-108">The calling objects pass along the value you specify in the method that began the asynchronous action.</span></span> <span data-ttu-id="a01aa-109">Например, при вызове [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)можно передать значение для *пвконтекст*.</span><span class="sxs-lookup"><span data-stu-id="a01aa-109">For example, when you call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can pass a value for *pvContext*.</span></span> <span data-ttu-id="a01aa-110">Когда метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) вызывается объектом Reader для уведомления приложения о том, что файл был открыт, он передает любое значение, использованное в вызове **, в качестве параметра** *пвконтекст* в **OnStatus**.</span><span class="sxs-lookup"><span data-stu-id="a01aa-110">When the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method is called by the reader object to notify your application that the file has been opened, it will pass whatever value you used in your call to **Open** as the *pvContext* parameter of **OnStatus**.</span></span> <span data-ttu-id="a01aa-111">Этот параметр контекста предоставляется для использования, и его можно использовать любым способом.</span><span class="sxs-lookup"><span data-stu-id="a01aa-111">This context parameter is provided for your use and you can use it in any way you like.</span></span>

<span data-ttu-id="a01aa-112">Параметр *пвконтекст* чаще всего используется, если несколько объектов должны совместно использовать один и тот же обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="a01aa-112">The *pvContext* parameter is most often used when multiple objects need to share the same callback.</span></span> <span data-ttu-id="a01aa-113">Например, несколько объектов используют метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="a01aa-113">For example, several objects use the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="a01aa-114">*Пвконтекст* можно использовать, чтобы разрешить различным объектам совместно использовать одну реализацию **OnStatus** , передав другое значение для *пвконтекст* в исходном вызове.</span><span class="sxs-lookup"><span data-stu-id="a01aa-114">You can use *pvContext* to enable the different objects to share one implementation of **OnStatus** by passing a different value for *pvContext* on your original call.</span></span> <span data-ttu-id="a01aa-115">В реализации **OnStatus** логику обработки сообщений можно создать с учетом значения *пвконтекст*.</span><span class="sxs-lookup"><span data-stu-id="a01aa-115">In your implementation of **OnStatus**, you can branch the message handling logic based on the value of *pvContext*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a01aa-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a01aa-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a01aa-117">**Использование методов обратного вызова**</span><span class="sxs-lookup"><span data-stu-id="a01aa-117">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




