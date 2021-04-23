---
title: Атрибуты функций
description: Атрибуты \ callback \ и \ Local \ могут применяться в качестве атрибутов функций.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793381"
---
# <a name="function-attributes"></a><span data-ttu-id="8b211-103">Атрибуты функций</span><span class="sxs-lookup"><span data-stu-id="8b211-103">Function Attributes</span></span>

<span data-ttu-id="8b211-104">**\[** [**Обратный вызов**](/windows/desktop/Midl/callback) **\]** и **\[** [**локальные**](/windows/desktop/Midl/local) **\]** атрибуты можно применять в качестве атрибутов функций.</span><span class="sxs-lookup"><span data-stu-id="8b211-104">The **\[**[**callback**](/windows/desktop/Midl/callback)**\]** and **\[**[**local**](/windows/desktop/Midl/local)**\]** attributes can be applied as function attributes.</span></span>

<span data-ttu-id="8b211-105">Обратный вызов — это удаленный вызов от сервера к клиенту, который выполняется как часть концептуального потока с одним выполнением.</span><span class="sxs-lookup"><span data-stu-id="8b211-105">A callback is a remote call from server to client that executes as part of a conceptual single-execution thread.</span></span> <span data-ttu-id="8b211-106">Обратный вызов всегда выдается в контексте удаленного вызова (или обратного вызова) и выполняется потоком, который выдал исходный удаленный вызов (или обратный вызов).</span><span class="sxs-lookup"><span data-stu-id="8b211-106">A callback is always issued in the context of a remote call (or callback) and is executed by the thread that issued the original remote call (or callback).</span></span>

<span data-ttu-id="8b211-107">Часто желательно поместить объявление локальной процедуры в IDL-файл, так как это логическое место для описания интерфейсов пакета.</span><span class="sxs-lookup"><span data-stu-id="8b211-107">It is often desirable to place a local procedure declaration in the IDL file, since this is the logical place to describe interfaces to a package.</span></span> <span data-ttu-id="8b211-108">**\[** [**Локальный**](/windows/desktop/Midl/local) **\]** атрибут указывает на то, что объявление процедуры на самом деле не является удаленной функцией, а локальной процедурой.</span><span class="sxs-lookup"><span data-stu-id="8b211-108">The **\[**[**local**](/windows/desktop/Midl/local)**\]** attribute indicates that a procedure declaration is not actually a remote function, but a local procedure.</span></span> <span data-ttu-id="8b211-109">Компилятор MIDL не создает никаких заглушек для функций с **\[ локальным \]** атрибутом.</span><span class="sxs-lookup"><span data-stu-id="8b211-109">The MIDL compiler does not generate any stubs for functions with the **\[local\]** attribute.</span></span>

<span data-ttu-id="8b211-110">Важно отметить, что использование **\[** [**обратного вызова**](/windows/desktop/Midl/callback) **\]** не рекомендуется в многопоточном программировании.</span><span class="sxs-lookup"><span data-stu-id="8b211-110">It is important to note that the use of **\[**[**callback**](/windows/desktop/Midl/callback)**\]** is not recommended in multi-thread programming.</span></span> <span data-ttu-id="8b211-111">Как однопотоковое программное обеспечение, оно не поддерживает требования безопасности для многопотоковой среды.</span><span class="sxs-lookup"><span data-stu-id="8b211-111">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

 

 