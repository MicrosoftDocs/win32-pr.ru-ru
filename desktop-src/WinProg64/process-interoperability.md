---
title: Взаимодействие процессов
description: Приложения на основе Win32 можно запускать в 64-разрядной системе Windows с помощью слоя эмуляции. Windows 10 в ARM включает слой эмуляции x86-on-ARM64. Дополнительные сведения см. в разделе Выполнение 32-разрядных приложений.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- взаимодействие процессов с 64-разрядным программированием для Windows
- совместимость с 64-разрядным программированием Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700589"
---
# <a name="process-interoperability"></a><span data-ttu-id="84b06-107">Взаимодействие процессов</span><span class="sxs-lookup"><span data-stu-id="84b06-107">Process Interoperability</span></span>

<span data-ttu-id="84b06-108">Приложения на основе Win32 можно запускать в 64-разрядной системе Windows с помощью слоя эмуляции.</span><span class="sxs-lookup"><span data-stu-id="84b06-108">You can run Win32-based applications on 64-bit Windows using an emulation layer.</span></span> <span data-ttu-id="84b06-109">Windows 10 в ARM включает слой эмуляции x86-on-ARM64.</span><span class="sxs-lookup"><span data-stu-id="84b06-109">Windows 10 on ARM includes an x86-on-ARM64 emulation layer.</span></span> <span data-ttu-id="84b06-110">Дополнительные сведения см. в разделе [выполнение 32-разрядных приложений](running-32-bit-applications.md).</span><span class="sxs-lookup"><span data-stu-id="84b06-110">For more information, see [Running 32-bit Applications](running-32-bit-applications.md).</span></span>

<span data-ttu-id="84b06-111">В 64-разрядной системе Windows 64-разрядный процесс не может загрузить 32-разрядную библиотеку динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="84b06-111">On 64-bit Windows, a 64-bit process cannot load a 32-bit dynamic-link library (DLL).</span></span> <span data-ttu-id="84b06-112">Кроме того, 32-разрядный процесс не может загрузить 64-разрядную библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="84b06-112">Additionally, a 32-bit process cannot load a 64-bit DLL.</span></span> <span data-ttu-id="84b06-113">Однако 64-разрядная версия Windows поддерживает удаленные вызовы процедур (RPC) между 64-и 32-разрядными процессами (как на одном компьютере, так и на нескольких компьютерах).</span><span class="sxs-lookup"><span data-stu-id="84b06-113">However, 64-bit Windows supports remote procedure calls (RPC) between 64-bit and 32-bit processes (both on the same computer and across computers).</span></span> <span data-ttu-id="84b06-114">В 64-разрядной системе Windows сервер стороннего 32-разрядного COM-сервера может взаимодействовать с 64-разрядным клиентом, а необработанный 64-разрядный сервер COM может взаимодействовать с 32-битным клиентом.</span><span class="sxs-lookup"><span data-stu-id="84b06-114">On 64-bit Windows, an out-of-process 32-bit COM server can communicate with a 64-bit client, and an out-of-process 64-bit COM server can communicate with a 32-bit client.</span></span> <span data-ttu-id="84b06-115">Поэтому при наличии 32-разрядной библиотеки DLL, которая не поддерживает модель COM, ее можно заключить в внутрипроцессный сервер COM и использовать COM для маршалирования вызовов и из 64-разрядного процесса.</span><span class="sxs-lookup"><span data-stu-id="84b06-115">Therefore, if you have a 32-bit DLL that is not COM-aware, you can wrap it in an out-of-process COM server and use COM to marshal calls to and from a 64-bit process.</span></span>

<span data-ttu-id="84b06-116">Внутрипроцессный сервер в настоящее время зарегистрирован с помощью записи реестра **инпроксервер** .</span><span class="sxs-lookup"><span data-stu-id="84b06-116">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="84b06-117">На 64-разрядных серверах под управлением Windows, 64 и 32-bit должны использовать запись **InprocServer32** .</span><span class="sxs-lookup"><span data-stu-id="84b06-117">On 64-bit Windows, 64- and 32-bit in-process servers should use the **InprocServer32** entry.</span></span>

<span data-ttu-id="84b06-118">Для дескрипторов портов, которые по своей природе являются локальными для компьютера и никогда не будут использоваться между 32-разрядной и 64-разрядной границей, используйте тип **\_ ptr дескриптора** вместо типа данных **int \_ ptr** или **DWORD \_** .</span><span class="sxs-lookup"><span data-stu-id="84b06-118">To port handles, which by their nature are local to the computer and would never be used across the 32-bit to 64-bit boundary, use the **HANDLE\_PTR** type instead of the **INT\_PTR** or **DWORD\_PTR** type.</span></span> <span data-ttu-id="84b06-119">Это включает в себя перенос интерфейсов RPC, передающих такие дескрипторы как значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="84b06-119">This includes porting RPC interfaces passing such handles as **DWORD** values.</span></span> <span data-ttu-id="84b06-120">64-разрядный **маркер \_** имеет значение 64 бит на канале передачи (не усекается) и поэтому не требует сопоставления.</span><span class="sxs-lookup"><span data-stu-id="84b06-120">The 64-bit **HANDLE\_PTR** is 64 bits on the wire (not truncated) and thus does not need mapping.</span></span> <span data-ttu-id="84b06-121">(32-разрядный **маркер \_** имеет значение 32 бит на канале передачи.)</span><span class="sxs-lookup"><span data-stu-id="84b06-121">(The 32-bit **HANDLE\_PTR** is 32 bits on the wire.)</span></span>

<span data-ttu-id="84b06-122">Дополнительные сведения см. в разделе [Разработка интерфейсов, совместимых с 64-bit](designing-64-bit-compatible-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="84b06-122">For more information, see [Designing 64-bit-Compatible Interfaces](designing-64-bit-compatible-interfaces.md).</span></span>

 

 




