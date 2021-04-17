---
title: Маршалирование интерфейса
description: Маршалирование интерфейса
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700937"
---
# <a name="interface-marshaling"></a><span data-ttu-id="6a8e7-103">Маршалирование интерфейса</span><span class="sxs-lookup"><span data-stu-id="6a8e7-103">Interface Marshaling</span></span>

<span data-ttu-id="6a8e7-104">Если вы не уверены, что ваш интерфейс никогда не будет использоваться в границах апартамента, потока или процесса, необходимо решить, как обеспечить поддержку маршалирования для интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-104">Unless you know beyond all doubt that your interface will never be used across apartment, thread, or process boundaries, you need to decide how to provide marshaling support for your interfaces.</span></span> <span data-ttu-id="6a8e7-105">Существует три способа обеспечения поддержки маршалирования:</span><span class="sxs-lookup"><span data-stu-id="6a8e7-105">There are three ways to provide marshaling support:</span></span>

-   <span data-ttu-id="6a8e7-106">Напишите собственный код прокси или заглушки, который вызывает канал COM, который, в свою очередь, вызывает библиотеки времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-106">Write your own proxy/stub code that calls the COM channel, which in turn calls the RPC run-time libraries.</span></span> <span data-ttu-id="6a8e7-107">Теоретически это можно сделать, но на практике практически невозможно выполнить без значительного объема усилий.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-107">Theoretically, it is possible to do this, but in practice it is almost impossible to do without a significant amount of effort.</span></span>
-   <span data-ttu-id="6a8e7-108">Опишите интерфейсы в файле языка определения интерфейса (IDL) и используйте компилятор MIDL для создания библиотеки прокси-сервера или заглушки.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-108">Describe your interfaces in an interface definition language (IDL) file and use the MIDL compiler to generate a proxy/stub DLL.</span></span> <span data-ttu-id="6a8e7-109">Этот метод обеспечивает максимальную производительность и максимальную гибкость в отношении допустимых типов данных.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-109">This method provides the best performance and the most flexibility in terms of acceptable data types.</span></span> <span data-ttu-id="6a8e7-110">Используя заглушки прокси-сервера, созданные с помощью MIDL, можно управлять не только управлением памятью, но даже упаковкой и распаковкой сложных типов данных на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-110">Using MIDL-generated proxy stubs, you can control not only memory management but even the marshaling and unmarshaling of complex data types across different platforms.</span></span>
-   <span data-ttu-id="6a8e7-111">Используйте MIDL для создания библиотеки типов, которую система использует для обеспечения поддержки маршалирования во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-111">Use MIDL to generate a type library that the system uses to provide marshaling support at run time.</span></span> <span data-ttu-id="6a8e7-112">Это самый простой способ реализации поддержки упаковки.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-112">This is the easiest way to implement marshaling support.</span></span> <span data-ttu-id="6a8e7-113">Все, что нужно сделать, — это создать библиотеку типов и зарегистрировать ее.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-113">All you have to do is generate a type library and register it.</span></span> <span data-ttu-id="6a8e7-114">Интерфейсы должны быть совместимы со службой автоматизации ( [**oleautomation**](/windows/desktop/Midl/oleautomation) или [**Dual**](/windows/desktop/Midl/dual)), которая помещает некоторые ограничения на типы данных, которые можно использовать в качестве параметров метода.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-114">Your interfaces must be Automation-compatible (either [**oleautomation**](/windows/desktop/Midl/oleautomation) or [**dual**](/windows/desktop/Midl/dual)), which places some restrictions on the kinds of data types you can use as method parameters.</span></span> <span data-ttu-id="6a8e7-115">Однако в большинстве случаев преимущество использования интерфейсов для программ, написанных на других языках, таких как Microsoft Visual Basic и Java, приводит к нарушениям ограничений на типы данных.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-115">However, in most cases, the advantage of having your interfaces accessible to programs written in other languages, such as Microsoft Visual Basic and Java, outweighs the limitations on data types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a8e7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6a8e7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a8e7-117">Обмен данными между объектами</span><span class="sxs-lookup"><span data-stu-id="6a8e7-117">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> </dl>

 

 