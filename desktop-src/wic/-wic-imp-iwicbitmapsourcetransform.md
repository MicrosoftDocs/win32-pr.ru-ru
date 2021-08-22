---
description: Реализация Ивикбитмапсаурцетрансформ
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Реализация Ивикбитмапсаурцетрансформ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79caa17fdb874b9cbee73a9a371c4ba454e72c6eb249a6ca7d626fdd9c86aea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711079"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>Реализация Ивикбитмапсаурцетрансформ

## <a name="iwicbitmapsourcetransform"></a>ивикбитмапсаурцетрансформ

Хотя это необязательно, настоятельно рекомендуется, чтобы каждый декодер реализовал этот интерфейс для класса декодирования на уровне кадров, так как он может предоставить значительные преимущества для повышения производительности. когда приложение запрашивает конкретный регион, размер, ориентацию или формат пикселей, вместо простого декодирования всего изображения при полном разрешении, а затем применения запрошенных преобразований, Windows компонент обработки изображений (WIC) вызывает [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для этого интерфейса в объекте [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . Если декодер кадров поддерживает его, то WIC вызывает соответствующий метод или методы, чтобы определить, может ли декодер кадров выполнить запрошенное преобразование, или определить ближайший размер или формат пикселей, который декодер может предоставить для запрошенного. Если декодер может выполнить запрошенное преобразование или преобразования, WIC вызывает [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) с соответствующими параметрами. Если декодер может выполнять некоторые, но не все запрошенные преобразования, WIC запрашивает у декодера, что они могут, и использует объекты преобразования WIC ([**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)и [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) для выполнения оставшихся преобразований, которые не могут быть выполнены декодером кадров в результате вызова **CopyPixels** . Если декодер не поддерживает [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), компонент WIC должен использовать объекты Transform для выполнения всех преобразований. Обычно гораздо эффективнее сделать так, чтобы декодер выполнял преобразования в процессе декодирования, чем декодировать все изображение, а затем выполнять преобразования. Это особенно справедливо для таких операций, как масштабирование до значительно меньшего размера или преобразований формата пикселей.


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [доессуппорттрансформ](#doessupporttransform)
-   [CopyPixels](#copypixels)
-   [жетклосестсизе](#getclosestsize)
-   [жетклосестпикселформат](#getclosestpixelformat)

### <a name="doessupporttransform"></a>доессуппорттрансформ

[**Доессуппорттрансформ**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) спрашивает, поддерживает ли декодер запрошенную операцию вращения или зеркального отражения. [**Викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) , которые могут быть запрошены:


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) выполняет фактическую работу декодирования битов изображения, например метода [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) в интерфейсе [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , но метод [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) в [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) является гораздо более мощным и может значительно повысить производительность обработки изображений.

При запросе нескольких операций преобразования результат зависит от порядка, в котором выполняются операции. Чтобы обеспечить предсказуемость и согласованность в кодеках, важно, чтобы все кодеки выполняли эти операции в том же порядке. Это канонический порядок выполнения этих операций.

1.  Масштабирование
2.  Crop
3.  Rotate

Преобразование формата пикселей можно выполнить в любое время, так как оно не влияет на другие преобразования.

Первый параметр, *прксрк*, используется для указания области интересов для обрезки изображения. Поскольку масштабирование выполняется до усечения по соглашению, если изображение должно масштабироваться, а также обрезано, необходимо определить интересующую область после масштабирования изображения.

Второй и третий параметры указывают размер, до которого будет масштабироваться изображение.

Параметр *пгуиддстформат* указывает запрошенный формат пикселей для декодированного изображения. Так как WIC уже вызвал [**жетклосестпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), это должен быть формат пикселей, который декодер указал, что он поддерживает.

Параметр *дсттрансформ* указывает запрошенный угол вращения и необходимость перелистывания изображения по вертикали, горизонтали или обоим. Опять же, поскольку компонент WIC уже назывался [**доессуппорттрансформ**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), запрошенное преобразование должно быть одним, что декодер уже указал, что он поддерживает. Помните, что вращение всегда должно выполняться после масштабирования и обрезки.

### <a name="getclosestsize"></a>жетклосестсизе

[**Жетклосестсизе**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) принимает два параметра in/out. Вызывающий объект использует параметры *пуивидс* и *пуихеигхт* для указания размера, в котором вызывающий объект предпочитает декодировать изображение. Однако декодер может декодировать изображение только до размера, кратного размеру его ДКТ, а различные форматы изображений могут иметь различные размеры ДКТ. Декодер должен определить, на основе собственного размера ДКТ, ближайший к запрошенному размеру, и установить для этих измерений *пуивидс* и *пуихеигхт* . Если запрашивается больший размер, но кодек не поддерживает масштабирование, исходный объект должен быть возвращен.

### <a name="getclosestpixelformat"></a>жетклосестпикселформат

[**Жетклосестпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) используется для определения наиболее близкого формата пикселей к запрошенному формату пикселей, который декодер может предоставить без потери данных. Всегда рекомендуется преобразовывать в более широкий формат пикселей, чем на более узкую, несмотря на увеличение размера изображения, поскольку при необходимости его всегда можно преобразовать в более ограничивающий формат. Однако после потери данных восстановить их будет невозможно.

## <a name="continued-reading"></a>Продолжение чтения

Дополнительные сведения о создании кодеков с поддержкой WIC см. в разделе [Реализация ивикдевелоправ](-wic-imp-iwicdevelopraw.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Зрения**
</dt> <dt>

[Реализация Ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Реализация Ивикдевелоправ](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
