---
description: Векторные обработчики исключений являются расширением для структурированной обработки исключений.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Обработка векторных исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895894"
---
# <a name="vectored-exception-handling"></a><span data-ttu-id="7ae75-103">Обработка векторных исключений</span><span class="sxs-lookup"><span data-stu-id="7ae75-103">Vectored Exception Handling</span></span>

<span data-ttu-id="7ae75-104">Векторные обработчики исключений являются расширением для структурированной обработки исключений.</span><span class="sxs-lookup"><span data-stu-id="7ae75-104">Vectored exception handlers are an extension to structured exception handling.</span></span> <span data-ttu-id="7ae75-105">Приложение может зарегистрировать функцию для просмотра или обработки всех исключений приложения.</span><span class="sxs-lookup"><span data-stu-id="7ae75-105">An application can register a function to watch or handle all exceptions for the application.</span></span> <span data-ttu-id="7ae75-106">Векторные обработчики не основаны на кадрах, поэтому можно добавить обработчик, который будет вызываться независимо от того, где находится в кадре вызова.</span><span class="sxs-lookup"><span data-stu-id="7ae75-106">Vectored handlers are not frame-based, therefore, you can add a handler that will be called regardless of where you are in a call frame.</span></span> <span data-ttu-id="7ae75-107">Векторные обработчики вызываются в том порядке, в котором они были добавлены, когда отладчик получает первое уведомление о шансе, но до того, как система начнет раскрутить стек.</span><span class="sxs-lookup"><span data-stu-id="7ae75-107">Vectored handlers are called in the order that they were added, after the debugger gets a first chance notification, but before the system begins unwinding the stack.</span></span>

<span data-ttu-id="7ae75-108">Чтобы добавить векторный обработчик Continue, используйте функцию [**аддвекторедконтинуехандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="7ae75-108">To add a vectored continue handler, use the [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) function.</span></span> <span data-ttu-id="7ae75-109">Чтобы удалить этот обработчик, используйте функцию [**ремовевекторедконтинуехандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="7ae75-109">To remove this handler, use the [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) function.</span></span>

<span data-ttu-id="7ae75-110">Чтобы добавить векторный обработчик исключений, используйте функцию [**аддвекторедексцептионхандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="7ae75-110">To add a vectored exception handler, use the [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) function.</span></span> <span data-ttu-id="7ae75-111">Чтобы удалить этот обработчик, используйте функцию [**ремовевекторедексцептионхандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="7ae75-111">To remove this handler, use the [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) function.</span></span>

 

 
