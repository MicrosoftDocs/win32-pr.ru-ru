---
title: Использование нескольких обработчиков контекста на один вызов
description: Возможность использования массивов дескрипторов контекста в том случае, когда параметры становятся доступными в Windows Vista и более поздних операционных системах.
ms.assetid: 84f3036b-ff4d-485d-bf23-ad10a03076a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7b1c69dd182bee8f68e7068bcfcef60efd380a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888371"
---
# <a name="using-more-than-one-context-handle-per-call"></a><span data-ttu-id="534b6-103">Использование нескольких обработчиков контекста на один вызов</span><span class="sxs-lookup"><span data-stu-id="534b6-103">Using More than One Context Handle per Call</span></span>

<span data-ttu-id="534b6-104">Возможность использования массивов дескрипторов контекста в том случае, когда параметры становятся доступными в Windows Vista и более поздних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="534b6-104">The ability to use arrays of context handles as parameters is made available in Windows Vista and later operating systems.</span></span> <span data-ttu-id="534b6-105">Однако эту функцию следует использовать в приложении аккуратно.</span><span class="sxs-lookup"><span data-stu-id="534b6-105">However, this feature should be used carefully within an application.</span></span> <span data-ttu-id="534b6-106">Например, в ситуации, когда маркер контекста используется в нескольких вызовах, отслеживание его использования становится все труднее.</span><span class="sxs-lookup"><span data-stu-id="534b6-106">For example, in a situation where a context handle is being used in multiple calls it becomes increasingly difficult to keep track of its use.</span></span>

 

 




