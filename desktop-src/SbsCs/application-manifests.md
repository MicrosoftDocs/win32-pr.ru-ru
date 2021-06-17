---
description: Манифест приложения — это файл XML, который описывает и определяет общие и закрытые сборки одновременного выполнения, которые приложению следует подключить во время выполнения.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Манифесты приложений
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230249"
---
# <a name="application-manifests"></a>Манифесты приложений

Манифест приложения — это файл XML, который описывает и определяет общие и закрытые сборки одновременного выполнения, которые приложению следует подключить во время выполнения. Это должны быть те же версии сборок, что и использованные для проверки приложения. Манифесты приложения также могут описывать метаданные закрытых для приложения файлов.

Полный список схем XML см. в разделе [Схема файла манифеста](manifest-file-schema.md).

Манифесты приложений имеют следующие элементы и атрибуты.

| Элемент                               | Атрибуты                | Обязательно |
|---------------------------------------|---------------------------|----------|
| **сборок**                          |                           | Да      |
|                                       | **манифестверсион**       | Да      |
| **не наследовать**                         |                           | Нет       |
| **Неправильн**                  |                           | Да      |
|                                       | **type**                  | Да      |
|                                       | **name**                  | Да      |
|                                       | **language**              | Нет       |
|                                       | **processorArchitecture** | Нет       |
|                                       | **version**               | Да      |
|                                       | **publicKeyToken**        | Нет       |
| **см**                     |                           | Нет       |
| **приложение**                       |                           | Нет       |
| **суппортедос**                       | **Id**                    | Нет       |
| **maxversiontested укажите установленную**                  | **Id**                    | Нет       |
| **зависимостей**                        |                           | Нет       |
| **dependentAssembly**                 |                           | Нет       |
| **file**                              |                           | Нет       |
|                                       | **name**                  | Нет       |
|                                       | **hashAlg**               | Нет       |
|                                       | **hash**                  | Нет       |
| **активекодепаже**                    |                           | Нет       |
| **автоповышение**                       |                           | Нет       |
| **дисаблесеминг**                    |                           | Нет       |
| **дисаблевиндовфилтеринг**            |                           | Нет       |
| **дпиаваре**                          |                           | Нет       |
| **дпиаваренесс**                      |                           | Нет       |
| **гдискалинг**                        |                           | Нет       |
| **хигхресолутионскроллингаваре**      |                           | Нет       |
| **лонгпасаваре**                     |                           | Нет       |
| **принтердриверисолатион**            |                           | Нет       |
| **ултрахигхресолутионскроллингаваре** |                           | Нет       |
| **msix**                              |                           | Нет       |
| **хеаптипе**                          |                           | Нет       |

## <a name="file-location"></a>Расположение файла

Манифесты приложений должны быть добавлены в качестве ресурсов в EXE-файл или библиотеку DLL приложения.

Дополнительные сведения см. в разделе [Установка параллельных сборок](installing-side-by-side-assemblies.md).

## <a name="file-name-syntax"></a>Синтаксис имени файла

Имя файла манифеста приложения — это имя исполняемого объекта приложения, за которым следует manifest.

Например, манифест приложения, который ссылается на example.exe или example.dll, будет использовать следующий синтаксис имени файла. Если идентификатор ресурса равен 1, можно опустить поле <*идентификатор ресурса*>.

**example.exe. <*идентификатор ресурса*>. manifest**

**example.dll. <*идентификатор ресурса*>. manifest**

## <a name="elements"></a>Элементы

В именах элементов и атрибутов учитывается регистр. Значения элементов и атрибутов не учитывают регистр, за исключением значения атрибута Type.

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>сборка

Элемент контейнера. Его первым подэлементом должен быть элемент **NoInherit** или **assemblyIdentity** . Обязательный.

Элемент **Assembly** должен находиться в пространстве имен urn: schemas-microsoft-com: ASM. v1. Дочерние элементы сборки также должны находиться в этом пространстве имен путем наследования или добавления тегов.

Элемент **Assembly** имеет следующие атрибуты.



| attribute           | Описание                                           |
|---------------------|-------------------------------------------------------|
| **манифестверсион** | Атрибут **манифестверсион** должен иметь значение 1,0. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>не наследовать

