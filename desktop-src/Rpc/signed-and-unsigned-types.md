---
title: Подписанные и неподписанные типы (RPC)
description: Компиляторы, использующие разные значения по умолчанию для подписанных и неподписанных типов, могут вызвать ошибки программного обеспечения в распределенном приложении.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453d45d0a4c29a2e30449fb645e6f40338eac546
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103891349"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="2a886-103">Подписанные и неподписанные типы (RPC)</span><span class="sxs-lookup"><span data-stu-id="2a886-103">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="2a886-104">Компиляторы, использующие разные значения по умолчанию для подписанных и неподписанных типов, могут вызвать ошибки программного обеспечения в распределенном приложении.</span><span class="sxs-lookup"><span data-stu-id="2a886-104">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="2a886-105">Эти проблемы можно избежать, явно объявляя типы символов как **подписанные** или **неподписанные**.</span><span class="sxs-lookup"><span data-stu-id="2a886-105">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="2a886-106">MIDL определяет [**небольшой**](/windows/desktop/Midl/small) тип, чтобы использовать тот же знак по умолчанию, что и тип **char** в целевом компиляторе C.</span><span class="sxs-lookup"><span data-stu-id="2a886-106">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="2a886-107">Если компилятор предполагает, что **char** не имеет знака, то **Small** также будет определяться как неподписанный.</span><span class="sxs-lookup"><span data-stu-id="2a886-107">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="2a886-108">Многие компиляторы C позволяют изменить значение по умолчанию в качестве параметра командной строки.</span><span class="sxs-lookup"><span data-stu-id="2a886-108">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="2a886-109">Например, параметр командной строки Microsoft C Compiler **/j** изменяет **знак символа по умолчанию с Sign** на неподписанный.</span><span class="sxs-lookup"><span data-stu-id="2a886-109">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="2a886-110">Кроме того, можно управлять знаком переменных типа **char** и **Small** с помощью параметра командной строки компилятора MIDL [**/char**](/windows/desktop/Midl/-char).</span><span class="sxs-lookup"><span data-stu-id="2a886-110">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="2a886-111">Этот параметр позволяет указать знак по умолчанию, используемый компилятором.</span><span class="sxs-lookup"><span data-stu-id="2a886-111">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="2a886-112">Компилятор MIDL явным образом объявляет знак всех типов **char** , которые не соответствуют типу по умолчанию C-Compiler в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="2a886-112">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
