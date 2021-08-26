---
description: начиная с Windows 8, пакет SDK DirectX входит в состав Windows SDK.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: Где находится пакет SDK для DirectX?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46559e839abea9d6e0c89ab7e5940e46b2d4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886457"
---
# <a name="where-is-the-directx-sdk"></a>Где находится пакет SDK для DirectX?

начиная с Windows 8, пакет SDK DirectX входит в состав Windows SDK.

Мы первоначально создали пакет SDK DirectX как высокопроизводительную платформу для разработки игр на Windows. По мере разработки технологий DirectX они стали важны для более широкого спектра приложений. Сегодня доступность оборудования Direct3D на компьютерах, в том числе традиционных настольных приложений, для использования аппаратного ускорения графики. В параллельном режиме технологии DirectX интегрируются с Windows. Теперь DirectX является основной частью Windows.

поскольку Windows SDK является основным пакетом SDK для разработчиков Windows, теперь в него включен DirectX. теперь вы можете использовать Windows SDK для создания отличных игр для Windows. чтобы скачать пакет sdk Windows 8. x или пакет sdk для Windows 10, см. раздел [Windows SDK и emulator archive](https://developer.microsoft.com/windows/downloads/sdk-archive).

следующие технологии и средства, ранее являющиеся частью пакета SDK для DirectX, теперь являются частью Windows SDK.


| Технология или инструмент | Описание | 
|--------------------|-------------|
| <span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Windows Графические компоненты<br /> | заголовки и библиотеки для <a href="/windows/desktop/direct3d">Direct3D</a> и других Windows графических интерфейсов api, таких как <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>, доступны в Windows SDK. <br /><blockquote>[!Note]<br />устаревшие библиотеки служебной программы D3DX9/D3DX10/D3DX11 доступны через <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>, но также существует ряд <a href="https://walbourn.github.io/living-without-d3dx/">альтернатив с открытым кодом</a>. библиотека служебной программы D3DCSX DirectCompute и распространяемая библиотека DLL доступны в Windows SDK. D3DX12 доступен на <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>.</blockquote><br /> | 
| <span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>Компилятор HLSL (FXC.EXE)<br /> | компилятор <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> — это инструмент в соответствующем подкаталоге архитектуры в папке bin в Windows SDK.<br /><blockquote>[!Note]<br />API D3DCompiler и распространяемая библиотека DLL доступны в Windows SDK.</blockquote><br /><br />для разработки DirectX 12 используйте дкскомпилер в Windows SDK и размещается на [GitHub](https://github.com/Microsoft/DirectXShaderCompiler).<br /> | 
| <span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>PIX для Windows<br /> | замена средства PIX for Windows теперь является функцией в Microsoft Visual Studio, называемой Visual Studio отладчика графики. эта функция значительно улучшила удобство использования, поддержку Windows 8 и Direct3D 11,1, а также интеграцию с традиционными Microsoft Visual Studioными функциями, такими как стеки вызовов и отладка Windows для <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> . Дополнительные сведения об этой новой функции см. в разделе <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">Отладка графики DirectX</a>.<br /><br />Сведения о разработке DirectX 12 см. в статье новейшее поколение <a href="https://devblogs.microsoft.com/pix/">PIX на Windows</a><br /> | 
| <span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> для Windows<br /> | API <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> теперь является системным компонентом в Windows 8. x и Windows 10. заголовки и библиотеки для XAudio2 доступны в Windows SDK. сведения о поддержке Windows 7 см. в разделе <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br /> | 
| <span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">Ксинпут</a> для Windows<br /> | API <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">ксинпут</a> 1,4 теперь является системным компонентом в Windows 8. x и Windows 10. заголовки и библиотеки для ксинпут доступны в Windows SDK.<br /><blockquote>[!Note]<br />устаревшие ксинпут 9.1.0 также доступны в составе Windows 7 или более поздней версии.</blockquote><br /> | 
| <span id="XNAMATH"></span><span id="xnamath"></span>кснамас<br /> | Последняя версия КСНАМАС, которая обновляется для новых наборов инструкций, а также ARM/ARM64, теперь <a href="/windows/desktop/dxmath/directxmath-portal">директксмас</a>. заголовки для директксмас доступны в Windows SDK и в <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>.<br /> | 
| <span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>Панель управления DirectX и средство просмотра возможностей DirectX<br /> | служебные программы directx для панели управления и средства просмотра возможностей directx включены в соответствующий подкаталог архитектуры в папке bin в Windows SDK. Средство просмотра возможностей DirectX также доступно на <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>.<br /> | 
| <span id="XACT"></span><span id="xact"></span>XACT<br /> | Средство для работы с Xbox Audio Cross Platform (активной платформы) больше не поддерживается для Windows.<br /> | 
| <span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Обозреватель игр</a> и гдфмакер<br /> | API <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">обозревателя игр</a> представляет собой игры для пользователей Windows. API обозревателя игр поддерживается только в Windows Vista и Windows 7. используйте средство студии файла определения игр (GDFMAKER.EXE), чтобы объявить рейтинги игр для приложений Windows Store. <br /> средство студии файла определения игр (GDFMaker.exe) включено в подкаталог x86 в папке bin в Windows SDK и поддерживает приложения Windows магазина и классические приложения Win32.<br /><br /> | 
| <span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Примеры<br /> | примеры приложений, которые выделяют технологии DirectX 12, можно найти на Windows в репозитории <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">примеров directx</a> . Большинство примеров для более ранних версий Direct3D также доступны в Интернете. Дополнительные сведения об этих примерах см. в статье <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">Каталог примеров DirectX SDK</a>.<br /> | 
| <span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>Управляемый DirectX 1,1<br /> | Сборки .NET DirectX являются устаревшими и не рекомендуются для использования новыми приложениями. Доступно несколько вариантов. См. раздел <a href="https://walbourn.github.io/directx-and-net/">DirectX и .NET</a>. <br /> | 




 

Устаревший пакет SDK DirectX можно скачать из [центра загрузки Майкрософт](https://go.microsoft.com/fwlink/?LinkId=226640) , если это необходимо, но использовать для новых проектов не рекомендуется.

> [!Note]  
> Пакет SDK для DirectX не устанавливается, если у вас уже установлена определенная версия распространяемого пакета Visual C++ 2010. Дополнительные сведения о и решении для устранения этой проблемы см. в разделе [об ошибке "S1023" при установке пакета SDK DirectX (июнь 2010)](https://support.microsoft.com/kb/2728613).

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Использование проектов DirectX SDK с Visual Studio

примеры из пакета SDK DirectX за июнь 2010 поддерживаются с номерами sku premium Visual Studio (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 или Microsoft Visual Studio Ultimate 2013) на Windows 7, а также Windows 8 и более поздних версий. из-за перехода заголовков и библиотек DirectX в Windows SDK изменения параметров проекта необходимы для правильной сборки этих примеров с учетом того, как пакет SDK Windows 8 и более поздних версий упакован с номерами sku premium Visual Studio.

Эти действия также применяются к собственным проектам, которые зависят от пакета SDK DirectX.

1.  Убедитесь, что на компьютере разработчика установлен выпуск пакета SDK для DirectX от июня 2010. при установке на компьютер, работающий под Windows 8 и более поздних версий, вам будет предложено включить .net 3,5 в качестве предварительной установки пакета SDK для DirectX.

    > [!Note]  
    > Пакет SDK для DirectX не устанавливается, если у вас уже установлена определенная версия распространяемого пакета Visual C++ 2010. Дополнительные сведения о и решении для устранения этой проблемы см. в разделе [об ошибке "S1023" при установке пакета SDK DirectX (июнь 2010)](https://support.microsoft.com/kb/2728613).

     

2.  убедитесь, что используется один из номеров sku premium Visual Studio. Microsoft Visual Studio Express 2012 для Windows 8 или Microsoft Visual Studio Express 2013 для Windows не будет создавать Windows 8 и более поздние настольные приложения, такие как примеры пакета SDK для DirectX. чтобы установить один из sku Visual Studio premium, перейдите по ссылке: [Visual Studio downloads](https://www.microsoft.com/visualstudio/11/downloads) и следуйте инструкциям.

3.  Используйте пример браузера DirectX SDK для установки файлов проекта для требуемого примера. откройте файл решения, совместимого с Microsoft Visual Studio 2010 (с суффиксом **\_ 2010**).

4.  при открытии образца в системе, в которой установлены только Microsoft Visual Studio 2012 или Microsoft Visual Studio 2013, появляется следующее сообщение: "это решение содержит один или несколько проектов, использующих более раннюю версию VC++ компилятора и библиотек. каждый проект можно обновить для использования VC++ компилятора и библиотек (v110). Выберите параметр **Обновить** в этом диалоговом окне, чтобы обновить его перед открытием проекта.

    в противном случае можно обновить компилятор и библиотеки Visual Studio 2012 или Visual Studio 2013 C++ 11 после загрузки, щелкнув решение правой кнопкой мыши и выбрав пункт **обновить VC++ проекты**.

5.  D3DX не считается каноническим API для использования Direct3D в Windows 8 и более поздних версий и, следовательно, не входит в соответствующие Windows SDK. Изучите альтернативные решения для работы с API Direct3D. для проектов предыдущих версий, таких как примеры sdk для directx Windows 7 (и более ранних версий), необходимо выполнить следующие действия для создания приложений с помощью D3DX с использованием пакета sdk directx:

    1.  измените каталоги **VC++** проекта следующим образом, чтобы использовать правильный порядок для заголовков и библиотек пакета SDK.

        <dl> i. откройте **свойства** проекта и выберите страницу **VC++ каталоги** .  
        ii. Выберите **все конфигурации и все платформы**.  
        iii. Задайте следующие каталоги:

        -   Каталоги исполняемых файлов: **<inherit from parent or project defaults>** (в раскрывающемся списке справа)
        -   Каталоги включаемых каталогов: **$ (IncludePath); $ (дкссдк \_ dir) include**
        -   Включить каталоги библиотек: **$ (либрарипас); $ (дкссдк \_ dir) lib \\ x86**

          
        iv. Щелкните **Применить**.  
        v. Выберите **платформу x64**.  
        vi. Задайте **Каталог библиотеки** следующим образом:

        -   Каталоги библиотек: **$ (либрарипас); $ (дкссдк \_ dir) lib \\ x64**

          
        </dl>

    2.  Если в проект включены "d3dx9. h", "d3dx10. h" или "d3dx11. h", обязательно явно включите "d3d9. h", "d3d10. h" и "DXGI. h", "D3D11. h" и "DXGI. h", чтобы убедиться, что вы выберете новую версию. При необходимости можно отключить **предупреждение C4005** . Однако это предупреждение означает, что вы используете более раннюю версию этих заголовков.
    3.  Удалите все ссылки на Дксгитипе. h в проекте. этот заголовок не существует в Windows SDK, и версия пакета SDK для DirectX конфликтует с новым winerror. h.
    4.  Все библиотеки DLL D3DX устанавливаются на компьютер разработчика при установке пакета SDK для DirectX. Убедитесь, что необходимые зависимости D3DX перераспределяются с любым примером или с приложением, если оно перемещается на другой компьютер.
    5.  Имейте в виду, что технологии замены для текущего использования D3DX11 включают [директкстекс](https://github.com/Microsoft/DirectXTex), [директкстк](https://github.com/Microsoft/DirectXTK), [директксмеш](https://github.com/Microsoft/DirectXMesh)и [уватлас](https://github.com/Microsoft/UVAtlas). D3DXMath заменяется на [директксмас](./dxmath/directxmath-portal.md).

6.  Убедитесь, что вы используете новую версию компилятора шейдеров HLSL, просматривая следующие условия:

    1.  изменение исполняемого каталога на шаг 5 приведет к тому, что сборки проекта будут использовать FXC из Windows SDK установки. Имейте в виду, что файлы HLSL теперь официально распознаются Visual Studio. Их можно добавить как файлы проекта и задать параметры компилятора с помощью системы проектов.

    2.  При вызове компиляции во время выполнения с помощью устаревшей библиотеки DLL D3DX будет использоваться неправильная старая версия компилятора HLSL. Замените все ссылки на \* API D3DXCompile, D3DX10Compile \* и D3DX11Compile \* в коде на функцию D3DCompile в D3DCOMPILER \_46.DLL или D3DCOMPILER \_47.DLL.

    3.  Любой проект, использующий компиляцию шейдера времени выполнения, должен иметь D3DCOMPILER \_xx.DLL, скопированный в локальный путь к исполняемому файлу для проекта. эта библиотека DLL доступна в этом подкаталоге Windows SDK установки в разделе **% programfiles (x86)% \\ Windows kits \\ 8,0 \\ \\ \\ &lt; &gt; redist d3d** , либо **% ProgramFiles (x86 \\ \\ \\ \\ \\ &lt; &gt; )% Windows kit 8,1** , где **&lt; arch &gt;** — **x86** и **x64**.

        47.DLL D3DCOMPILER \_46.DLL или D3DCOMPILER \_ из Windows SDK не является системным компонентом и не должны копироваться в системный каталог Windows. Эту библиотеку DLL можно распространить на другие компьютеры с помощью приложения в качестве параллельной библиотеки DLL.

7.  любой проект, использующий API ксинпут и предназначенный для работы в Windows 7 или более ранних версиях Windows должен использовать либо устаревшую версию (9.1.0), либо явно включать заголовки и библиотеки для этого компонента из пакета SDK DirectX. Заголовок Ксинпут и КСИНПУТ. LIB, включенный в Windows SDK, предназначен только для версии (1,4), которая поставляется в составе Windows 8 и более поздних версий. Один и тот же заголовок можно использовать с XINPUT9 \_ 1 \_ 0. lib для использования устаревшей версии, которая включена в более ранние версии Windows. Устаревшая версия Ксинпут не обнаруживает полные возможности или поддерживает аудио, интегрированную с контроллером, поэтому, если требуется поддержка этих функций, необходимо использовать DirectX SDK версии (1,3).

    Чтобы использовать Полнофункциональный API-интерфейс нижнего уровня Ксинпут, вы должны `#include` напрямую воспользоваться заголовком ксинпут из пакета SDK DirectX:

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... а в параметрах компоновщика для дополнительных зависимостей выполните прямую ссылку на библиотеку DirectX SDK Ксинпут:

    **% ДКССДК \_ dir% include \\ &lt; arch &gt; \\ ксинпут. lib**

    \_двоичный3.DLL XINPUT1 устанавливается в каталоги Windows систем с помощью установки пакета SDK DirectX на компьютере разработчика. Вам потребуется повторно распространить этот двоичный файл с помощью приложения, используя установку DirectX из пакета SDK DirectX.

8.  любой проект, использующий API XAudio2 и предназначенный для работы в Windows 7 или более ранних версиях Windows должен использовать либо более старую версию (9.1.0), либо явно включать заголовки и библиотеки для этого компонента из пакета SDK DirectX. заголовки XAudio2 и библиотеки, включенные в Windows SDK предназначены только для версии (2,8), которая входит в состав Windows 8.

    Например, при использовании XAudio2 необходимо `#include` напрямую заXAudio2 заголовки из пакета SDK DirectX:

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... а в параметрах компоновщика для дополнительных зависимостей выполните прямую ссылку на библиотеку DirectX SDK XAudio2:

    **% ДКССДК \_ dir% include \\ &lt; arch &gt; \\ XAudio2. lib**

    \_двоичный7.DLL XAUDIO2 устанавливается в каталоги Windows систем с помощью установки пакета SDK DirectX на компьютере разработчика. Эти библиотеки необходимо распространить вместе с приложением с помощью установки DirectX из пакета SDK DirectX.

9.  если вы использовали пакет sdk для directx с предыдущими версиями Visual Studio, обновление Visual Studio 2010 может перенести путь пакета SDK directx в параметры проекта по умолчанию. Рекомендуется удалить эти параметры, чтобы предотвратить возникновение ошибок сборки в будущем. в **локальной папке% USERPROFILE% \\ AppData \\ Local \\ microsoft \\ MSBuild \\ v 4.0** измените файлы **microsoft. cpp. Win32. user** и **microsoft. Cpp. x64. user** , чтобы удалить все ссылки на пути к дкссдк \_ DIR. Кроме того, можно удалить весь &lt; узел PropertyGroup &gt; , содержащий записи пути, такие как &lt; ExecutablePath &gt; и IncludePath, &lt; &gt; чтобы вернуться к стандартным значениям по умолчанию. Если в этих файлах не отображаются ссылки на ДКССДК \_ dir, изменения не требуются.

10. если полученное приложение поддерживает Windows Vista с пакетом обновления 2 (sp2), а также Windows 7 и Windows 8 и более поздних версий, установите определение препроцессора с именем **\_ WIN32 \_ WINNT** в 0x600. если он поддерживает только Windows 7 и Windows 8 и более поздних версий, задайте для него значение 0x601.

    Пример.

    1.  Откройте **Свойства** проекта и выберите Препроцессор **C/C++**  >  .
    2.  Выберите **все конфигурации** и **все платформы**.
    3.  Перейдите в раздел **определений препроцессора** и задайте \_ Win32 \_ WinNT = 0x600.
    4.  Щелкните **Применить**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Записи блога, посвященные играм для Windows и DirectX SDK**
</dt> <dt>

[Где находится пакет SDK DirectX (выпуск 2021)?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[Пакеты SDK DirectX определенного возраста](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Жить без D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