Включите этот элемент в манифест приложения, чтобы задать [контексты активации](activation-contexts.md) , созданные из манифеста, с флагом "без наследования". Если этот флаг не установлен в контексте активации, а контекст активации активен, он наследуется новыми потоками в том же процессе, в окнах, в процедурах Windows и [асинхронных вызовах процедур](/windows/desktop/Sync/asynchronous-procedure-calls). Установка этого флага предотвращает наследование активного контекста новым объектом.

Элемент **NoInherit** является необязательным и обычно опускается. Большинство сборок работает неправильно с помощью контекста активации без наследования, так как сборка должна быть специально разработана для управления распространением собственного контекста активации. Использование элемента **NoInherit** требует, чтобы все зависимые сборки, на которые ссылается манифест приложения, имели элемент **NoInherit** в [манифесте сборки](assembly-manifests.md).

Если в манифесте используется параметр **NoInherit** , он должен быть первым подэлементом элемента **Assembly** . Элемент **assemblyIdentity** должен идти сразу после элемента **NoInherit** . Если параметр **NoInherit** не используется, то **assemblyIdentity** должен быть первым подэлементом элемента **Assembly** . У элемента **NoInherit** нет дочерних элементов. Он не является допустимым элементом в [манифестах сборки](assembly-manifests.md).

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Как первый подэлемент элемента **Assembly** , **assemblyIdentity** описывает и уникально идентифицирует приложение, владеющее этим манифестом приложения. Как первый подэлемент элемента **dependentAssembly** , **assemblyIdentity** описывает параллельную сборку, необходимую для приложения. Обратите внимание, что каждая сборка, указанная в манифесте приложения, требует наличия **assemblyIdentity** , точно совпадающего с **assemblyIdentity** в манифесте сборки, на которую указывает ссылка.

Элемент **assemblyIdentity** имеет следующие атрибуты. У него нет вложенных элементов.

| attribute                 | Описание                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Указывает тип приложения или сборки. Значение должно быть в виде Win32, а все — в нижнем регистре. Обязательный.                                                                                                                                                                                                                                                                                                                              |
| **name**                  | Уникально именует приложение или сборку. Используйте следующий формат для имени: Organization.Division.Name. Например, Microsoft. Windows. Мисамплеапп. Обязательный.                                                                                                                                                                                                                                                               |
| **language**              | Определяет язык приложения или сборки. Необязательный элемент. Если приложение или сборка зависит от языка, укажите код языка DHTML. На **теге assemblyIdentity** приложения, предназначенного для международных использования (не зависит от языка), не указывайте атрибут Language.<br/> В **теге assemblyIdentity** сборки, предназначенной для международных использования (нейтральный к языку), задайте для параметра Language значение " \* ".<br/> |
| **processorArchitecture** | Указывает процессор. Допустимые значения: `x86`, `amd64`, `arm` и `arm64`. Необязательный элемент.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Указывает версию приложения или сборки. Используйте формат версии из четырех частей: оближешь. nnnnn. ууо. ппппп. Каждая из частей, разделенных точками, может быть 0-65535 включительно. Дополнительные сведения см. в разделе [версии сборки](assembly-versions.md). Обязательный.                                                                                                                                                                        |
| **publicKeyToken**        | 16-символьная шестнадцатеричная строка, представляющая последние 8 байт хэша SHA-1 открытого ключа, для которого подписано приложение или сборка. Открытый ключ, используемый для подписи каталога, должен иметь длину 2048 бит или более. Требуется для всех общих параллельных сборок.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>совместимость

Содержит по крайней мере одно **приложение**. У него нет атрибутов. Необязательный элемент. Манифесты приложений без элемента Compatibility по умолчанию имеют совместимость с Windows Vista в Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>application

Содержит по крайней мере один элемент **суппортедос** . Начиная с Windows 10 версии 1903, она также может содержать один необязательный элемент **maxversiontested укажите установленную** . У него нет атрибутов. Необязательный элемент.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>суппортедос

Элемент **суппортедос** имеет следующий атрибут. У него нет вложенных элементов.

