---
title: Драйверы (руководством по программированию для 64-разрядной версии Windows)
description: 64-разрядная версия Windows предназначена для того, чтобы разработчики использовали одну базу исходного кода для своих 32-и 64-разрядных приложений. В большой степени это также справедливо для 32-разрядных и 64-разрядных драйверов Windows.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- драйверы 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340210"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a><span data-ttu-id="966ca-105">Драйверы (руководством по программированию для 64-разрядной версии Windows)</span><span class="sxs-lookup"><span data-stu-id="966ca-105">Drivers (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="966ca-106">64-разрядная версия Windows предназначена для того, чтобы разработчики использовали одну базу исходного кода для своих 32-и 64-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="966ca-106">The 64-bit version of Windows is designed to make it possible for developers to use a single source-code base for their 32-bit and 64-bit applications.</span></span> <span data-ttu-id="966ca-107">В большой степени это также справедливо для 32-разрядных и 64-разрядных драйверов Windows.</span><span class="sxs-lookup"><span data-stu-id="966ca-107">To a large extent, this is also true for 32-bit and 64-bit Windows drivers.</span></span>

<span data-ttu-id="966ca-108">Однако 32-разрядные драйверы не могут работать в 64-разрядной версии Windows и должны быть перенесены.</span><span class="sxs-lookup"><span data-stu-id="966ca-108">However, 32-bit drivers cannot run on 64-bit Windows and must be ported.</span></span> <span data-ttu-id="966ca-109">Для приложений, работающих в пользовательском режиме, в 64-разрядной ОС Windows есть WOW64, который позволяет выполнять 32-разрядные приложения Windows (с потерей производительности) в системах под управлением 64-bit Windows.</span><span class="sxs-lookup"><span data-stu-id="966ca-109">For user-mode applications, 64-bit Windows includes WOW64, which enables 32-bit Windows applications to execute (with some loss of performance) on systems running 64-bit Windows.</span></span> <span data-ttu-id="966ca-110">Для драйверов не существует эквивалентного слоя перевода.</span><span class="sxs-lookup"><span data-stu-id="966ca-110">No equivalent translation layer exists for drivers.</span></span>

<span data-ttu-id="966ca-111">Сведения о переносе драйверов в 64-разрядную версию Windows см. в статье [64-разрядные проблемы](https://msdn.microsoft.com/library/aa489627.aspx) в наборе драйверов для Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="966ca-111">For information about porting drivers to 64-bit Windows, see [64-Bit Issues](https://msdn.microsoft.com/library/aa489627.aspx) in the Windows Driver Kit (WDK).</span></span>

 

 




