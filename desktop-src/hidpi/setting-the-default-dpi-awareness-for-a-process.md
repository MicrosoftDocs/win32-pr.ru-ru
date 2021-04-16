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
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Настройка отслеживания количества точек на дюйм по умолчанию для процесса

Классические приложения в Windows могут работать в разных режимах определения DPI. Эти режимы позволяют разрешать различные способы масштабирования DPI и могут использовать разные пространства координат. Дополнительные сведения о поддержке DPI см. в разделе [Разработка приложений с высоким разрешением в Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) Важно явно задать режим поддержки DPI по умолчанию для процесса, чтобы избежать непредвиденного поведения.

Существует два основных метода указания сведений о DPI по умолчанию для процесса:

1 \) через параметр манифеста приложения

2 \) программным путем через вызов API

Рекомендуется указывать сведения о соответствии процесса по умолчанию для процессов с помощью параметра манифеста. При указании интерфейса API по умолчанию поддержка не рекомендуется.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Настройка осведомленности по умолчанию в манифесте приложения

Существует два параметра манифеста, которые позволяют указать режим поддержки по умолчанию для отслеживания количества точек на дюйм: \<dpiAwareness\> и \<dpiAware\> . \<dpiAware\> была введена в Windows Vista и позволяет установить для процесса по умолчанию только сведения о системе. \<dpiAwareness\> был введен в Windows 10 версии 1607 и позволяет указать упорядоченный список режимов по умолчанию для отслеживания количества точек на дюйм. Это позволяет задать режимы определения количества точек на дюйм для резервного копирования, которые будут использоваться, если приложение запущено в версии Windows не может поддерживать первый режим службы поддержки. В более старых версиях Windows новый \<dpiAwareness\> тег будет проигнорирован. Это означает, что можно использовать оба этих параметра манифеста, чтобы включить сценарий, в котором по умолчанию для процесса может быть включена поддержка системы в более старой версии Windows при Per-Monitor в версиях, превышающих Windows 10, версия 1607. В Windows 10 версии 1607 и в \<dpiAware\> параметр не учитывается, если \<dpiAwareness\> элемент имеется в наличии.

В следующей таблице показано, как задать различные режимы поддержки DPI по умолчанию для процессов с помощью двух параметров манифеста:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Обработка режима поддержки DPI по умолчанию</th>
<th>&lt;&gt;параметр дпиаваре</th>
<th>&lt;&gt;параметр дпиаваренесс (Windows 10, версия 1607 и более поздние)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>связан</td>
<td><p>Н/д (нет параметра Дпиаваре в манифесте)</p>
<p>или</p>
<p>&lt;Дпиаваре &gt; false &lt; /дпиаваре&gt;</p></td>
<td>&lt;Дпиаваренесс &gt; &lt; /дпиаваренесс&gt;</td>
</tr>
<tr class="even">
<td>С учетом системы</td>
<td>&lt;Дпиаваре &gt; Истина &lt; /дпиаваре&gt;</td>
<td>&lt;Дпиаваренесс &gt; System &lt; /дпиаваренесс&gt;</td>
</tr>
<tr class="odd">
<td>На монитор</td>
<td>&lt;Дпиаваре &gt; true/PM &lt; дпиаваре&gt;</td>
<td>&lt;Дпиаваренесс &gt; пермонитор &lt; /дпиаваренесс&gt;</td>
</tr>
<tr class="even">
<td>На монитор версии 2</td>
<td>Не поддерживается</td>
<td>&lt;Дпиаваренесс &gt; PerMonitorV2 &lt; /дпиаваренесс&gt;</td>
</tr>
</tbody>
</table>

 

В приведенном ниже примере показаны \<dpiAwareness\> Параметры и, используемые в одном и том \<dpiAware\> же файле манифеста, для настройки поведения процесса по умолчанию для отслеживания dpi для различных версий Windows.

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

## <a name="setting-default-awareness-programmatically"></a>Программное задание осведомленности по умолчанию

Хотя это и не рекомендуется, по умолчанию можно задать отслеживание количества точек на дюйм программным способом. После создания окна (HWND) в процессе изменение режима поддержки DPI больше не поддерживается. Если вы устанавливаете режим поддержки по умолчанию для обработки точек на дюйм как программно, необходимо вызвать соответствующий API перед созданием дескрипторов HWND.

Существует несколько интерфейсов API, которые позволяют указать для процесса сведения о DPI по умолчанию. Текущий рекомендуемый API — [**сетпроцессдпиаваренессконтекст**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), так как более старые API предлагают меньше функциональных возможностей.

 

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
<th>API</th>
<th>Минимальная версия Windows</th>
<th>Неосведомленность DPI</th>
<th>Учитывать DPI системы</th>
<th>На уровне DPI для каждого монитора</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">сетпроцессдпиаваре</a></td>
<td>Windows Vista</td>
<td>Н/Д</td>
<td>Сетпроцессдпиаваре ()</td>
<td>Н/Д</td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>сетпроцессдпиаваренесс</strong></a></td>
<td>Windows 8.1</td>
<td>Сетпроцессдпиаваренесс (PROCESS_DPI_UNAWARE)</td>
<td>Сетпроцессдпиаваренесс (PROCESS_DPI_SYSTEM_DPI_AWARE)</td>
<td>Сетпроцессдпиаваренесс (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>сетпроцессдпиаваренессконтекст</strong></a></td>
<td>Windows 10, версия 1607</td>
<td>Сетпроцессдпиаваренессконтекст (DPI_AWARENESS_CONTEXT_UNAWARE)</td>
<td>Сетпроцессдпиаваренессконтекст (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</td>
<td><p>Сетпроцессдпиаваренессконтекст (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p>
<p>Сетпроцессдпиаваренессконтекст (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a>Процесс-по умолчанию и поток по умолчанию

В этом документе описывается установка по умолчанию для процесса отслеживания DPI. Это обусловлено тем, что в Windows 10 появилась поддержка использования более одного режима поддержки точек на дюйм в одном процессе (до Windows 10, весь процесс должен соответствовать режиму поддержки одного DPI). Поддержка выполнения более одного режима поддержки DPI в рамках процесса называется масштабированием DPI в смешанном режиме. При использовании масштабирования DPI в смешанном режиме в пределах процесса каждое окно верхнего уровня может работать в режиме поддержки DPI, который может отличаться от значения по умолчанию для процесса. Если явно не указано иное, каждый поток будет по умолчанию обрабатываться по умолчанию при создании. Дополнительные сведения о масштабировании DPI в смешанном режиме см. в статье [масштабирование в смешанном режиме](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .
