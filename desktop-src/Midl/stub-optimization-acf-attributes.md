---
title: Атрибуты ACF для оптимизации заглушек
description: Эти атрибуты позволяют оптимизировать размер и скорость кода заглушки.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF MIDL, атрибуты, оптимизация с заглушкой
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888119"
---
# <a name="stub-optimization-acf-attributes"></a><span data-ttu-id="86a9a-104">Атрибуты ACF для оптимизации заглушек</span><span class="sxs-lookup"><span data-stu-id="86a9a-104">Stub Optimization ACF Attributes</span></span>

<span data-ttu-id="86a9a-105">Эти атрибуты позволяют оптимизировать размер и скорость кода заглушки.</span><span class="sxs-lookup"><span data-stu-id="86a9a-105">These attributes enable you to optimize the size and speed of your stub code.</span></span>



| <span data-ttu-id="86a9a-106">attribute</span><span class="sxs-lookup"><span data-stu-id="86a9a-106">Attribute</span></span>                                    | <span data-ttu-id="86a9a-107">Использование</span><span class="sxs-lookup"><span data-stu-id="86a9a-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86a9a-108">[**код кода**](code.md)[](nocode.md)</span><span class="sxs-lookup"><span data-stu-id="86a9a-108">[**code**](code.md)[**nocode**](nocode.md)</span></span> | <span data-ttu-id="86a9a-109">Используйте вместе [](code.md) атрибуты код [**и код,**](nocode.md) чтобы избежать создания кода-заглушки для неиспользуемых функций.</span><span class="sxs-lookup"><span data-stu-id="86a9a-109">Use the [**code**](code.md) and [**nocode**](nocode.md) attributes together to avoid generating stub code for unused functions.</span></span> <span data-ttu-id="86a9a-110">Примените **атрибут InAttribute** к заголовку интерфейса и примените атрибут **Code** к этим процедурам, которые будет реализовывать клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="86a9a-110">Apply the **nocode** attribute to the interface header, and apply the **code** attribute to those procedures that the client application will implement.</span></span> <span data-ttu-id="86a9a-111">Код заглушки клиента будет создан только для выбранных процедур.</span><span class="sxs-lookup"><span data-stu-id="86a9a-111">Client stub code will be generated only for the selected procedures.</span></span>                                                                |
| [<span data-ttu-id="86a9a-112">**увеличить**</span><span class="sxs-lookup"><span data-stu-id="86a9a-112">**optimize**</span></span>](optimize.md)                 | <span data-ttu-id="86a9a-113">Позволяет точно настроить уровень оптимизации, выполняемый компилятором MIDL при создании кода-заглушки, указав, что данные должны быть упакованы в смешанном режиме или интерпретированном методе.</span><span class="sxs-lookup"><span data-stu-id="86a9a-113">Lets you fine-tune the level of optimization that the MIDL compiler performs when generating stub code, by specifying that data is to be marshaled by either the mixed-mode or interpreted method.</span></span> <span data-ttu-id="86a9a-114">Атрибут [**optimize**](optimize.md) можно применить к интерфейсу или к выбранным функциям в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="86a9a-114">You can apply the [**optimize**](optimize.md) attribute to an interface or to selected functions within the interface.</span></span> <span data-ttu-id="86a9a-115">В любом случае его использование переопределит оптимизацию командной строки и все существовавшие ранее значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86a9a-115">In either case, its use will override the command-line optimizations and any pre-existing defaults.</span></span> |



 

 

 




