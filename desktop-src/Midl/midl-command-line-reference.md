---
title: Справочник по MIDL Command-Line
description: В этом разделе содержатся справочные сведения по каждому параметру командной строки и переключателю, распознаваемым компилятором Microsoft RPC MIDL.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Язык MIDL MIDL, Справочник
- Справочник по командной строке MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105662001"
---
# <a name="midl-command-line-reference"></a><span data-ttu-id="7a909-105">Справочник по MIDL Command-Line</span><span class="sxs-lookup"><span data-stu-id="7a909-105">MIDL Command-Line Reference</span></span>

<span data-ttu-id="7a909-106">В этом разделе содержатся справочные сведения по каждому параметру командной строки и переключателю, распознаваемым компилятором Microsoft RPC MIDL.</span><span class="sxs-lookup"><span data-stu-id="7a909-106">This section contains reference information for each command-line switch and switch option recognized by the Microsoft RPC MIDL compiler.</span></span> <span data-ttu-id="7a909-107">Записи переключателей упорядочены в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="7a909-107">Switch entries are arranged in alphabetical order.</span></span> <span data-ttu-id="7a909-108">[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md) описывает общий синтаксис командной строки.</span><span class="sxs-lookup"><span data-stu-id="7a909-108">[General MIDL Command-line Syntax](general-midl-command-line-syntax.md) describes the general command-line syntax.</span></span>

<dl>

