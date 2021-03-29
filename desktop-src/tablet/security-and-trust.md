---
description: В платформе .NET Framework реализована система безопасности, по-разному обрабатывающая приложения в зависимости от их происхождения.
ms.assetid: 37fa870a-6f38-44ae-943e-27697f6b9fba
title: Безопасность и доверие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e3039f8aa93c2ae563a918177462cd09a217af
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105647753"
---
# <a name="security-and-trust"></a>Безопасность и доверие

В платформе .NET Framework реализована система безопасности, по-разному обрабатывающая приложения в зависимости от их происхождения. Исполняемые файлы и сборки, наявляющиеся от компьютера пользователя, обычно выполняются с полным доверием; те же исполняемые файлы и сборки, работающие через Интернет, обычно выполняются с частичным доверием. Это необходимо для того, чтобы вредоносный код не читал или не изменял сведения, к которым у него нет доступа, например локальные файлы, элементы в буфере обмена и другие ресурсы. Если исполняемый объект вызывает сборку, которая, в свою очередь, вызывает другую сборку, для которой требуется определенный уровень доверия, применяется самый низкий уровень доверия всех компонентов в цепочке. Однако администратор компьютера может задать определенные разрешения, переопределяющие разрешения по умолчанию.

Обзор модели безопасности задается в [защищенных Light-Weight Client-Sideных элементах управления](/archive/msdn-magazine/2002/january/dhtml-and-net-host-secure-lightweight-client-side-controls-in-microsoft-internet-explorer), и вы можете получить более подробную информацию о модели безопасности в [системе безопасности доступа к коду на практике](/previous-versions/msp-n-p/ff648663(v=pandp.10)). Хороший обзор безопасности библиотек (особенно важных для объектов [**UserControl**](/uwp/api/Windows.UI.Xaml.Controls.UserControl?view=winrt-19041) на веб-странице) можно найти в разделе [Использование библиотек из частично доверенного кода](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconusinglibrariesfrompartiallytrustedcode.asp), а другие сведения о безопасности управляемых элементов управления можно найти в статье [Создание защищенных управляемых элементов управления](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconwritingsecuremanagedcontrols.asp%3fframe%3dtrue).

## <a name="permissions"></a>Разрешения

Большинство управляемых объектов и членов API технологий для планшетных ПК имеют два требования:

-   Выполнение всегда требуется.
-   При выполнении действия по обеспечению безопасности [InheritanceDemand](/previous-versions/windows/) требуется FullTrust. Это означает, что требуется полное доверие, если производный класс наследует класс или переопределяет метод из пакета SDK для планшетных ПК.

В следующей таблице перечислены классы и члены, для которых требуются дополнительные разрешения. Разрешения для данного класса также применяются ко всем членам, не перечисленным в этой таблице.



