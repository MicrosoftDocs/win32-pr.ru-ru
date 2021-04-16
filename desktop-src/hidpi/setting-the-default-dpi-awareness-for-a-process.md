---
description: Дополнительные сведения см. в статье Настройка отслеживания количества точек на дюйм по умолчанию для процесса.
title: Настройка отслеживания DPI по умолчанию для процесса (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: ff869974e6d9aa2eec2b3251832c061d7b6826da
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720822"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="9aa03-103">Настройка отслеживания количества точек на дюйм по умолчанию для процесса</span><span class="sxs-lookup"><span data-stu-id="9aa03-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="9aa03-104">Классические приложения в Windows могут работать в разных режимах определения DPI.</span><span class="sxs-lookup"><span data-stu-id="9aa03-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="9aa03-105">Эти режимы позволяют разрешать различные способы масштабирования DPI и могут использовать разные пространства координат.</span><span class="sxs-lookup"><span data-stu-id="9aa03-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="9aa03-106">Дополнительные сведения о поддержке DPI см. в разделе [Разработка приложений с высоким разрешением в Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="9aa03-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="9aa03-107">Важно явно задать режим поддержки DPI по умолчанию для процесса, чтобы избежать непредвиденного поведения.</span><span class="sxs-lookup"><span data-stu-id="9aa03-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="9aa03-108">Существует два основных метода указания сведений о DPI по умолчанию для процесса:</span><span class="sxs-lookup"><span data-stu-id="9aa03-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="9aa03-109">1 \) через параметр манифеста приложения</span><span class="sxs-lookup"><span data-stu-id="9aa03-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="9aa03-110">2 \) программным путем через вызов API</span><span class="sxs-lookup"><span data-stu-id="9aa03-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="9aa03-111">Рекомендуется указывать сведения о соответствии процесса по умолчанию для процессов с помощью параметра манифеста.</span><span class="sxs-lookup"><span data-stu-id="9aa03-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="9aa03-112">При указании интерфейса API по умолчанию поддержка не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9aa03-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="9aa03-113">Настройка осведомленности по умолчанию в манифесте приложения</span><span class="sxs-lookup"><span data-stu-id="9aa03-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="9aa03-114">Существует два параметра манифеста, которые позволяют указать режим поддержки по умолчанию для отслеживания количества точек на дюйм: \<dpiAwareness\> и \<dpiAware\> .</span><span class="sxs-lookup"><span data-stu-id="9aa03-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="9aa03-115">\<dpiAware\> была введена в Windows Vista и позволяет установить для процесса по умолчанию только сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="9aa03-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="9aa03-116">\<dpiAwareness\> был введен в Windows 10 версии 1607 и позволяет указать упорядоченный список режимов по умолчанию для отслеживания количества точек на дюйм.</span><span class="sxs-lookup"><span data-stu-id="9aa03-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="9aa03-117">Это позволяет задать режимы определения количества точек на дюйм для резервного копирования, которые будут использоваться, если приложение запущено в версии Windows не может поддерживать первый режим службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="9aa03-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="9aa03-118">В более старых версиях Windows новый \<dpiAwareness\> тег будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="9aa03-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="9aa03-119">Это означает, что можно использовать оба этих параметра манифеста, чтобы включить сценарий, в котором по умолчанию для процесса может быть включена поддержка системы в более старой версии Windows при Per-Monitor в версиях, превышающих Windows 10, версия 1607.</span><span class="sxs-lookup"><span data-stu-id="9aa03-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="9aa03-120">В Windows 10 версии 1607 и в \<dpiAware\> параметр не учитывается, если \<dpiAwareness\> элемент имеется в наличии.</span><span class="sxs-lookup"><span data-stu-id="9aa03-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="9aa03-121">В следующей таблице показано, как задать различные режимы поддержки DPI по умолчанию для процессов с помощью двух параметров манифеста:</span><span class="sxs-lookup"><span data-stu-id="9aa03-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9aa03-122">Обработка режима поддержки DPI по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9aa03-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="9aa03-123">&lt;&gt;параметр дпиаваре</span><span class="sxs-lookup"><span data-stu-id="9aa03-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="9aa03-124">&lt;&gt;параметр дпиаваренесс (Windows 10, версия 1607 и более поздние)</span><span class="sxs-lookup"><span data-stu-id="9aa03-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9aa03-125">связан</span><span class="sxs-lookup"><span data-stu-id="9aa03-125">unaware</span></span></td>
<td><p><span data-ttu-id="9aa03-126">Н/д (нет параметра Дпиаваре в манифесте)</span><span class="sxs-lookup"><span data-stu-id="9aa03-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="9aa03-127">или</span><span class="sxs-lookup"><span data-stu-id="9aa03-127">or</span></span></p>
<p><span data-ttu-id="9aa03-128">&lt;Дпиаваре &gt; false &lt; /дпиаваре&gt;</span><span class="sxs-lookup"><span data-stu-id="9aa03-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="9aa03-129">&lt;Дпиаваренесс &gt; &lt; /дпиаваренесс&gt;</span><span class="sxs-lookup"><span data-stu-id="9aa03-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9aa03-130">С учетом системы</span><span class="sxs-lookup"><span data-stu-id="9aa03-130">System aware</span></span></td>
<td><span data-ttu-id="9aa03-131">&lt;Дпиаваре &gt; Истина &lt; /дпиаваре&gt;</span><span class="sxs-lookup"><span data-stu-id="9aa03-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="9aa03-132">&lt;Дпиаваренесс &gt; System &lt; /дпиаваренесс&gt;</span><span class="sxs-lookup"><span data-stu-id="9aa03-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9aa03-133">На монитор</span><span class="sxs-lookup"><span data-stu-id="9aa03-133">Per Monitor</span></span></td>
<td><span data-ttu-id="9aa03-134">&lt;Дпиаваре &gt; true/PM &lt; дпиаваре&gt;</span><span class="sxs-lookup"><span data-stu-id="9aa03-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="9aa03-135">&lt;Дпиаваренесс &gt; пермонитор &lt; /дпиаваренесс&gt;</span><span class="sxs-lookup"><span data-stu-id="9aa03-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9aa03-136">На монитор версии 2</span><span class="sxs-lookup"><span data-stu-id="9aa03-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="9aa03-137">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9aa03-137">Not supported</span></span></td>
<td><span data-ttu-id="9aa03-138">&lt;Дпиаваренесс &gt; PerMonitorV2 &lt; /дпиаваренесс&gt;</span><span class="sxs-lookup"><span data-stu-id="9aa03-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9aa03-139">В приведенном ниже примере показаны \<dpiAwareness\> Параметры и, используемые в одном и том \<dpiAware\> же файле манифеста, для настройки поведения процесса по умолчанию для отслеживания dpi для различных версий Windows.</span><span class="sxs-lookup"><span data-stu-id="9aa03-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
  <asmv3:application>
    <asmv3:windowsSettings>
      <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
      <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="9aa03-140">Программное задание осведомленности по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9aa03-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="9aa03-141">Хотя это и не рекомендуется, по умолчанию можно задать отслеживание количества точек на дюйм программным способом.</span><span class="sxs-lookup"><span data-stu-id="9aa03-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="9aa03-142">После создания окна (HWND) в процессе изменение режима поддержки DPI больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9aa03-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="9aa03-143">Если вы устанавливаете режим поддержки по умолчанию для обработки точек на дюйм как программно, необходимо вызвать соответствующий API перед созданием дескрипторов HWND.</span><span class="sxs-lookup"><span data-stu-id="9aa03-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="9aa03-144">Существует несколько интерфейсов API, которые позволяют указать для процесса сведения о DPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9aa03-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="9aa03-145">Текущий рекомендуемый API — [**сетпроцессдпиаваренессконтекст**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), так как более старые API предлагают меньше функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="9aa03-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9aa03-146">API</span><span class="sxs-lookup"><span data-stu-id="9aa03-146">API</span></span></th>
<th><span data-ttu-id="9aa03-147">Минимальная версия Windows</span><span class="sxs-lookup"><span data-stu-id="9aa03-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="9aa03-148">Неосведомленность DPI</span><span class="sxs-lookup"><span data-stu-id="9aa03-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="9aa03-149">Учитывать DPI системы</span><span class="sxs-lookup"><span data-stu-id="9aa03-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="9aa03-150">На уровне DPI для каждого монитора</span><span class="sxs-lookup"><span data-stu-id="9aa03-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9aa03-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">сетпроцессдпиаваре</a></span><span class="sxs-lookup"><span data-stu-id="9aa03-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span></span></td>
<td><span data-ttu-id="9aa03-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9aa03-152">Windows Vista</span></span></td>
<td><span data-ttu-id="9aa03-153">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9aa03-153">N/A</span></span></td>
<td><span data-ttu-id="9aa03-154">Сетпроцессдпиаваре ()</span><span class="sxs-lookup"><span data-stu-id="9aa03-154">SetProcessDpiAware()</span></span></td>
<td><span data-ttu-id="9aa03-155">Н/Д</span><span class="sxs-lookup"><span data-stu-id="9aa03-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9aa03-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>сетпроцессдпиаваренесс</strong></a></span><span class="sxs-lookup"><span data-stu-id="9aa03-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="9aa03-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9aa03-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="9aa03-158">Сетпроцессдпиаваренесс (PROCESS_DPI_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="9aa03-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="9aa03-159">Сетпроцессдпиаваренесс (PROCESS_DPI_SYSTEM_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="9aa03-159">SetProcessDpiAwareness(PROCESS_DPI_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="9aa03-160">Сетпроцессдпиаваренесс (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="9aa03-160">SetProcessDpiAwareness(PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9aa03-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>сетпроцессдпиаваренессконтекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="9aa03-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="9aa03-162">Windows 10, версия 1607</span><span class="sxs-lookup"><span data-stu-id="9aa03-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="9aa03-163">Сетпроцессдпиаваренессконтекст (DPI_AWARENESS_CONTEXT_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="9aa03-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="9aa03-164">Сетпроцессдпиаваренессконтекст (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span><span class="sxs-lookup"><span data-stu-id="9aa03-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="9aa03-165">Сетпроцессдпиаваренессконтекст (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span><span class="sxs-lookup"><span data-stu-id="9aa03-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="9aa03-166">Сетпроцессдпиаваренессконтекст (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span><span class="sxs-lookup"><span data-stu-id="9aa03-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="9aa03-167">Процесс-по умолчанию и поток по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9aa03-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="9aa03-168">В этом документе описывается установка по умолчанию для процесса отслеживания DPI.</span><span class="sxs-lookup"><span data-stu-id="9aa03-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="9aa03-169">Это обусловлено тем, что в Windows 10 появилась поддержка использования более одного режима поддержки точек на дюйм в одном процессе (до Windows 10, весь процесс должен соответствовать режиму поддержки одного DPI).</span><span class="sxs-lookup"><span data-stu-id="9aa03-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="9aa03-170">Поддержка выполнения более одного режима поддержки DPI в рамках процесса называется масштабированием DPI в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="9aa03-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="9aa03-171">При использовании масштабирования DPI в смешанном режиме в пределах процесса каждое окно верхнего уровня может работать в режиме поддержки DPI, который может отличаться от значения по умолчанию для процесса.</span><span class="sxs-lookup"><span data-stu-id="9aa03-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="9aa03-172">Если явно не указано иное, каждый поток будет по умолчанию обрабатываться по умолчанию при создании.</span><span class="sxs-lookup"><span data-stu-id="9aa03-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="9aa03-173">Дополнительные сведения о масштабировании DPI в смешанном режиме см. в статье [масштабирование в смешанном режиме](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .</span><span class="sxs-lookup"><span data-stu-id="9aa03-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>
