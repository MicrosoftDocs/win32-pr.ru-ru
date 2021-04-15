---
title: Указание ресурсов изображения ленты
description: В качестве обширной системы представления команд платформа Windows Ribbon разработана для обеспечения широкого спектра графических ресурсов на протяжении всего пользовательского интерфейса ленты. Все ресурсы изображений объявляются в разметке ленты или запрашиваются из хост-приложения ленты.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Лента Windows, ресурсы изображений
- Лента, ресурсы изображений
- Лента Windows, прозрачность
- Лента, прозрачность
- Лента Windows, глубина цвета
- Лента, глубина цвета
- Лента Windows, контрастность
- Лента, контрастность
- ресурсы изображений на ленте Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488124"
---
# <a name="specifying-ribbon-image-resources"></a>Указание ресурсов изображения ленты

В качестве обширной системы представления команд платформа Windows Ribbon разработана для обеспечения широкого спектра графических ресурсов на протяжении всего пользовательского интерфейса ленты. Все ресурсы изображений объявляются в [разметке ленты](windowsribbon-schema.md) или запрашиваются из хост-приложения ленты.

Для Windows 8 и более поздних версий платформа Ribbon поддерживает следующие форматы графики: 32-битовые растровые файлы ARGB (BMP) и PNG-файлы с прозрачностью.

Для Windows 7 и более ранних версий ресурсы образа должны соответствовать стандартному графическому формату BMP, используемому в Windows.

> [!Note]  
> Если платформе предоставляется неподдерживаемый формат изображения, может возникнуть ошибка компиляции.

 

## <a name="image-sizes"></a>Размеры изображений

Чтобы обеспечить большую гибкость для макетов элементов управления ленты при изменении размера окна приложения, платформа Ribbon принимает и визуализирует изображения в одном из двух размеров: крупный или маленький.

На следующих рисунках показано приложение ленты, которое поддерживает несколько размеров ленты с помощью гибких макетов элементов управления и замены больших изображений с помощью небольших изображений, где они доступны.

На следующем снимке экрана показана лента с большими изображениями для элементов управления масштабом.

![снимок экрана, на котором показана лента, использующая крупные изображения для элементов управления масштабом.](images/overviews/imageresources-largeimage.png)

На следующем снимке экрана показана та же лента с мелкими изображениями для элементов управления масштабом.

![снимок экрана, на котором показана лента, использующая небольшие изображения для элементов управления масштабом.](images/overviews/imageresources-smallimage.png)

На следующем снимке экрана показана лента в скрытом состоянии. Лента скрывается, когда все возможные макеты элементов управления исчерпаны, и лента не может быть подготовлена к использованию рабочей областью приложения.

![снимок экрана, показывающий свернутую ленту.](images/overviews/imageresources-noimage.png)

Для любого изображения точный размер пикселя зависит от разрешения экрана или от точек на дюйм (DPI) используемого монитора. При 96 dpi крупные изображения имеют размер 32x32 пикселя, а небольшие — 16x16 пикселей в размере. Размеры изображений увеличиваются в линейной манере относительно dpi, как показано в следующей таблице.



| DPI     | Небольшое изображение  | Большое изображение  |
|---------|--------------|--------------|
| 96 точек на дюйм  | 16x16 пикселей | 32x32 пикселя |
| 120 точек на дюйм | 20x20 пикселей | 40x40 пикселей |
| 144 точек на дюйм | 24x24 пикселей | 48x48 пикселей |
| 192 точек на дюйм | 32x32 пикселя | 64 x 64 пикселей |



 

Платформа Ribbon масштабирует ресурсы изображения по мере необходимости. Однако, поскольку изменение размера может привести к нежелательным артефактам и ухудшению изображения, настоятельно рекомендуется, чтобы приложение преддавало небольшой набор графических ресурсов, которые охватывают различные часто используемые параметры dpi. Если точное соответствие не найдено, то ближайшее изображение будет масштабироваться вверх или вниз.

Чтобы упростить это, ресурсы изображения можно объявить в разметке ленты, используя набор элементов [**Image**](windowsribbon-element-image.md) для каждого элемента [**Command**](windowsribbon-element-command.md) . Во время выполнения платформа выбирает изображение для вывода на основе атрибута *миндпи* каждого элемента **Image** .

