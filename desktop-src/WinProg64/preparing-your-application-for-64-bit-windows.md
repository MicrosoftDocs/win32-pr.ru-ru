---
title: Подготовка приложения для 64-разрядной версии Windows
description: Существует несколько функций, упрощающих разработку приложений, которые будут работать как в 32, так и в 64-разрядной версии Windows. Большинство из них, например новые типы данных, описаны в разделе Подготовка к 64-разрядной версии Windows.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- 64-разрядный набор средств 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260989"
---
# <a name="preparing-your-application-for-64-bit-windows"></a><span data-ttu-id="75313-105">Подготовка приложения для 64-разрядной версии Windows</span><span class="sxs-lookup"><span data-stu-id="75313-105">Preparing Your Application for 64-bit Windows</span></span>

<span data-ttu-id="75313-106">Существует несколько функций, упрощающих разработку приложений, которые будут работать как в 32, так и в 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="75313-106">There are several features that make it easier for you to develop applications that will run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="75313-107">Большинство из них, например новые типы данных, описаны в разделе Подготовка к [64-разрядной версии Windows](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="75313-107">Most of these, such as the new data types, are described in [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

<span data-ttu-id="75313-108">64-разрядный набор средств, поставляемый с Windows SDK, включает в себя 64-разрядный компилятор MIDL, Midl.exe для создания собственных 64-разрядных заглушек, а также 32-разрядные заглушки.</span><span class="sxs-lookup"><span data-stu-id="75313-108">The 64-bit toolkit that ships with the Windows SDK includes a 64-bit MIDL compiler, Midl.exe, for generating native 64-bit stubs, as well as 32-bit stubs.</span></span> <span data-ttu-id="75313-109">Используйте коммутатор **/env Win64** для создания только 64-разрядных заглушек.</span><span class="sxs-lookup"><span data-stu-id="75313-109">Use the **/env win64** switch to generate 64-bit stubs only.</span></span> <span data-ttu-id="75313-110">По умолчанию создаются двойные заглушки, которые работают на обеих платформах.</span><span class="sxs-lookup"><span data-stu-id="75313-110">The default is to generate dual stubs that run on both platforms.</span></span>

<span data-ttu-id="75313-111">Обратите внимание, что 64-разрядный MIDL поддерживает только режимы оптимизации [**/Oicf**](/windows/desktop/Midl/-oi) и [**/OS**](/windows/desktop/Midl/-os) .</span><span class="sxs-lookup"><span data-stu-id="75313-111">Note that the 64-bit MIDL supports the [**/Oicf**](/windows/desktop/Midl/-oi) and [**/Os**](/windows/desktop/Midl/-os) optimization modes only.</span></span>

 

 