| attribute | Описание   |
|-----------|-----------------------|
| **Id**    | Задайте для атрибута ID значение **{e2011457-1546-43c5-a5fe-008deee3d3f0}** , чтобы запустить приложение с помощью функции Vista. Это может позволить приложению, разработанному для Windows Vista, работать в более поздней версии операционной системы. <br/> Задайте для атрибута ID значение **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** , чтобы запустить приложение с помощью функции Windows 7.<br/> Для приложений, поддерживающих функции Windows Vista, Windows 7 и Windows 8, не требуются отдельные манифесты. В этом случае добавьте идентификаторы GUID для всех операционных систем Windows.<br/> Сведения о поведении атрибута **ID** в Windows см. в статье [совместимость Windows 8 и Windows Server 2012 Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).<br/> Следующие идентификаторы GUID соответствуют указанным операционным системам:<br/> **{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** — > Windows 10, windows Server 2016 и windows Server 2019<br/> **{1f676c76-80e1-4239-95bb-83d0f6d0da78}** — > Windows 8.1 и Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** — > Windows 8 и windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** — > Windows 7 и windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008deee3d3f0}** — > Windows Vista и windows Server 2008<br/> Вы можете протестировать это в Windows 7 или Windows 8. x, запустив монитор ресурсов (ресмон), перейдя на вкладку ЦП, щелкнув правой кнопкой мыши метки столбцов, выбрать столбец и проверить "контекст операционной системы". В Windows 8. x можно также найти этот столбец, доступный в диспетчере задач (панели Диспетчер задач). Содержимое столбца показывает наибольшее найденное значение или "Windows Vista" в качестве значения по умолчанию. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested укажите установленную

