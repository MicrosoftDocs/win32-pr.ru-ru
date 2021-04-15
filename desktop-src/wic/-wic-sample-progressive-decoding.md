---
description: В этом примере демонстрируется использование компонента Windows Imaging Component (WIC) для декодирования изображения, закодированного с помощью последовательных уровней.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Пример прогрессивного декодирования компонента WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105714073"
---
# <a name="wic-progressive-decoding-sample"></a>Пример прогрессивного декодирования компонента WIC

В этом примере демонстрируется использование компонента Windows Imaging Component (WIC) для декодирования изображения, закодированного с помощью последовательных уровней. В этом примере используется Direct2D для отображения различных последовательных уровней на экране.

## <a name="requirements"></a>Требования

Этот пример имеет следующие требования.

| Требование | Значение |
|-|
| Минимальная версия клиента | Windows 7 |
| Минимальное Windows SDK | [Пакет средств разработки программного обеспечения (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) для Windows 7 |

## <a name="downloading-the-sample"></a>Скачивание примера

Этот пример доступен в [прогрессивной кодировке WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).

## <a name="building-the-sample"></a>Создание примера

### <a name="using-visual-studio-preferred-method"></a>Использование Visual Studio (предпочтительный метод)

1. Откройте проводник и перейдите к каталогу.
2. Дважды щелкните значок файла. sln (решение), чтобы открыть файл в Visual Studio.
3. В меню Построение выберите команду Построить решение. Приложение будет построено в \\ каталоге отладки или выпуска по умолчанию \\ .

### <a name="using-the-command-prompt"></a>Использование командной строки

Для построения примера с помощью командной строки.

1. Откройте командную строку и перейдите к каталогу примеров.
2. Введите `msbuild WICProgressiveDecoding.sln`

## <a name="running-the-sample"></a>Выполнение примера

После запуска приложения Загрузите файл изображения через меню открыть файл. При загрузке для последовательного уровня по умолчанию устанавливается значение 0. Переход к различным последовательным уровням можно осуществлять с помощью меню или клавиши со стрелками вверх или вниз. Текущий текст последовательного уровня отображается в строке состояния главного окна. Изменение размера окна поддерживается.

> [!NOTE]
> Прогрессивное декодирование доступно только для образов с последовательной кодировкой. Образ, предоставленный в этом примере, был постепенно закодирован.

## <a name="see-also"></a>См. также раздел

[Кодек Microsoft Windows Imaging](-wic-lh.md)

[Руководство по программированию](-wic-programming-guide.md)

[Ссылки](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Примеры и примеры кода](-wic-samples.md)

[Обзор прогрессивного декодирования](-wic-progressive-decoding.md)
