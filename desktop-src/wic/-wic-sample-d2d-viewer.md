---
description: В этом примере демонстрируется использование компонента Windows Imaging Component (WIC) для декодирования файла изображения и Direct2D для отображения изображения на экране.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Средство просмотра изображений WIC с использованием примера Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105651567"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a>Средство просмотра изображений WIC с использованием примера Direct2D

В этом примере демонстрируется использование компонента Windows Imaging Component (WIC) для декодирования файла изображения и Direct2D для отображения изображения на экране.

## <a name="requirements"></a>Требования

Этот пример имеет следующие требования.

| Требование | Значение |
|-|-|
| Минимальная версия клиента | Windows Vista |
| Минимальное Windows SDK | [Пакет средств разработки программного обеспечения (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) для Windows 7 |

## <a name="downloading-the-sample"></a>Скачивание примера

Этот образец доступен в [средстве просмотра WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).

## <a name="building-the-sample"></a>Создание примера

### <a name="using-visual-studio-preferred-method"></a>Использование Visual Studio (предпочтительный метод)

1. Откройте проводник и перейдите к каталогу.
2. Дважды щелкните значок файла. sln (решение), чтобы открыть файл в Visual Studio.
3. В меню **Построение** выберите команду **Построить решение**. Приложение будет построено в \\ каталоге отладки или выпуска по умолчанию \\ .

### <a name="using-the-command-prompt"></a>Использование командной строки

Чтобы построить пример с помощью командной строки, выполните следующую команду:

1. Откройте окно командной строки и перейдите к каталогу примеров.
2. Введите `msbuild WICViewerD2D.sln`

## <a name="running-the-sample"></a>Выполнение примера

После запуска приложения Загрузите файл изображения с помощью команды **Открыть** в меню **файл** .

## <a name="see-also"></a>См. также раздел

[Кодек Microsoft Windows Imaging](-wic-lh.md)

[Руководство по программированию](-wic-programming-guide.md)

[Ссылки](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Примеры и примеры кода](-wic-samples.md)