Элемент **maxversiontested укажите установленную** указывает версии Windows, с которыми проверялось приложение, начиная с минимальной версии ОС, поддерживаемой приложением до максимальной версии. Полный набор версий можно найти [здесь](https://developer.microsoft.com/windows/downloads/sdk-archive/). Он предназначен для использования в приложениях для настольных систем, использующих [острова XAML](/windows/apps/desktop/modernize/xaml-islands) и не развернутых в пакете MSIX. Этот элемент поддерживается в Windows 10, версии 1903 и более поздних версиях.

Элемент **maxversiontested укажите установленную** имеет следующий атрибут. У него нет вложенных элементов.

| attribute | Описание    |
|-----------|----------------|
| **Id**    | Задайте для атрибута ID строку версии из 4 частей, которая указывает максимальную версию Windows, с которой было протестировано приложение. Например, "10.0.18226.0". |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency

Содержит по меньшей мере один **dependentAssembly**. У него нет атрибутов. Необязательный элемент.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

Первый подэлемент **dependentAssembly** должен быть элементом **assemblyIdentity** , описывающим параллельную сборку, необходимую для приложения. Каждое **dependentAssembly** должно находиться внутри только одной **зависимости**. У него нет атрибутов.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>файл

Указывает файлы, являющиеся частными для приложения. Необязательный элемент.

Элемент **File** содержит атрибуты, приведенные в следующей таблице.



| attribute   | Описание                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Имя файла. Например, Comctl32.dll.                                                            |
| **hashAlg** | Алгоритм, используемый для создания хэша файла. Это значение должно быть SHA1.                                 |
| **hash**    | Хэш файла, на который ссылается имя. Шестнадцатеричная строка длины в зависимости от хэш-алгоритма. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>активекодепаже

Заставить процесс использовать UTF-8 в качестве кодовой страницы процесса.

**активекодепаже** был добавлен в Windows версии 1903 (обновление 2019 мая). Вы можете объявить это свойство и целевой объект или выполнить его в более ранних сборках Windows, но необходимо как обычно выполнять обнаружение и преобразование кодовых страниц прежних версий. Дополнительные сведения см. [в разделе Использование кодовой страницы UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) .

Этот элемент не содержит атрибуты. **UTF-8** является допустимым значением для элемента **активекодепаже** .

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a>автоповышение

Указывает, включен ли автоматический повышенный уровень прав. **Значение true** указывает, что он включен. У него нет атрибутов.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>дисаблесеминг

Указывает, отключено ли предоставление элементов пользовательского интерфейса для темы. **Значение true** указывает, что отключено. У него нет атрибутов.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>дисаблевиндовфилтеринг

Указывает, следует ли отключить фильтрацию окон. **True** — отключить фильтрацию окон, чтобы можно было перечислить иммерсивное окно с рабочего стола. **дисаблевиндовфилтеринг** был добавлен в Windows 8 и не имеет атрибутов.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a>дпиаваре

Указывает, учитывается ли текущий процесс в точках на дюйм (DPI).

**Windows 10, версия 1607:** Элемент **дпиаваре** игнорируется, если имеется элемент **дпиаваренесс** . Можно включить оба элемента в манифест, если вы хотите указать другое поведение для Windows 10 версии 1607, чем для более ранней версии операционной системы.

В следующей таблице описывается поведение, получаемое в зависимости от наличия элемента **дпиаваре** и содержащегося в нем текста. В тексте элемента не учитывается регистр.

| Состояние элемента **дпиаваре** | Описание     |
|-----------------------------------|---------|
| Absent                            | По умолчанию текущий процесс не знает dpi. Этот параметр можно изменить программным путем, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .                                                                                                                                                            |
| Содержит значение "true"                   | Текущий процесс учитывает dpi системы.                                                                                                                                                                                                                                                                                                                                                          |
| Содержит значение "false"                  | Windows **Vista, Windows 7 и Windows 8:** Поведение аналогично поведению, если **дпиаваре** отсутствует.<br/> **Windows 8.1 и Windows 10:** Текущий процесс не знает dpi, и программное изменение этого параметра невозможно выполнить, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |
| Содержит "true/PM"                | Windows **Vista, Windows 7 и Windows 8:** Текущий процесс учитывает dpi системы.<br/> **Windows 8.1 и Windows 10:** Текущий процесс учитывает dpi для каждого монитора.<br/>                                                                                                                                                                                                          |
| Содержит "на монитор"            | Windows **Vista, Windows 7 и Windows 8:** Поведение аналогично поведению, если **дпиаваре** отсутствует.<br/> **Windows 8.1 и Windows 10:** Текущий процесс учитывает dpi для каждого монитора.<br/>                                                                                                                                                                                      |
| Содержит любую другую строку         | Windows **Vista, Windows 7 и Windows 8:** Поведение аналогично поведению, если **дпиаваре** отсутствует.<br/> **Windows 8.1 и Windows 10:** Текущий процесс не знает dpi, и программное изменение этого параметра невозможно выполнить, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |

Дополнительные сведения о параметрах осведомленности о dpi см. в разделе [Сравнение уровней осведомленности о dpi](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

**дпиаваре** не имеет атрибутов.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a>дпиаваренесс

Указывает, учитывается ли текущий процесс в точках на дюйм (DPI).

Минимальная версия операционной системы, поддерживающая элемент **дпиаваренесс** , — Windows 10, версия 1607. Для версий, которые поддерживают элемент **дпиаваренесс** , **дпиаваренесс** переопределяет элемент **дпиаваре** . Можно включить оба элемента в манифест, если вы хотите указать другое поведение для Windows 10 версии 1607, чем для более ранней версии операционной системы.

Элемент **дпиаваренесс** может содержать один элемент или список элементов с разделителями-запятыми. В последнем случае используется первый (крайний левый) элемент в списке, распознанном операционной системой. Таким образом можно указать различные варианты поведения, поддерживаемые в будущих версиях операционной системы Windows.

В следующей таблице описывается поведение, получаемое в зависимости от наличия элемента **дпиаваренесс** и содержащегося в нем текста в его левом распознанном элементе. В тексте элемента не учитывается регистр.

| состояние элемента **дпиаваренесс** :        | Описание                          |
|-----------------------------------------|-------------------------------------------|
| Отсутствует элемент                       | Элемент **дпиаваре** указывает, учитывается ли в процессе разрешение dpi.                                                                                                                                                                   |
| Не содержит распознанные элементы            | По умолчанию текущий процесс не знает dpi. Этот параметр можно изменить программным путем, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) . |
| Первый распознанный элемент — "System"       | Текущий процесс учитывает dpi системы.                                                                                                                                                                                               |
| Первый распознанный элемент — "пермонитор"   | Текущий процесс учитывает dpi для каждого монитора.                                                                                                                                                                                          |
| Первый распознанный элемент — "permonitorv2" | В текущем процессе используется контекст осведомленности по dpi для каждого монитора. Этот элемент будет распознан только в Windows 10 версии 1703 или более поздней.                                                                                              |
| Первый распознанный элемент «не осведомлен»      | Текущий процесс является неосведомленным от dpi. Вы **не можете** программно изменить этот параметр, вызвав функцию [**сетпроцессдпиаваренесс**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) или [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .      |

Дополнительные сведения о параметрах осведомленности о разрешении, поддерживаемых этим элементом, см. в разделе [ \_ Поддержка dpi](/windows/desktop/api/windef/ne-windef-dpi_awareness) и [ \_ \_ контекст осведомленности](/windows/desktop/hidpi/dpi-awareness-context)о dpi.

**дпиаваренесс** не имеет атрибутов.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a>гдискалинг

Указывает, включено ли масштабирование GDI. Минимальная версия операционной системы, поддерживающая элемент **гдискалинг** , — Windows 10 версии 1703.

Платформа GDI (интерфейс графических устройств) может применять масштабирование DPI к примитивам и тексту на уровне отдельных мониторов без обновления самого приложения. Это может быть полезно для приложений GDI, которые больше не обновляются.

Невекторная графика (например, точечные рисунки, значки или панели инструментов) не может масштабироваться этим элементом. Кроме того, графика и текст, отображаемые в растровых изображениях, динамически создаваемые приложениями, также не могут масштабироваться этим элементом.

**Значение true** указывает, что этот элемент включен. У него нет атрибутов.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a>хигхресолутионскроллингаваре

Указывает, включено ли разрешение на прокрутку с высоким разрешением. **Значение true** указывает, что он включен. У него нет атрибутов.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>лонгпасаваре

Включает длинные пути, длина которых превышает **MAX_PATH** . Этот элемент поддерживается в Windows 10, версии 1607 и более поздних версиях. Дополнительные сведения см. в [этой статье](../fileio/maximum-file-path-limitation.md).

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a>принтердриверисолатион

Указывает, включена ли изоляция драйвера принтера. **Значение true** указывает, что он включен. У него нет атрибутов. Изоляция драйвера принтера повышает надежность службы печати Windows, позволяя драйверам принтера выполняться в процессах, отдельных от процесса, в котором работает диспетчер очереди печати. Поддержка изоляции драйвера принтера начата в Windows 7 и Windows Server 2008 R2. Приложение может объявить изоляцию драйвера принтера в своем манифесте приложения, чтобы изолировать себя от драйвера принтера и повысить его надежность. Это значит, что приложение не будет завершаться сбоем, если в драйвере принтера произошла ошибка.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a>ултрахигхресолутионскроллингаваре

Указывает, включено ли разрешение на прокрутку Ultra-High-resolution. **Значение true** указывает, что он включен. У него нет атрибутов.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>msix

Указывает сведения об удостоверении [разреженного пакета MSIX](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) для текущего приложения. Этот элемент поддерживается в Windows 10, версии 2004 и более поздних версиях.

Элемент **msix** должен находиться в пространстве имен `urn:schemas-microsoft-com:msix.v1` . Он содержит атрибуты, приведенные в следующей таблице.

| attribute   | Описание                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **publisher**    | Описание сведений об издателе. Это значение должно соответствовать атрибуту **издателя** в элементе [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) манифеста разреженного пакета. |
| **packageName** | Описывает содержимое пакета. Это значение должно соответствовать атрибуту **Name** в элементе [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) манифеста разреженного пакета.    |
| **applicationId**    | Уникальный идентификатор приложения. Это значение должно соответствовать атрибуту **ID** в элементе [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) в манифесте разреженного пакета.  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a>хеаптипе

Переопределяет реализацию кучи по умолчанию для использования [API кучи Win32](../Memory/heap-functions.md) .

* Значение **сегменсеап** указывает, что будет использоваться куча сегмента. Куча сегментов — это современная реализация кучи, которая обычно сокращает общее использование памяти. Этот элемент поддерживается в Windows 10, версия 2004 (сборка 19041) и более поздние версии.
* Все остальные значения игнорируются.

Этот элемент не содержит атрибуты.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a>Пример

Ниже приведен пример манифеста приложения для приложения с именем MySampleApp.exe. Приложение использует Самплеассембли параллельную сборку.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