[<span data-ttu-id="7a909-109">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="7a909-109">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)  
[<span data-ttu-id="7a909-110">Команда файла ответа</span><span class="sxs-lookup"><span data-stu-id="7a909-110">The Response File Command</span></span>](the-response-file-command.md)  
[<span data-ttu-id="7a909-111">**/акф**</span><span class="sxs-lookup"><span data-stu-id="7a909-111">**/acf**</span></span>](-acf.md)  
[<span data-ttu-id="7a909-112">**/align**</span><span class="sxs-lookup"><span data-stu-id="7a909-112">**/align**</span></span>](-align.md)  
[<span data-ttu-id="7a909-113">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="7a909-113">**/amd64**</span></span>](-amd64.md)  
[<span data-ttu-id="7a909-114">**\_Конфигурация/АПП**</span><span class="sxs-lookup"><span data-stu-id="7a909-114">**/app\_config**</span></span>](-app-config.md)  
[<span data-ttu-id="7a909-115">совместимость с/бакквард \_</span><span class="sxs-lookup"><span data-stu-id="7a909-115">/backward\_compat</span></span>](-backward-compat.md)  
[<span data-ttu-id="7a909-116">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="7a909-116">**/c\_ext**</span></span>](-c-ext.md)  
[<span data-ttu-id="7a909-117">**/каукс**</span><span class="sxs-lookup"><span data-stu-id="7a909-117">**/caux**</span></span>](-caux.md)  
[<span data-ttu-id="7a909-118">**/Char**</span><span class="sxs-lookup"><span data-stu-id="7a909-118">**/char**</span></span>](-char.md)  
[<span data-ttu-id="7a909-119">**/Client**</span><span class="sxs-lookup"><span data-stu-id="7a909-119">**/client**</span></span>](-client.md)  
[<span data-ttu-id="7a909-120">**/конфирм**</span><span class="sxs-lookup"><span data-stu-id="7a909-120">**/confirm**</span></span>](-confirm.md)  
[<span data-ttu-id="7a909-121">**/КПП \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="7a909-121">**/cpp\_cmd**</span></span>](-cpp-cmd.md)  
[<span data-ttu-id="7a909-122">**/КПП \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="7a909-122">**/cpp\_opt**</span></span>](-cpp-opt.md)  
<span data-ttu-id="7a909-123">[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)</span><span class="sxs-lookup"><span data-stu-id="7a909-123">[**/cstruct_out**](-cstruct-out.md)
[**/cstub**](-cstub.md)</span></span>  
[<span data-ttu-id="7a909-124">**/D**</span><span class="sxs-lookup"><span data-stu-id="7a909-124">**/D**</span></span>](-d.md)  
[<span data-ttu-id="7a909-125">**/dlldata**</span><span class="sxs-lookup"><span data-stu-id="7a909-125">**/dlldata**</span></span>](-dlldata.md)  
[<span data-ttu-id="7a909-126">**/env**</span><span class="sxs-lookup"><span data-stu-id="7a909-126">**/env**</span></span>](-env.md)  
[<span data-ttu-id="7a909-127">**/Error**</span><span class="sxs-lookup"><span data-stu-id="7a909-127">**/error**</span></span>](-error.md)  
[<span data-ttu-id="7a909-128">**/Error**</span><span class="sxs-lookup"><span data-stu-id="7a909-128">**/error**</span></span>](-error.md)  
[<span data-ttu-id="7a909-129">**/h**</span><span class="sxs-lookup"><span data-stu-id="7a909-129">**/h**</span></span>](-h.md)  
[<span data-ttu-id="7a909-130">**/Header**</span><span class="sxs-lookup"><span data-stu-id="7a909-130">**/header**</span></span>](-header.md)  
[<span data-ttu-id="7a909-131">**/Help (/?)**</span><span class="sxs-lookup"><span data-stu-id="7a909-131">**/help (/?)**</span></span>](-help-.md)  
[<span data-ttu-id="7a909-132">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="7a909-132">**/ia64**</span></span>](-ia64.md)  
[<span data-ttu-id="7a909-133">**/I**</span><span class="sxs-lookup"><span data-stu-id="7a909-133">**/I**</span></span>](-i.md)  
[<span data-ttu-id="7a909-134">**/IID**</span><span class="sxs-lookup"><span data-stu-id="7a909-134">**/iid**</span></span>](-iid.md)  
[<span data-ttu-id="7a909-135">**/Import**</span><span class="sxs-lookup"><span data-stu-id="7a909-135">**/import**</span></span>](-import.md)  
[<span data-ttu-id="7a909-136">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="7a909-136">**/lcid**</span></span>](-lcid.md)  
[<span data-ttu-id="7a909-137">**/mktyplib203**</span><span class="sxs-lookup"><span data-stu-id="7a909-137">**/mktyplib203**</span></span>](-mktyplib203.md)  
[<span data-ttu-id="7a909-138">**/МС \_ ext**</span><span class="sxs-lookup"><span data-stu-id="7a909-138">**/ms\_ext**</span></span>](-ms-ext.md)  
[<span data-ttu-id="7a909-139">**\_объединение/МС**</span><span class="sxs-lookup"><span data-stu-id="7a909-139">**/ms\_union**</span></span>](-ms-union.md)  
[<span data-ttu-id="7a909-140">**/МСК \_ ver**</span><span class="sxs-lookup"><span data-stu-id="7a909-140">**/msc\_ver**</span></span>](-msc-ver.md)  
[<span data-ttu-id="7a909-141">**/New**</span><span class="sxs-lookup"><span data-stu-id="7a909-141">**/new**</span></span>](-new.md)  
[<span data-ttu-id="7a909-142">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="7a909-142">**/newtlb**</span></span>](-newtlb.md)  
[<span data-ttu-id="7a909-143">**/но \_ cpp,/нокпп**</span><span class="sxs-lookup"><span data-stu-id="7a909-143">**/no\_cpp, /nocpp**</span></span>](-no-cpp-nocpp.md)  
[<span data-ttu-id="7a909-144">**/но \_ по умолчанию \_ ЕПВ**</span><span class="sxs-lookup"><span data-stu-id="7a909-144">**/no\_default\_epv**</span></span>](-no-default-epv.md)  
[<span data-ttu-id="7a909-145">**\_идир/но DEF \_**</span><span class="sxs-lookup"><span data-stu-id="7a909-145">**/no\_def\_idir**</span></span>](-no-def-idir.md)  
[<span data-ttu-id="7a909-146">**/но в \_ формате \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="7a909-146">**/no\_format\_opt**</span></span>](-no-format-opt.md)  
[<span data-ttu-id="7a909-147">**/но \_ надежность**</span><span class="sxs-lookup"><span data-stu-id="7a909-147">**/no\_robust**</span></span>](-no-robust.md)  
[<span data-ttu-id="7a909-148">**\_предупреждение/но**</span><span class="sxs-lookup"><span data-stu-id="7a909-148">**/no\_warn**</span></span>](-no-warn.md)  
[<span data-ttu-id="7a909-149">**/nologo**</span><span class="sxs-lookup"><span data-stu-id="7a909-149">**/nologo**</span></span>](-nologo.md)  
[<span data-ttu-id="7a909-150">**/notlb**</span><span class="sxs-lookup"><span data-stu-id="7a909-150">**/notlb**</span></span>](-notlb.md)  
[<span data-ttu-id="7a909-151">**/o**</span><span class="sxs-lookup"><span data-stu-id="7a909-151">**/o**</span></span>](-o.md)  
[<span data-ttu-id="7a909-152">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="7a909-152">**/Oi**</span></span>](-oi.md)  
[<span data-ttu-id="7a909-153">**/Old**</span><span class="sxs-lookup"><span data-stu-id="7a909-153">**/old**</span></span>](-old.md)  
[<span data-ttu-id="7a909-154">**/oldtlb**</span><span class="sxs-lookup"><span data-stu-id="7a909-154">**/oldtlb**</span></span>](-oldtlb.md)  
[<span data-ttu-id="7a909-155">**/oldnames**</span><span class="sxs-lookup"><span data-stu-id="7a909-155">**/oldnames**</span></span>](-oldnames.md)  
[<span data-ttu-id="7a909-156">**/OS**</span><span class="sxs-lookup"><span data-stu-id="7a909-156">**/Os**</span></span>](-os.md)  
[<span data-ttu-id="7a909-157">**/осф**</span><span class="sxs-lookup"><span data-stu-id="7a909-157">**/osf**</span></span>](-osf.md)  
[<span data-ttu-id="7a909-158">**/out**</span><span class="sxs-lookup"><span data-stu-id="7a909-158">**/out**</span></span>](-out.md)  
[<span data-ttu-id="7a909-159">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="7a909-159">**/pack**</span></span>](-pack.md)  
[<span data-ttu-id="7a909-160">**/префикс**</span><span class="sxs-lookup"><span data-stu-id="7a909-160">**/prefix**</span></span>](-prefix.md)  
[<span data-ttu-id="7a909-161">**/протокол**</span><span class="sxs-lookup"><span data-stu-id="7a909-161">**/protocol**</span></span>](-protocol.md)  
[<span data-ttu-id="7a909-162">**/Proxy**</span><span class="sxs-lookup"><span data-stu-id="7a909-162">**/proxy**</span></span>](-proxy.md)  
[<span data-ttu-id="7a909-163">**/robust**</span><span class="sxs-lookup"><span data-stu-id="7a909-163">**/robust**</span></span>](-robust.md)  
[<span data-ttu-id="7a909-164">**/рпксс**</span><span class="sxs-lookup"><span data-stu-id="7a909-164">**/rpcss**</span></span>](-rpcss.md)  
[<span data-ttu-id="7a909-165">**/сал**</span><span class="sxs-lookup"><span data-stu-id="7a909-165">**/sal**</span></span>](-sal.md)  
[<span data-ttu-id="7a909-166">**/Сал \_ локальный**</span><span class="sxs-lookup"><span data-stu-id="7a909-166">**/sal\_local**</span></span>](-sal-local.md)  
[<span data-ttu-id="7a909-167">**/саукс**</span><span class="sxs-lookup"><span data-stu-id="7a909-167">**/saux**</span></span>](-saux.md)  
[<span data-ttu-id="7a909-168">**/савепп**</span><span class="sxs-lookup"><span data-stu-id="7a909-168">**/savePP**</span></span>](-savepp.md)  
[<span data-ttu-id="7a909-169">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="7a909-169">**/sstub**</span></span>](-sstub.md)  
[<span data-ttu-id="7a909-170">**\_Проверка/синтакс**</span><span class="sxs-lookup"><span data-stu-id="7a909-170">**/syntax\_check**</span></span>](-syntax-check.md)  
[**/<system>**](-system-.md)  
[<span data-ttu-id="7a909-171">**/Target**</span><span class="sxs-lookup"><span data-stu-id="7a909-171">**/target**</span></span>](-target.md)  
[<span data-ttu-id="7a909-172">**/TLB**</span><span class="sxs-lookup"><span data-stu-id="7a909-172">**/tlb**</span></span>](-tlb.md)  
[<span data-ttu-id="7a909-173">**/U**</span><span class="sxs-lookup"><span data-stu-id="7a909-173">**/U**</span></span>](-u.md)  
[<span data-ttu-id="7a909-174">**/TestCleanup используется \_ ЕПВ**</span><span class="sxs-lookup"><span data-stu-id="7a909-174">**/use\_epv**</span></span>](-use-epv.md)  
[<span data-ttu-id="7a909-175">**\_Метка/Version**</span><span class="sxs-lookup"><span data-stu-id="7a909-175">**/version\_stamp**</span></span>](-version-stamp.md)  
[<span data-ttu-id="7a909-176">**/W**</span><span class="sxs-lookup"><span data-stu-id="7a909-176">**/W**</span></span>](-w.md)  
[<span data-ttu-id="7a909-177">**/warn**</span><span class="sxs-lookup"><span data-stu-id="7a909-177">**/warn**</span></span>](-warn.md)  
[<span data-ttu-id="7a909-178">**/win32**</span><span class="sxs-lookup"><span data-stu-id="7a909-178">**/win32**</span></span>](-win32.md)  
[<span data-ttu-id="7a909-179">**/win64**</span><span class="sxs-lookup"><span data-stu-id="7a909-179">**/win64**</span></span>](-win64.md)  
[<span data-ttu-id="7a909-180">**/WX**</span><span class="sxs-lookup"><span data-stu-id="7a909-180">**/WX**</span></span>](-wx.md)  
[<span data-ttu-id="7a909-181">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="7a909-181">**/Zp**</span></span>](-zp.md)  
[<span data-ttu-id="7a909-182">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="7a909-182">**/Zs**</span></span>](-zs.md)  
</dl>

