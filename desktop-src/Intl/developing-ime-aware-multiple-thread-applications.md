---
description: Модуль IMM включает проверку идентификации потоков, которая определяет, является ли вызывающий поток создателем указанного дескриптора контекста входного метода (типа ХИМК) или дескриптора окна (типа HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Разработка IME-Aware приложений с несколькими потоками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684256"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a><span data-ttu-id="25f42-103">Разработка IME-Aware приложений с несколькими потоками</span><span class="sxs-lookup"><span data-stu-id="25f42-103">Developing IME-Aware Multiple-thread Applications</span></span>

<span data-ttu-id="25f42-104">Модуль IMM включает проверку идентификации потоков, которая определяет, является ли вызывающий поток создателем указанного дескриптора контекста входного метода (типа ХИМК) или дескриптора окна (типа HWND).</span><span class="sxs-lookup"><span data-stu-id="25f42-104">The IMM includes thread identification checking that determines if a calling thread is the creator of a specified input method context handle (HIMC type) or window handle (HWND type).</span></span> <span data-ttu-id="25f42-105">Если поток не является создателем маркера, вызываемая функция IMM завершается с ошибкой, а последующий вызов [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку \_ Недопустимый \_ доступ.</span><span class="sxs-lookup"><span data-stu-id="25f42-105">If the thread is not the creator of the handle, the called IMM function fails and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_ACCESS.</span></span>

> [!Note]  
> <span data-ttu-id="25f42-106">Текущая архитектура IMM не предоставляет средство синхронизации для доступа к дескрипторам IMM.</span><span class="sxs-lookup"><span data-stu-id="25f42-106">The current IMM architecture does not provide a synchronization facility for access to IMM handles.</span></span>

 

<span data-ttu-id="25f42-107">Чтобы использовать проверку идентификации потоков, приложения должны соблюдать следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="25f42-107">To use thread identification checking, your applications must adhere to the following guidelines:</span></span>

-   <span data-ttu-id="25f42-108">Поток не должен обращаться к входному контексту, созданному другим потоком.</span><span class="sxs-lookup"><span data-stu-id="25f42-108">A thread should not access the input context created by another thread.</span></span>
-   <span data-ttu-id="25f42-109">Поток не должен связывать входной контекст с окном, созданным другим потоком, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="25f42-109">A thread should not associate an input context with a window created by another thread, and vice versa.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25f42-110">См. также</span><span class="sxs-lookup"><span data-stu-id="25f42-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25f42-111">Использование диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="25f42-111">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