| Класс или метод                                                                       | Разрешения                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**канпасте**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                                  | [UIPermissionClipboard. Аллклипбоард](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. Клипбоардкопи**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                                    | [UIPermissionClipboard. Овнклипбоард](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. Клипбоардпасте**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                                  | [UIPermissionClipboard. Аллклипбоард](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**InkCollector**](inkcollector-class.md)                                            | [UIPermissionWindow. Сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| InkCollector (IntPtr)                                                                  | [UIPermissionWindow. сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| InkCollector. Handle                                                                   | [UIPermissionWindow. аллвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (см. Примечание ниже)<br/> |
| InkEdit                                                                               | [UIPermissionWindow. Сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [InkOverlay](/previous-versions/ms552322(v=vs.100))                                   | [UIPermissionWindow. Сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| InkOverlay (IntPtr)                                                                    | [UIPermissionWindow. сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и SecurityPermissionFlag. UnmanagedCode<br/>                                                                 |
| [InkOverlay. Handle](/previous-versions/ms833109(v=msdn.10))                      | [UIPermissionWindow. аллвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (см. Примечание ниже)<br/> |
| [InkPicture](/previous-versions/aa514604(v=msdn.10))                                   | [UIPermissionWindow. Сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| [пенинпутпанел](/previous-versions/aa514041(v=msdn.10))                             | См. примечание ниже.<br/>                                                                                                                                                                                     |
| [**инкрендерер**](inkrenderer-class.md)                                              | [UIPermissionWindow. Сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw), [ **дравстроке**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)        | [UIPermissionWindow. сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Модуль подготовки. Инкспацетопиксел (IntPtr, Point), визуализатор. Инкспацетопиксел (IntPtr, Point \[ \] )    | [UIPermissionWindow. сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Модуль подготовки. Пикселтоинкспаце (IntPtr, Point), визуализатор. Пикселтоинкспаце (IntPtr, Point \[ \] )    | [UIPermissionWindow. сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))                                      | [UIPermissionWindow. Сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| DynamicRenderer (IntPtr)                                                               | [UIPermissionWindow. сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**Каскад**](realtimestylus-class.md)                                        | [UIPermissionWindow. Сафетоплевелвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| RealTimeStylus (IntPtr), RealTimeStylus (IntPtr, Boolean), RealTimeStylus (IntPtr, планшетный) | [UIPermissionWindow. аллвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>                  |



 

> [!Note]  
> Обычно предпочтительнее использовать элемент управления, а не дескриптор (IntPtr) для конструкторов, так как для элементов управления требуется меньше разрешений. Аналогичным образом предпочтительнее использовать графический объект, а не маркер для модуля подготовки отчетов [. Draw](/previous-versions/ms828488(v=msdn.10)), модуля [подготовки отчетов. Инкспацетопиксел](/previous-versions/ms828495(v=msdn.10)) и модуля [подготовки](/previous-versions/ms828505(v=msdn.10))отчетов. пикселтоинкспаце.

 

> [!Note]  
> Свойства [InkCollector. Handle](/previous-versions/ms836504(v=msdn.10)) и [InkOverlay. Handle](/previous-versions/ms833109(v=msdn.10)) не нуждаются в разрешении [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) , если этот обработчик предназначен для Windows Formsного элемента управления, но для других окон.

 

> [!Note]  
> Для класса [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) следующим методам и свойствам требуются [SecurityPermissionFlag. аллфлагс](/previous-versions/windows/): пенинпутпанел (IntPtr), [аттачедедитвиндов](/previous-versions/ms582240(v=vs.100)), [Busy](/previous-versions/ms571975(v=vs.100)), [коммитпендингинпут](/previous-versions/ms569650(v=vs.100)), [куррентпанел](/previous-versions/ms571976(v=vs.100)), [DefaultPanel](/previous-versions/ms571977(v=vs.100)), [EnableTsf](/previous-versions/ms569656(v=vs.100)), [Factoid](/previous-versions/ms571978(v=vs.100)), [Height](/previous-versions/ms571979(v=vs.100)), HorizontalOffset, [InputFailed](/previous-versions/ms567738(v=vs.100)), [Left](/previous-versions/ms571981(v=vs.100)), [MoveTo](/previous-versions/ms569667(v=vs.100)), [PanelChanged](/previous-versions/ms567741(v=vs.100)), [PanelMoving](/previous-versions/ms567748(v=vs.100)), [Обновить](/previous-versions/ms569778(v=vs.100)), [Top](/previous-versions/ms571982(v=vs.100)), [VerticalOffset](/previous-versions/ms571983(v=vs.100)), [Visible](/previous-versions/ms571984(v=vs.100)), [VisibleChanged](/previous-versions/ms567754(v=vs.100))и [Width](/previous-versions/ms571985(v=vs.100)). [](/previous-versions/ms571980(v=vs.100))

 

## <a name="other-considerations"></a>Другие вопросы

Ниже приведены некоторые другие известные вопросы безопасности.

-   Чтобы веб-элементы управления работали правильно, требуется Microsoft Internet Explorer 6 или более поздняя версия. В Internet Explorer 5,5 только начальные управляемые элементы управления загружаются; Дополнительные элементы управления нельзя загружать динамически во время выполнения.
-   Если используется Windows XP с пакетом обновления 2 (SP2) и CLR 1.0, то для веб-элементов управления в Internet Explorer требуется добавить сайт в качестве доверенного сайта, даже если они находятся в зоне интрасети. Однако при этом они больше не будут выполняться в зоне доверенного сайта, хотя они выполняются в зоне интрасети. Эта проблема устранена в среде CLR 1.1.

 

 