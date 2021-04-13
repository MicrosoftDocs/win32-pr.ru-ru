---
title: Уровень отладки Direct2D
description: Расширение среды выполнения для Direct2D, которое предоставляет описательные сообщения об ошибках, обнаружение утечек объектов, уведомления о производительности и другие подсказки, помогающие создавать приложения Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410687"
---
# <a name="direct2d-debug-layer"></a><span data-ttu-id="2f3eb-103">Уровень отладки Direct2D</span><span class="sxs-lookup"><span data-stu-id="2f3eb-103">Direct2D Debug Layer</span></span>

## <a name="purpose"></a><span data-ttu-id="2f3eb-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="2f3eb-104">Purpose</span></span>

<span data-ttu-id="2f3eb-105">Слой отладки Direct2D, реализованный отдельно от Direct2D в собственной библиотеке DLL с именем d2d1debug.dll, предоставляет отладочные сообщения времени разработки для снижения сбоев приложения среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-105">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="2f3eb-106">Сообщения об отладке часто возникают из-за нарушений контрактов API, таких как недопустимые параметры (которые могут быть связаны с Direct3D), недопустимых ресурсов, нарушений потоков и других проблем с производительностью, таких как использование слоя при достаточном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-106">The debug messages often result from violations of API contracts such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and other performance issues such as using a layer when a clip would suffice.</span></span>

<span data-ttu-id="2f3eb-107">Чтобы решить, какой объем информации отслеживается слоем отладки, слой отладки предлагает три уровня отладки: сведения, предупреждение и ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-107">To help you decide how much information is traced by the debug layer, the debug layer offers three debug levels: information, warning, and error.</span></span> <span data-ttu-id="2f3eb-108">Эти три уровня интерпретируется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2f3eb-108">These three levels are interpreted as follows:</span></span>

-   <span data-ttu-id="2f3eb-109">**Ошибка:** Direct2D отправляет серьезные сообщения об ошибках на слой отладки.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-109">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="2f3eb-110">Например, при критическом ограничении потоков будет создаваться серьезная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-110">For example, breaking a threading constraint will generate a severe error.</span></span>

    <span data-ttu-id="2f3eb-111">Кроме того, сообщение об ошибке уровня активирует точку останова, которая поможет вам выполнить отладку.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-111">Further, a message of level error triggers the breakpoint to help you debug.</span></span>

-   <span data-ttu-id="2f3eb-112">**Предупреждение:** Direct2D отправляет сообщения об ошибках и предупреждения на слой отладки, чтобы можно было обращаться к любому из этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-112">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="2f3eb-113">**Сведения:** Direct2D отправляет сообщения об ошибках, предупреждения и дополнительные диагностические сведения на слой отладки.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-113">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="2f3eb-114">Например, сообщения улучшения производительности будут отправляться на этом уровне отладки.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-114">For example, performance improvement messages will be sent at this debug level.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2f3eb-115">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2f3eb-115">In this section</span></span>



| <span data-ttu-id="2f3eb-116">Раздел</span><span class="sxs-lookup"><span data-stu-id="2f3eb-116">Topic</span></span>                                                                                     | <span data-ttu-id="2f3eb-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2f3eb-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="2f3eb-118">Установка слоя отладки Direct2D</span><span class="sxs-lookup"><span data-stu-id="2f3eb-118">Installing the Direct2D Debug Layer</span></span>](installing-the-direct2d-debug-layer.md)<br/> | <span data-ttu-id="2f3eb-119">Описывает, как установить слой отладки Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-119">Describes how to install the Direct2D debug layer.</span></span><br/>      |
| [<span data-ttu-id="2f3eb-120">Общие сведения о слое отладки Direct2D</span><span class="sxs-lookup"><span data-stu-id="2f3eb-120">Direct2D Debug Layer Overview</span></span>](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [<span data-ttu-id="2f3eb-121">Сообщения отладки</span><span class="sxs-lookup"><span data-stu-id="2f3eb-121">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)<br/>                         | <span data-ttu-id="2f3eb-122">Выводит список сообщений отладки из слоя отладки Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-122">Lists the debug messages from the Direct2D Debug Layer.</span></span><br/> |



 

 

 





