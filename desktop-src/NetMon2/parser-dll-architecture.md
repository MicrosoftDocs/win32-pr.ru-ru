---
description: Архитектура библиотеки DLL средства синтаксического анализа должна предоставлять функции, показанные на следующем рисунке.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Архитектура библиотеки DLL средства синтаксического анализа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498144"
---
# <a name="parser-dll-architecture"></a><span data-ttu-id="1a0ce-103">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="1a0ce-103">Parser DLL Architecture</span></span>

<span data-ttu-id="1a0ce-104">Архитектура библиотеки DLL средства синтаксического анализа должна предоставлять функции, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="1a0ce-104">The architecture of the parser DLL must provide the features shown in the following illustration.</span></span> <span data-ttu-id="1a0ce-105">Имейте в виду, что для некоторых функций требуется реализация только одной точки входа.</span><span class="sxs-lookup"><span data-stu-id="1a0ce-105">Be aware that some features require the implementation of only one entry point.</span></span> <span data-ttu-id="1a0ce-106">Однако если библиотека DLL средства синтаксического анализа поддерживает несколько протоколов, то для этой функции требуется реализация нескольких точек входа.</span><span class="sxs-lookup"><span data-stu-id="1a0ce-106">However, if your parser DLL supports multiple protocols, then the feature requires the implementation of multiple entry points.</span></span>

![функции библиотеки DLL средства синтаксического анализа](images/parserarchitecture1.png)



| <span data-ttu-id="1a0ce-108">Сведения о</span><span class="sxs-lookup"><span data-stu-id="1a0ce-108">For information about</span></span>                                                  | <span data-ttu-id="1a0ce-109">См.</span><span class="sxs-lookup"><span data-stu-id="1a0ce-109">See</span></span>                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1a0ce-110">Реализация функций экспорта библиотеки DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="1a0ce-110">How to implement parser DLL export functions.</span></span>                          | [<span data-ttu-id="1a0ce-111">Написание средства синтаксического анализа протокола</span><span class="sxs-lookup"><span data-stu-id="1a0ce-111">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="1a0ce-112">Конкретные функции и структуры, используемые анализаторами — справочные разделы.</span><span class="sxs-lookup"><span data-stu-id="1a0ce-112">Specific functions and structures that parsers use — reference topics.</span></span> | [<span data-ttu-id="1a0ce-113">Функции и структуры средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="1a0ce-113">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



