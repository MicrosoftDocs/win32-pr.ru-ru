---
description: В этом примере демонстрируется декодирование различных кадров в файле GIF, чтение соответствующих метаданных для каждого кадра, составление кадров и визуализация анимации с помощью Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Пример анимированного GIF-файла WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105651568"
---
# <a name="wic-animated-gif-sample"></a>Пример анимированного GIF-файла WIC

В этом примере демонстрируется декодирование различных кадров в файле GIF, чтение соответствующих метаданных для каждого кадра, составление кадров и визуализация анимации с помощью Direct2D.

## <a name="requirements"></a>Требования

Этот пример имеет следующие требования.

| Требование | Значение |
|-|-|
| Минимальная версия клиента | Windows 7 |
| Минимальное Windows SDK | [Пакет средств разработки программного обеспечения (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) для Windows 7 |

## <a name="downloading-the-sample"></a>Скачивание примера

Этот пример доступен на [анимированном GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif)-файле WIC.

## <a name="building-the-sample"></a>Создание примера

### <a name="using-visual-studio-preferred-method"></a>Использование Visual Studio (предпочтительный метод)

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

[Кодек Microsoft Windows Imaging](-wic-lh.md)

[Руководство по программированию](-wic-programming-guide.md)

[Ссылки](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Примеры и примеры кода](-wic-samples.md)
