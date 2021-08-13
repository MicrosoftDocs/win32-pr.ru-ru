---
description: В этом примере демонстрируется декодирование различных кадров в файле GIF, чтение соответствующих метаданных для каждого кадра, составление кадров и визуализация анимации с помощью Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Пример анимированного GIF-файла WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 925beb45b58bdecb7d12505a9d2067cbcb9e6fbf1867786286f18333fea986e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709608"
---
# <a name="wic-animated-gif-sample"></a>Пример анимированного GIF-файла WIC

В этом примере демонстрируется декодирование различных кадров в файле GIF, чтение соответствующих метаданных для каждого кадра, составление кадров и визуализация анимации с помощью Direct2D.

## <a name="requirements"></a>Requirements (Требования)

Этот пример имеет следующие требования.

| Требование | Значение |
|-|-|
| Минимальная версия клиента | Windows 7 |
| минимальное Windows SDK | [пакет средств разработки программного обеспечения (SDK) для Windows 7 (Windows)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |

## <a name="downloading-the-sample"></a>Скачивание примера

Этот пример доступен на [анимированном GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif)-файле WIC.

## <a name="building-the-sample"></a>Создание примера

### <a name="using-visual-studio-preferred-method"></a>использование Visual Studio (предпочтительный метод)

1. Откройте проводник и перейдите к каталогу.
2. Дважды щелкните значок файла. sln (решение), чтобы открыть файл в Visual Studio.
3. В меню **Построение** выберите команду **Построить решение**. Приложение будет построено в \\ каталоге отладки или выпуска по умолчанию \\ .

### <a name="using-the-command-prompt"></a>Использование командной строки

Построение образца с помощью командной строки.

1. Откройте командную строку и перейдите к каталогу примеров.
2. Введите `msbuild WICAnimatedGif.sln`

## <a name="running-the-sample"></a>Выполнение примера

После запуска приложения Загрузите файл образа с помощью команды **Открыть** в меню **файл** . Изменение размера окна поддерживается.

## <a name="see-also"></a>См. также раздел

[кодек Microsoft Windows imaging](-wic-lh.md)

[Руководство по программированию](-wic-programming-guide.md)

[Ссылки](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Примеры и примеры кода](-wic-samples.md)
