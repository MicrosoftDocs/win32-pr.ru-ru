---
title: Типы данных и возвращаемые значения функции
description: Типы данных и возвращаемые значения функции
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986396"
---
# <a name="function-data-types-and-return-values"></a><span data-ttu-id="c0f0d-103">Типы данных и возвращаемые значения функции</span><span class="sxs-lookup"><span data-stu-id="c0f0d-103">Function Data Types and Return Values</span></span>

<span data-ttu-id="c0f0d-104">Функции и макросы Авифиле используют обработчики файлов и потоков, реализованные с помощью технологии OLE.</span><span class="sxs-lookup"><span data-stu-id="c0f0d-104">The AVIFile functions and macros use file and stream handlers implemented with OLE technology.</span></span> <span data-ttu-id="c0f0d-105">Стандартный тип данных функции OLE — **стдапи**, а функция возвращает значение **HRESULT** (ноль для успешного выполнения или ошибка в противном случае).</span><span class="sxs-lookup"><span data-stu-id="c0f0d-105">The standard data type of an OLE function is **STDAPI**, and the function returns an **HRESULT** value (zero for success or an error otherwise).</span></span> <span data-ttu-id="c0f0d-106">Если функция возвращает значение, отличное от **HRESULT**, тип прототипа функции немного отличается от синтаксиса, который внедряет тип возвращаемого значения в круглые скобки после "стдапи \_ ".</span><span class="sxs-lookup"><span data-stu-id="c0f0d-106">If a function returns a value other than an **HRESULT**, the type of the function's prototype has a slightly different syntax that embeds the return value type in parentheses following "STDAPI\_".</span></span> <span data-ttu-id="c0f0d-107">Например, функция, возвращающая значение **типа Long** Data, использует **стдапи \_ (Long)** в инструкции prototype.</span><span class="sxs-lookup"><span data-stu-id="c0f0d-107">For example, a function that returns a **LONG** data value uses **STDAPI\_(LONG)** in the prototype statement.</span></span>

 

 




