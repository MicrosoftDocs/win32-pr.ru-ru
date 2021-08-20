---
description: Реализация Ивикдевелоправ
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Реализация Ивикдевелоправ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68a78705fcfb53651d1099d01d17d9ddff554df9632a5cc322db229bc04d38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965013"
---
# <a name="implementing-iwicdevelopraw"></a>Реализация Ивикдевелоправ

## <a name="iwicdevelopraw"></a>ивикдевелоправ

Интерфейс [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) предоставляет параметры обработки, характерные для обработки необработанных изображений. Все необработанные кодеки должны поддерживать интерфейс **ивикдевелоправ** . Некоторые кодеки необработанных кодеков могут не поддерживать каждый параметр, предоставленный этим интерфейсом, но вы должны поддерживать все параметры, которые может выполнять кодек. Как минимум каждый кодек RAW должен реализовывать методы [**сетротатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) и [**сетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .

Кроме того, для необработанных кодеков настоятельно рекомендуется использовать некоторые методы и интерфейсы, которые являются необязательными для других кодеков. К ним [**относятся методы**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) [**OnPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) и ивикбитмапсаурцетрансформ в классе декодера уровня контейнера, а также интерфейс [](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) для класса декодирования на уровне кадров.

Параметры задается с помощью методов [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , должны сохраняться кодеком так, чтобы они соответствовали способу сохранения других метаданных, но не следует перезаписывать исходные параметры "как". Путем сохранения метаданных и реализации [**лоадпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) и [**жеткуррентпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)вы включаете приложения обработки необработанных приложений для извлечения и применения параметров обработки в сеансах.

Основным назначением интерфейса [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) является предоставление разработчикам приложений возможности создавать пользовательский интерфейс для настройки необработанных параметров, которые будут работать как можно одинаково в разных кодеках. Предположим, что конечный пользователь настроит параметры с помощью ползунка с минимальным и максимальным значениями, сопоставленными с минимальным и максимальным диапазонами для параметра. Для поддержки этой ситуации следует сделать все усилия, чтобы все диапазоны параметров считались линейными. Чтобы элементы управления "ползунок" не были избыточно конфиденциальными, необходимо также поддерживать как можно более широкий диапазон для каждого параметра, охватывающий по крайней мере 50 процентов от максимально возможного диапазона. Например, если максимально возможный диапазон контрастов находится в диапазоне от чисто серого до чисто черного и белого, а значение по умолчанию сопоставляется с 0,0, минимальный диапазон, поддерживаемый кодеком, будет иметь размер не менее половины между значением по умолчанию и чистым серым в нижней части (– 1,0), по меньшей мере на половину между значением по умолчанию и чистым черным и белым в верхней 1,0


```C++
interface IWICDevelopRaw : IWICBitmapFrameDecode
{
   HRESULT QueryRawCapabilitiesInfo ( WICRawCapabilitiesInfo *pInfo );
   HRESULT LoadParameterSet ( WICRawParameterSet ParameterSet );
   HRESULT GetCurrentParameterSet ( IPropertyBag2 **ppCurrentParameterSet );
   HRESULT SetExposureCompensation ( double ev );
   HRESULT GetExposureCompensation ( double *pEV );
   HRESULT SetWhitePointRGB ( UINT Red, UINT Green, UINT Blue );
   HRESULT GetWhitePointRGB ( UINT *pRed, UINT *pGreen, UINT *pBlue );
   HRESULT SetNamedWhitePoint ( WICNamedWhitePoint WhitePoint );
   HRESULT GetNamedWhitePoint ( WICNamedWhitePoint *pWhitePoint );
   HRESULT SetWhitePointKelvin ( UINT WhitePointKelvin );
   HRESULT GetWhitePointKelvin ( UINT *pWhitePointKelvin );
   HRESULT GetKelvinRangeInfo ( UINT *pMinKelvinTemp,
               UINT *pMaxKelvinTemp,
               UINT *pKelvinTempStepValue );
   HRESULT SetContrast ( double Contrast );
   HRESULT GetContrast ( double *pContrast );
   HRESULT SetGamma ( double Gamma );
   HRESULT GetGamma ( double *pGamma );
   HRESULT SetSharpness ( double Sharpness );
   HRESULT GetSharpness ( double *pSharpness );
   HRESULT SetSaturation ( double Saturation );
   HRESULT GetSaturation ( double *pSaturation );
   HRESULT SetTint ( double Tint );
   HRESULT GetTint ( double *pTint );
   HRESULT SetNoiseReduction ( double NoiseReduction );
   HRESULT GetNoiseReduction ( double *pNoiseReduction );
   HRESULT SetDestinationColorContext (const IWICColorContext *pColorContext );
   HRESULT SetToneCurve ( UINT cbToneCurveSize,
               const WICRawToneCurve *pToneCurve );
   HRESULT GetToneCurve ( UINT cbToneCurveBufferSize,
               WICRawToneCurve *pToneCurve,
               UINT *pcbActualToneCurveBufferSize );
   HRESULT SetRotation ( double Rotation );
   HRESULT GetRotation ( double *pRotation );
   HRESULT SetRenderMode ( WICRawRenderMode RenderMode );
   HRESULT GetRenderMode ( WICRawRenderMode *pRenderMode ); 
   HRESULT SetNotificationCallback ( IWICDevelopRawNotificationCallback 
               *pCallback );
}
```



-   [куериравкапабилитиесинфо](#queryrawcapabilitiesinfo)
-   [лоадпараметерсет](#loadparameterset)
-   [жеткуррентпараметерсет](#getcurrentparameterset)
-   [Set/Жетекспосурекомпенсатион](#setgetexposurecompensation)
-   [Set/Жеткуррентпараметерргб, Set/Жетнамедвхитепоинт, Set/Жетвхитепоинткелвин](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/контрастность](#setgetcontrast)
-   [Set/-гамма](#setgetgamma)
-   [Set/диез](#setgetsharpness)
-   [Задание/перенасыщенность](#setgetsaturation)
-   [Set/-тонированный](#setgettint)
-   [Set/Жетноисередуктион](#setgetnoisereduction)
-   [сетдестинатионколорконтекст](#setdestinationcolorcontext)
-   [Set/Жеттонекурве](#setgettonecurve)
-   [Задание/вращение](#setgetrotation)
-   [Set/Жетрендермоде](#setgetrendermode)
-   [сетнотификатионкаллбакк](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>куериравкапабилитиесинфо

[**Куериравкапабилитиесинфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) возвращает набор поддерживаемых возможностей для этого необработанного файла. Структура [**викравкапабилитиесинфо**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) определяется следующим образом:


```C++
struct WICRawCapabilitiesInfo
{
   UINT cbSize;
   UINT CodecMajorVersion;
   UINT CodecMinorVersion;
   WICRawCapabilities ExposureCompensationSupport;
   WICRawCapabilities ContrastSupport;
   WICRawCapabilities RGBWhitePointSupport;
   WICRawCapabilities NamedWhitePointSupport;
   UINT NamedWhitePointSupportMask;
   WICRawCapabilities KelvinWhitePointSupport;
   WICRawCapabilities GammaSupport;
   WICRawCapabilities TintSupport;
   WICRawCapabilities SaturationSupport;
   WICRawCapabilities SharpnessSupport;
   WICRawCapabilities NoiseReductionSupport;
   WICRawCapabilities DestinationColorProfileSupport;
   WICRawCapabilities ToneCurveSupport;
   WICRawRotationCapabilities RotationSupport;              
}
```



Перечисление [**викравкапабилитиес**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) , используемое в этой структуре, определяется следующим образом:


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



Последним полем является перечисление [**викравротатионкапабилитиес**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , определенное следующим образом:


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a>лоадпараметерсет

[**Лоадпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) позволяет пользователю указать, следует ли использовать в качестве параметров снимка, использовать настроенные пользователем параметры или запросить автоматическое исправление образа в декодере.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>жеткуррентпараметерсет

[**Жеткуррентпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) возвращает **IPropertyBag2** с текущим набором параметров. Затем вызывающий объект может передать этот набор параметров кодировщику для использования в качестве параметров кодировщика.

### <a name="setgetexposurecompensation"></a>Set/Жетекспосурекомпенсатион

[**Жетекспосурекомпенсатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) и [**сетекспосурекомпенсатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) указывают компенсацию экспозиции, применяемую к окончательному выходу. Допустимый диапазон для EV — от – 5,0 до + 5,0.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/Жеткуррентпараметерргб, Set/Жетнамедвхитепоинт, Set/Жетвхитепоинткелвин

Все эти функции предоставляют способы получения и задания белого пункта как значения RGB, предустановки именованного значения или в качестве значения Кельвина. Допустимый диапазон для Кельвина — 1 500 – 30 000.

### <a name="setgetcontrast"></a>Set/контрастность

Параметр " [**контрастность**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) " и [**сетконтраст**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) указывает степень контрастности, применяемую к выходным данным. Допустимый диапазон для указания контрастности — от – 1,0 до + 1,0, а контраст по умолчанию — 0,0.

### <a name="setgetgamma"></a>Set/-гамма

Параметр [**сетгамма**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) указывает гамму [**, которую**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) необходимо применить. Допустимый диапазон для гаммы — 0,2 – 5,0, значение по умолчанию — 1,0. Гамма обычно реализуется с помощью традиционной функции гаммы-коррекции мощности (линейная функция питания с помощью Unity). Яркость увеличивается с увеличением гамма и уменьшается при приближении к нулевому гамме. (Обратите внимание, что минимальное значение не равно нулю, поскольку ноль приведет к ошибке деления на ноль в традиционных вычислениях гаммы. Логический минимальный предел — 1/Max, поэтому минимальное значение — 0,2.)

### <a name="setgetsharpness"></a>Set/диез

[**Четкость**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) и [**сетшарпнесс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) указывают объем данных, которые нужно применить. Допустимый диапазон — от – 1,0 до + 1,0, где 0,0 — это значение по умолчанию, а – 1,0, указывающее на отсутствие резкости.

### <a name="setgetsaturation"></a>Задание/перенасыщенность

Параметр [**сетсатуратион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) указывает степень насыщенности [**, которую**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) необходимо применить. Допустимый диапазон для указания насыщенности — от – 1,0 до + 1,0, а 0,0 — нормальная насыщенность, – 1,0 представляет полную раснасыщенность, а + 1,0 — полную насыщенность.

### <a name="setgettint"></a>Set/-тонированный

Параметр [**сеттинт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) указывает, какой [**оттенок следует**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) применить, с зеленым или пурпурным смещением. Допустимый диапазон — от – 1,0 до + 1,0, зеленый — на отрицательной стороне шкалы и пурпурный на положительном. Шкала оттенков определяется как ортогональная цветовая температура.

### <a name="setgetnoisereduction"></a>Set/Жетноисередуктион

[**Жетноисередуктион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) и [**сетноисередуктион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) указывают объем применяемого снижения шума. Допустимый диапазон — от – 1,0 до + 1,0, с 0,0, указывающим значение по умолчанию для снижения шума, – 1,0, указывающее на отсутствие шума и + 1,0, указывающее на максимальное снижение шума.

### <a name="setdestinationcolorcontext"></a>сетдестинатионколорконтекст

[**Сетдестинатионколорконтекст**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) указывает цветовой профиль, применяемый к изображению. Для получения текущего цветового профиля можно вызвать [**жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) .

### <a name="setgettonecurve"></a>Set/Жеттонекурве

[**Жеттонекурве**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) и [**сеттонекурве**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) определяют применяемую кривую тона. Предположим линейную интерполяцию между точками. **Птонекурве** — это структура [**викравтонекурве**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) , которая содержит массив структур [**викравтонекурвепоинт**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) и количество точек в массиве.


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



[**Викравтонекурвепоинт**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) содержит входное значение и выходное значение.


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



Когда вызывающий объект передает **значение NULL** в параметре *птонекурве* , необходимо передать обратно необходимый размер для [**викравтонекурве**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) в параметре *пкбактуалтонекурвебуфферсизе* .

### <a name="setgetrotation"></a>Задание/вращение

[**Вращение**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) и [**сетротатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) указывают степень поворота для применения. При повороте 90,0 будет задан поворот на 90 градусов по часовой стрелке. (Разница между использованием **сетротатион** и заданием вращения с помощью метода [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) заключается в том, что угол поворота, заданный с помощью **сетротатион** , должен сохраняться кодеком, а установка вращения через **CopyPixels** только поворачивает изображение в памяти.

### <a name="setgetrendermode"></a>Set/Жетрендермоде

[**Жетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) и [**сетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) указывают уровень качества выходных данных, необходимых вызывающему объекту. Когда пользователь настраивает параметры, в приложении должно отображаться очень быстрое приближение того, как будет выглядеть фактический образ при применении изменений. Для этой цели изображение обычно отображается при разрешении экрана или меньше, а не на фактическом разрешении изображения, чтобы обеспечить немедленную отклики пользователя. Это происходит, когда приложение запрашивает качество режима черновика, поэтому это должно быть очень быстрым. Когда пользователь внес все изменения, просматривает их в режиме черновика и решил декодировать полное изображение с текущими параметрами, приложение запрашивает оптимальное качество расшифровки. Обычно это также требуется для печати. Если требуется разумное компромиссное качество, приложение запрашивает нормальное качество.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>сетнотификатионкаллбакк

[**Сетнотификатионкаллбакк**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) регистрирует функцию обратного вызова для вызова декодера при изменении любого из параметров обработки необработанных данных. Сигнатура для [**ивикдевелоправнотификатионкаллбакк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) имеет только один метод, именуемый [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify). **Notify** имеет единственный параметр — маску, указывающую, какие из параметров обработки необработанных данных были изменены.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Операция OR выполняется для следующих значений Нотификатионмаск.


```C++
WICRawChangeNotification_ExposureCompensation
WICRawChangeNotification_NamedWhitePoint
WICRawChangeNotification_KelvinWhitePoint
WICRawChangeNotification_RGBWhitePoint
WICRawChangeNotification_Contrast
WICRawChangeNotification_Gamma
WICRawChangeNotification_Sharpness
WICRawChangeNotification_Saturation
WICRawChangeNotification_Tint
WICRawChangeNotification_NoiseReduction
WICRawChangeNotification_DestinationColorContext
WICRawChangeNotification_ToneCurve
WICRawChangeNotification_Rotation
WICRawChangeNotification_RenderMode
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

**Зрения**
</dt> <dt>

[Реализация Ивикбитмапсаурцетрансформ](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Реализация кодировщика WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



