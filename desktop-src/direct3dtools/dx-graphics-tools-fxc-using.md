---
title: Автономная компиляция
description: Средство компилятора Effect (fxc.exe) предназначено для автономной компиляции шейдеров HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- fxc, Автономная компиляция
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a15d3a71dbfb79541a75bd38cb28140d832b45e75a88a52b2d0c8988865f12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406334"
---
# <a name="offline-compiling"></a>Автономная компиляция

Средство компилятора Effect (fxc.exe) предназначено для автономной компиляции шейдеров HLSL.

## <a name="compiling-with-the-current-compiler"></a>Компиляция с текущим компилятором

Модели шейдеров, поддерживаемые текущим компилятором, отображаются в [профилях](dx-graphics-tools-fxc-syntax.md). В этом примере компилируется шейдер пикселей для целевого объекта модели шейдера 5,1.

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

В этом примере:

-   PS \_ 5 \_ 1 является целевым профилем.
-   PixelShader1. fxc — выходной объектный файл, содержащий скомпилированный шейдер.
-   PixelShader1. HLSL является источником.

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Параметры отладки включают дополнительные параметры для отключения оптимизации компилятора (OD) и включения отладочных данных (Zi), таких как номера строк и символы.

Полный список параметров командной строки см. на странице [синтаксис](dx-graphics-tools-fxc-syntax.md) .

## <a name="compiling-with-the-legacy-compiler"></a>Компиляция с использованием устаревшего компилятора

Начиная с Direct3D 10, некоторые модели шейдеров больше не поддерживаются. К ним относятся модели шейдеров пикселей: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 и PS \_ 1 \_ 4, которые поддерживают очень ограниченные ресурсы и зависят от оборудования. Компилятор был переработан с помощью шейдера модели 2 (или более поздней версии), что позволяет повысить эффективность компиляции. Для этого курса потребуется использовать оборудование, которое поддерживает модели шейдеров 2 и более поздних версий.

Кроме того, обратите внимание на заметки о выпуске пакета SDK, связанные с вашей версией компилятора FXC, для поведения, затронутого параметром/жек.

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>Использование средства компилятора Effect в подпроцессах

Если fxc.exe порождается приложением как подпроцесс, важно убедиться, что приложение проверяет наличие и считывает данные в выходных данных или каналах ошибок, переданных в функцию CreateProcess. Если приложение ожидает завершения подпроцесса и один из каналов становится заполненным, подпроцесс никогда не завершится.

В следующем примере кода показано ожидание подпроцесса и считывание выходных данных и каналов ошибок, прикрепленных к подпроцессу. Содержимое `WaitHandles` массива соответствует дескрипторам подпроцесса, каналу stdout и каналу для stderr.

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

Дополнительные сведения об порождении процесса см. на странице справки по [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).

## <a name="related-topics"></a>Связанные темы

* [Effect — средство компилятора](fxc.md)