---
title: Атрибуты ACF управления памятью
description: Атрибуты, перечисленные в следующей таблице, позволяют выполнять управление памятью со стороны клиента.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF MIDL, атрибуты, управление памятью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987455"
---
# <a name="memory-management-acf-attributes"></a><span data-ttu-id="46597-104">Атрибуты ACF управления памятью</span><span class="sxs-lookup"><span data-stu-id="46597-104">Memory Management ACF Attributes</span></span>

<span data-ttu-id="46597-105">Атрибуты, перечисленные в следующей таблице, позволяют выполнять управление памятью со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="46597-105">The attributes listed in the following table enable you to perform memory management from the client side.</span></span>



| <span data-ttu-id="46597-106">attribute</span><span class="sxs-lookup"><span data-stu-id="46597-106">Attribute</span></span>                                   | <span data-ttu-id="46597-107">Использование</span><span class="sxs-lookup"><span data-stu-id="46597-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46597-108">**allocate**</span><span class="sxs-lookup"><span data-stu-id="46597-108">**allocate**</span></span>](allocate.md)                | <span data-ttu-id="46597-109">Указывает способ выделения и освобождения памяти для клиентских приложений и заглушки для указателей.</span><span class="sxs-lookup"><span data-stu-id="46597-109">Specifies the way the client application and stub allocate and release memory for pointers.</span></span> <span data-ttu-id="46597-110">Этот атрибут особенно полезен, если требуется, чтобы определенные структуры указателей оставались доступными для серверного приложения после возврата вызова удаленной процедуры клиенту.</span><span class="sxs-lookup"><span data-stu-id="46597-110">This attribute is particularly useful when you want certain pointer structures to remain accessible to the server application after the remote procedure call returns to the client.</span></span> <span data-ttu-id="46597-111">Можно также использовать атрибут [**выделения**](allocate.md) , чтобы указать заглушке вычислить размер всей памяти, на которую ссылается указатель указанного типа, и выполнить один вызов для [**\_ \_ выделения пользователю MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="46597-111">You can also use the [**allocate**](allocate.md) attribute to direct the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span> |
| [<span data-ttu-id="46597-112">**\_число байтов**</span><span class="sxs-lookup"><span data-stu-id="46597-112">**byte\_count**</span></span>](byte-count.md)           | <span data-ttu-id="46597-113">Позволяет создать постоянный непрерывный блок памяти, который можно повторно использовать для нескольких удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="46597-113">Enables you to create a persistent, contiguous block of memory that can be reused over multiple remote procedure calls.</span></span> <span data-ttu-id="46597-114">Это освобождает клиентское приложение от затрат на многократное выделение и освобождение памяти, которая может включать несколько указателей и других сложных структур данных.</span><span class="sxs-lookup"><span data-stu-id="46597-114">This frees the client application from the overhead of repeatedly allocating and releasing memory that may include multiple pointers and other complex data structures.</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="46597-115">**включить \_ выделение**</span><span class="sxs-lookup"><span data-stu-id="46597-115">**enable\_allocate**</span></span>](enable-allocate.md) | <span data-ttu-id="46597-116">Указывает, что код заглушки сервера должен включать среду управления памятью заглушки.</span><span class="sxs-lookup"><span data-stu-id="46597-116">Specifies that the server stub code should enable the stub memory-management environment.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 