> [!IMPORTANT]
>
> Если коллекция графических ресурсов, предназначенная для поддержки конкретных параметров dpi на экране, предоставляется для платформы Ribbon через набор элементов [**Image**](windowsribbon-element-image.md) , платформа использует **изображение** со значением атрибута *миндпи* , которое соответствует текущему значению dpi на экране.
>
> Если элемент [**Image**](windowsribbon-element-image.md) не объявлен со значением *миндпи* , совпадающим с текущим параметром dpi на экране, платформа выбирает **изображение** с ближайшим значением *миндпи* , которое меньше текущего значения DPI на экране, и масштабирует ресурс изображения. В противном случае, если ни один из элементов **изображения** не объявлен с атрибутом *миндпи* , значение которого меньше текущего значения DPI экрана, платформа выбирает ближайшее значение *миндпи* , превышающее текущий параметр dpi на экране, и масштабирует ресурс изображения вниз.

 

В следующем примере показано, как объявить набор изображений для размещения различных размеров ленты и системных параметров.


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



Если изображения, объявленные в разметке, становятся недействительными во время выполнения по какой-либо причине, ведущее приложение запрашивает новые образы. Когда эти образы создаются и загружаются программно, приложение должно попытаться вернуть изображения, размер которых изменяется в соответствии с размерами системных значков по умолчанию, определенными [ \_ системным показателем SM кксикон](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).

> [!Note]  
> Крупные образы имеют размер SM \_ кксикон на SM кксикон, \_ а небольшие образы имеют размер SM \_ кксикон/2 на SM \_ кксикон/2.

 

## <a name="color-depth-transparency-and-contrast"></a>Глубина цвета, прозрачность и контрастность

Предполагается, что обычные образы находятся в формате 32 бит на пиксель (бит в пикселах) ARGB и масштабируются до размера значка системы по умолчанию. Этот формат поддерживает как прозрачность, так и сглаживание (по 8 бит на канал).

> [!WARNING]
> Многие инструменты для редактирования изображений не сохраняют самый высокий 8-разрядный канал альфа при загрузке или сохранении образов 32 бит/с.

 

Чтобы изображение отображалось правильно в режиме высокой контрастности, оно должно иметь формат пикселей с размером в 4 пиксела. При отрисовке изображения платформа Ribbon сопоставляет определенные цвета на основе контекста с высокой контрастностью изображения.

В следующей таблице приводится описание поведения платформы с высокой контрастностью для отрисовки цветов.



Цвет пикселя

Значение RGB

Поведение

Белый фон

Темный фон

ЦВЕТ

800080

Прозрачный

Прозрачный

ЭКРАН

000000

ЦВЕТная \_ WINDOWTEXT

Белый

Белый

FFFFFF

\_окно цвета

ЭКРАН

ТЕМНО-СЕРЫЙ

808080

ЦВЕТ \_ 3DSHADOW

ЦВЕТ \_ 3DSHADOW

GRAY

C0C0C0

ЦВЕТ \_ 3DFACE

ЦВЕТ \_ 3DFACE

СВЕТЛО-СЕРЫЙ

дфдфдф

ЦВЕТ \_ 3DLIGHT

ЦВЕТ \_ 3DLIGHT

ТЕМНО-СИНИЙ

000080

Недоступно

Белый



 

Дополнительные сведения о форматах изображений, поддерживаемых платформой Ribbon, см. в следующих статьях:

-   [Структура битмапинфохеадер](/previous-versions//dd183376(v=vs.85)) . описывает формат пикселей ARGB в 32 бит.
-   [Функция креатедибсектион](/windows/win32/api/wingdi/nf-wingdi-createdibsection) — описывает создание изображения формата пикселей ARGB в 32 бит на пиксель.
-   [Функция лоадимаже](/windows/win32/api/winuser/nf-winuser-loadimagea) — описывает, как загрузить изображение формата пикселей ARGB в 32 бит на пиксель.

## <a name="accessibility"></a>Специальные возможности

Использование ресурсов изображений для предоставления информации, передачи функций управления и предоставления состояния приложения увеличивает потребность в требованиях к специальным возможностям во время проектирования и разработки приложений.

Для базовой поддержки высокой контрастности лента позволяет отображать отдельный набор файлов изображений, когда активна тема с высокой контрастностью. Эти изображения могут составлять 32 бит/4 бит, с цветами, сопоставленными с специальной палитрой, в которой темные и легкие цвета инвертированы в зависимости от цвета переднего плана и фона активной темы с высокой контрастностью.

В следующем примере показано, как ресурсы изображения с высокой контрастностью объявляются в разметке ленты.


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Command. Смаллимажес**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[UI \_ PKEY \_ смаллимаже](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**Command. Ларжеимажес**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[UI \_ PKEY \_ ларжеимаже](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**Command. Смаллхигхконтрастимажес**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ смаллхигхконтрастимаже](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**Command. Ларжехигхконтрастимажес**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ ларжехигхконтрастимаже](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 