<span data-ttu-id="7a909-183">Компилятор MIDL может создавать код для различных платформ и системных выпусков.</span><span class="sxs-lookup"><span data-stu-id="7a909-183">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="7a909-184">Дополнительные сведения о предлагаемых параметрах и способах создания кода, оптимизированного для конкретного выпуска, см. в параметре [**/Target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="7a909-184">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a given release.</span></span>

<span data-ttu-id="7a909-185">Обратите внимание, что знак минус (–) может быть заменен на косую черту (/) во всех параметрах командной строки MIDL, начинающихся с косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="7a909-185">Note that the minus sign (–) may be substituted for the slash (/) in all MIDL command-line switches that begin with a slash (/).</span></span> <span data-ttu-id="7a909-186">В следующем примере демонстрируется их эквивалентность при вызове компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="7a909-186">The following example demonstrates their equivalence when invoking the MIDL compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="7a909-187">Примеры</span><span class="sxs-lookup"><span data-stu-id="7a909-187">Examples</span></span>

<span data-ttu-id="7a909-188">**MIDL/АКФ My \_ ACF. ACF** *имя_файла \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="7a909-188">**midl /acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

<span data-ttu-id="7a909-189">**MIDL-ACF My \_ ACF. ACF** *имя_файла \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="7a909-189">**midl -acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

 

 




