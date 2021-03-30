---
title: Использование методов обратного вызова
description: Использование методов обратного вызова
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Пакет SDK для формата Windows Media, методы обратного вызова
- Пакет SDK Windows Media Format, методы, вызываемые асинхронно
- методы обратного вызова
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788701"
---
# <a name="using-the-callback-methods"></a><span data-ttu-id="8a347-106">Использование методов обратного вызова</span><span class="sxs-lookup"><span data-stu-id="8a347-106">Using the Callback Methods</span></span>

<span data-ttu-id="8a347-107">Несколько интерфейсов в пакете SDK формата Windows Media содержат методы, которые вызываются асинхронно.</span><span class="sxs-lookup"><span data-stu-id="8a347-107">Several interfaces in the Windows Media Format SDK contain methods that are called asynchronously.</span></span> <span data-ttu-id="8a347-108">Большинство из этих методов используют функции обратного вызова для передачи информации в управляющее приложение.</span><span class="sxs-lookup"><span data-stu-id="8a347-108">Most of these methods use callback functions to pass information to the controlling application.</span></span>

<span data-ttu-id="8a347-109">В следующих разделах описаны некоторые общие проблемы, связанные с использованием методов обратного вызова в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8a347-109">The following sections describe some of the general issues regarding the use of callback methods with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="8a347-110">Section</span><span class="sxs-lookup"><span data-stu-id="8a347-110">Section</span></span>                                                                          | <span data-ttu-id="8a347-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8a347-111">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a347-112">Использование обратного вызова OnStatus</span><span class="sxs-lookup"><span data-stu-id="8a347-112">Using the OnStatus Callback</span></span>](using-the-onstatus-callback.md)                   | <span data-ttu-id="8a347-113">Описывает, как реализовать метод обратного вызова [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , который используется несколькими объектами для уведомления приложений о ходе выполнения операции пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="8a347-113">Describes how to implement the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, which is used by several objects to advise applications of SDK operation progress.</span></span> |
| [<span data-ttu-id="8a347-114">Использование событий с асинхронными вызовами</span><span class="sxs-lookup"><span data-stu-id="8a347-114">Using Events with Asynchronous Calls</span></span>](using-events-with-asynchronous-calls.md) | <span data-ttu-id="8a347-115">Описывает распространенный способ работы с асинхронными вызовами методов в приложении.</span><span class="sxs-lookup"><span data-stu-id="8a347-115">Describes a common technique to handle asynchronous method calls in an application.</span></span>                                                                                                                  |
| [<span data-ttu-id="8a347-116">Использование параметра context</span><span class="sxs-lookup"><span data-stu-id="8a347-116">Using the Context Parameter</span></span>](using-the-context-parameter.md)                   | <span data-ttu-id="8a347-117">Представляет параметр *пвконтекст* , совместно используемый несколькими обратными вызовами и их вызывающими методами, и объясняет, как его использовать.</span><span class="sxs-lookup"><span data-stu-id="8a347-117">Introduces the *pvContext* parameter, shared by several callbacks and their calling methods, and explains how to use it.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="8a347-118">См. также</span><span class="sxs-lookup"><span data-stu-id="8a347-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a347-119">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="8a347-119">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




