---
title: Подписанные и неподписанные типы (MIDL)
description: Сведения о подписанных и неподписанных типах в MIDL. Компиляторы, использующие различные типы значений по умолчанию, могут вызывать ошибки программного обеспечения в распределенном приложении.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- типы данных MIDL, со знаком и без знака
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407387"
---
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="ca554-105">Подписанные и неподписанные типы (MIDL)</span><span class="sxs-lookup"><span data-stu-id="ca554-105">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="ca554-106">Компиляторы, использующие разные значения по умолчанию для подписанных и неподписанных типов, могут вызвать ошибки программного обеспечения в распределенном приложении.</span><span class="sxs-lookup"><span data-stu-id="ca554-106">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="ca554-107">Эти проблемы можно избежать, явно объявляя типы символов как подписанные или неподписанные.</span><span class="sxs-lookup"><span data-stu-id="ca554-107">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="ca554-108">Обратите внимание, что компиляторы устройства DCE не распознают ключевое слово [**со знаком**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="ca554-108">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="ca554-109">Поэтому эта функция недоступна при использовании параметра компилятора MIDL/**Использование** .</span><span class="sxs-lookup"><span data-stu-id="ca554-109">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="ca554-110">MIDL определяет [**небольшой**](small.md) тип, чтобы использовать тот же знак по умолчанию, что и тип [**char**](char-idl.md) в целевом компиляторе C.</span><span class="sxs-lookup"><span data-stu-id="ca554-110">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="ca554-111">Если компилятор предполагает, что **char** не имеет знака, то **Small** также будет определяться как неподписанный.</span><span class="sxs-lookup"><span data-stu-id="ca554-111">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="ca554-112">Многие компиляторы C позволяют изменить значение по умолчанию в качестве параметра командной строки.</span><span class="sxs-lookup"><span data-stu-id="ca554-112">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="ca554-113">Например, в среде разработки Microsoft Visual C++ параметр командной строки **/j** изменяет знак **символа** по умолчанию с Sign на неподписанный.</span><span class="sxs-lookup"><span data-stu-id="ca554-113">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="ca554-114">Кроме того, можно управлять знаком переменных типа [**char**](char-idl.md) и [**Small**](small.md) с помощью параметра командной строки компилятора MIDL [**/char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="ca554-114">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="ca554-115">Этот параметр позволяет указать знак по умолчанию, используемый компилятором.</span><span class="sxs-lookup"><span data-stu-id="ca554-115">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="ca554-116">Компилятор MIDL явным образом объявляет знак всех типов **char** , которые не соответствуют типу по умолчанию C-Compiler в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="ca554-116">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




