---
title: Автономная компиляция
description: Средство компилятора Effect (fxc.exe) предназначено для автономной компиляции шейдеров HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- fxc, Автономная компиляция
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c2bf96a24cb586a5d229a395cbf6dc0cb9ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793584"
---
# <a name="offline-compiling"></a><span data-ttu-id="b96ba-104">Автономная компиляция</span><span class="sxs-lookup"><span data-stu-id="b96ba-104">Offline compiling</span></span>

<span data-ttu-id="b96ba-105">Средство компилятора Effect (fxc.exe) предназначено для автономной компиляции шейдеров HLSL.</span><span class="sxs-lookup"><span data-stu-id="b96ba-105">The effect-compiler tool (fxc.exe) is designed for offline compilation of HLSL shaders.</span></span>

## <a name="compiling-with-the-current-compiler"></a><span data-ttu-id="b96ba-106">Компиляция с текущим компилятором</span><span class="sxs-lookup"><span data-stu-id="b96ba-106">Compiling with the current compiler</span></span>

<span data-ttu-id="b96ba-107">Модели шейдеров, поддерживаемые текущим компилятором, отображаются в [профилях](dx-graphics-tools-fxc-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b96ba-107">The shader models supported by the current compiler are shown in [Profiles](dx-graphics-tools-fxc-syntax.md).</span></span> <span data-ttu-id="b96ba-108">В этом примере компилируется шейдер пикселей для целевого объекта модели шейдера 5,1.</span><span class="sxs-lookup"><span data-stu-id="b96ba-108">This example compiles a pixel shader for the shader model 5.1 target.</span></span>

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="b96ba-109">В этом примере:</span><span class="sxs-lookup"><span data-stu-id="b96ba-109">In this example:</span></span>

-   <span data-ttu-id="b96ba-110">PS \_ 5 \_ 1 является целевым профилем.</span><span class="sxs-lookup"><span data-stu-id="b96ba-110">ps\_5\_1 is the target profile.</span></span>
-   <span data-ttu-id="b96ba-111">PixelShader1. fxc — выходной объектный файл, содержащий скомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="b96ba-111">PixelShader1.fxc is the output object file containing the compiled shader.</span></span>
-   <span data-ttu-id="b96ba-112">PixelShader1. HLSL является источником.</span><span class="sxs-lookup"><span data-stu-id="b96ba-112">PixelShader1.hlsl is the source.</span></span>

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="b96ba-113">Параметры отладки включают дополнительные параметры для отключения оптимизации компилятора (OD) и включения отладочных данных (Zi), таких как номера строк и символы.</span><span class="sxs-lookup"><span data-stu-id="b96ba-113">The debug options include additional options to disable compiler optimizations (Od) and enable debug information (Zi) like line numbers and symbols.</span></span>

<span data-ttu-id="b96ba-114">Полный список параметров командной строки см. на странице [синтаксис](dx-graphics-tools-fxc-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="b96ba-114">For a full listing of the command-line options, see the [Syntax](dx-graphics-tools-fxc-syntax.md) page.</span></span>

## <a name="compiling-with-the-legacy-compiler"></a><span data-ttu-id="b96ba-115">Компиляция с использованием устаревшего компилятора</span><span class="sxs-lookup"><span data-stu-id="b96ba-115">Compiling with the legacy compiler</span></span>

<span data-ttu-id="b96ba-116">Начиная с Direct3D 10, некоторые модели шейдеров больше не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b96ba-116">Beginning with Direct3D 10, some shader models are no longer supported.</span></span> <span data-ttu-id="b96ba-117">К ним относятся модели шейдеров пикселей: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 и PS \_ 1 \_ 4, которые поддерживают очень ограниченные ресурсы и зависят от оборудования.</span><span class="sxs-lookup"><span data-stu-id="b96ba-117">These include pixel shader models: ps\_1\_1, ps\_1\_2, ps\_1\_3, and ps\_1\_4 which support very limited resources and are dependent on hardware.</span></span> <span data-ttu-id="b96ba-118">Компилятор был переработан с помощью шейдера модели 2 (или более поздней версии), что позволяет повысить эффективность компиляции.</span><span class="sxs-lookup"><span data-stu-id="b96ba-118">The compiler has been redesigned with shader model 2 (or greater) which allows for greater efficiencies with compilation.</span></span> <span data-ttu-id="b96ba-119">Для этого курса потребуется использовать оборудование, которое поддерживает модели шейдеров 2 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="b96ba-119">This of course will require that you are running on hardware that supports shader models 2 and greater.</span></span>

<span data-ttu-id="b96ba-120">Кроме того, обратите внимание на заметки о выпуске пакета SDK, связанные с вашей версией компилятора FXC, для поведения, затронутого параметром/жек.</span><span class="sxs-lookup"><span data-stu-id="b96ba-120">Also note that you should consult the SDK release notes associated with your version of the FXC compiler for behavior affected by the /Gec switch.</span></span>

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a><span data-ttu-id="b96ba-121">Использование средства компилятора Effect в подпроцессах</span><span class="sxs-lookup"><span data-stu-id="b96ba-121">Using the effect-compiler tool in a subprocess</span></span>

<span data-ttu-id="b96ba-122">Если fxc.exe порождается приложением как подпроцесс, важно убедиться, что приложение проверяет наличие и считывает данные в выходных данных или каналах ошибок, переданных в функцию CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="b96ba-122">If fxc.exe is spawned as a subprocess by an application it is important to ensure that the application checks for and reads any data in output or error pipes passed to the CreateProcess function.</span></span> <span data-ttu-id="b96ba-123">Если приложение ожидает завершения подпроцесса и один из каналов становится заполненным, подпроцесс никогда не завершится.</span><span class="sxs-lookup"><span data-stu-id="b96ba-123">If the application only waits for the subprocess to finish and one of the pipes becomes full the subprocess will never finish.</span></span>

<span data-ttu-id="b96ba-124">В следующем примере кода показано ожидание подпроцесса и считывание выходных данных и каналов ошибок, прикрепленных к подпроцессу.</span><span class="sxs-lookup"><span data-stu-id="b96ba-124">The following example code illustrates waiting on a subprocess and reading the output and error pipes attached to the subprocess.</span></span> <span data-ttu-id="b96ba-125">Содержимое `WaitHandles` массива соответствует дескрипторам подпроцесса, каналу stdout и каналу для stderr.</span><span class="sxs-lookup"><span data-stu-id="b96ba-125">The contents of the `WaitHandles` array correspond to handles for the subprocess, the pipe for stdout and the pipe for stderr.</span></span>

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

<span data-ttu-id="b96ba-126">Дополнительные сведения об порождении процесса см. на странице справки по [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="b96ba-126">For additional information on spawning a process see the reference page for [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b96ba-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b96ba-127">Related topics</span></span>

* [<span data-ttu-id="b96ba-128">Effect — средство компилятора</span><span class="sxs-lookup"><span data-stu-id="b96ba-128">Effect-Compiler Tool</span></span>](fxc.md)