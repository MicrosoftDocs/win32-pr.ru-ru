---
title: Подготовка к 64-разрядной версии Windows
description: Ключевой целью 64-разрядной версии Windows является упрощение разработчиков использовать единую базу исходного кода для своих 32-и 64-разрядных приложений.
ms.assetid: 62101e20-13bb-46d5-9542-2afd414ad224
keywords:
- 64-разрядное руководство по программированию Windows 64-разрядное программирование для Windows, подготовка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b585f2798650f84930e6aa2e5d6e19cb9aa5e8e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413464"
---
# <a name="getting-ready-for-64-bit-windows"></a><span data-ttu-id="f6a53-104">Подготовка к 64-разрядной версии Windows</span><span class="sxs-lookup"><span data-stu-id="f6a53-104">Getting Ready for 64-bit Windows</span></span>

<span data-ttu-id="f6a53-105">Ключевой целью 64-разрядной версии Windows является упрощение разработчиков использовать единую базу исходного кода для своих 32-и 64-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="f6a53-105">A key goal of the 64-bit version of Windows is to make it easy for developers to use a single source-code base for their 32-bit and 64-bit applications.</span></span> <span data-ttu-id="f6a53-106">В этом обзоре описывается, как сделать исходный код поддерживать как 32-разрядные, так и 64-разрядные вычисления.</span><span class="sxs-lookup"><span data-stu-id="f6a53-106">This overview describes how to make your source code support both 32-bit and 64-bit computing.</span></span> <span data-ttu-id="f6a53-107">Это поможет вам ознакомиться с существующими [типами данных Windows](/windows/desktop/WinProg/windows-data-types) .</span><span class="sxs-lookup"><span data-stu-id="f6a53-107">Familiarity with existing [Windows data types](/windows/desktop/WinProg/windows-data-types) will help.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f6a53-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="f6a53-108">In this Section</span></span>

-   [<span data-ttu-id="f6a53-109">Абстрактные модели данных</span><span class="sxs-lookup"><span data-stu-id="f6a53-109">Abstract Data Models</span></span>](abstract-data-models.md)
-   [<span data-ttu-id="f6a53-110">Новые типы данных</span><span class="sxs-lookup"><span data-stu-id="f6a53-110">The New Data Types</span></span>](the-new-data-types.md)
-   [<span data-ttu-id="f6a53-111">Среда</span><span class="sxs-lookup"><span data-stu-id="f6a53-111">The Environment</span></span>](the-environment.md)
-   [<span data-ttu-id="f6a53-112">Средства</span><span class="sxs-lookup"><span data-stu-id="f6a53-112">The Tools</span></span>](the-tools.md)
-   [<span data-ttu-id="f6a53-113">Правила использования указателей</span><span class="sxs-lookup"><span data-stu-id="f6a53-113">Rules for Using Pointers</span></span>](rules-for-using-pointers.md)
-   [<span data-ttu-id="f6a53-114">Виртуальное адресное пространство</span><span class="sxs-lookup"><span data-stu-id="f6a53-114">Virtual Address Space</span></span>](virtual-address-space.md)
-   [<span data-ttu-id="f6a53-115">Ошибки выравнивания</span><span class="sxs-lookup"><span data-stu-id="f6a53-115">Alignment Faults</span></span>](fault-alignments.md)
-   [<span data-ttu-id="f6a53-116">Взаимодействие процессов</span><span class="sxs-lookup"><span data-stu-id="f6a53-116">Process Interoperability</span></span>](process-interoperability.md)
-   [<span data-ttu-id="f6a53-117">Поставщиков</span><span class="sxs-lookup"><span data-stu-id="f6a53-117">Drivers</span></span>](drivers.md)

 

 