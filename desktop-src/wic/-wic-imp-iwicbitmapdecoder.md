---
description: Реализация Ивикбитмапдекодер
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Реализация Ивикбитмапдекодер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080859"
---
# <a name="implementing-iwicbitmapdecoder"></a>Реализация Ивикбитмапдекодер

## <a name="iwicbitmapdecoder"></a>ивикбитмапдекодер

Когда приложение запрашивает декодер, первая точка взаимодействия с кодеком осуществляется через интерфейс [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) . Это интерфейс уровня контейнера, который предоставляет доступ к свойствам верхнего уровня контейнера и, что самое важное, к кадрам, которые он содержит. Это основной интерфейс класса декодера уровня контейнера.

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

Некоторые форматы изображений имеют глобальные эскизы, цветовые контексты или метаданные, а многие форматы изображений предоставляют их только для отдельных кадров. Методы доступа к этим элементам являются необязательными для [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), но требуются для [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Аналогичным образом, некоторые кодеки не используют Индексированные форматы пикселей, поэтому не нужно реализовывать методы [копипалетте](-wic-imp-iwicbitmapframedecode.md) в любом интерфейсе. Дополнительные сведения о необязательных методах **ивикбитмапдекодер** см. в разделе [Реализация IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), где они чаще всего реализуются.

### <a name="querycapability"></a>куерикапабилити

[**Куерикапабилити**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) — это метод, используемый для арбитража кодека. (См. раздел [Обнаружение и арбитраж](-wic-howwicworks.md) в разделе [Working of Windows Imaging Component](-wic-howwicworks.md) . Если два кодека способны декодировать один и тот же формат изображения или если возникает конфликт шаблонов, в котором два кодека используют один и тот же идентифицирующий шаблон, этот метод позволяет выбрать кодек, который наилучшим образом будет обрабатывать любые конкретные изображения.

При вызове этого метода компонент Windows Imaging Component (WIC) передает фактический поток, содержащий изображение. Необходимо проверить, можно ли декодировать каждый кадр в изображении и перечислить блоки метаданных, чтобы точно объявить возможности этого декодера относительно конкретного переданного в него потока файлов. Это важно для всех декодеров, но особенно важно для форматов изображений, основанных на контейнерах формата TIFF. Процесс обнаружения выполняется путем сопоставления шаблонов, связанных с декодерами в реестре, с шаблонами в фактическом файле изображения. Объявление идентифицирующего шаблона в реестре гарантирует, что декодер будет всегда обнаруживаться для изображений в вашем формате изображения. Однако декодер по-прежнему может быть обнаружен для изображений в других форматах. Например, все контейнеры TIFF включают шаблон TIFF, который является допустимым идентифицирующим шаблоном для формата изображения TIFF. Это означает, что во время обнаружения в файлах изображений будут найдены по крайней мере два идентифицирующих шаблона для любого формата изображений, основанного на контейнере в стиле TIFF. Один из них будет шаблоном TIFF, а другой — фактическим шаблоном формата изображения. Хотя это и менее вероятно, возможны конфликты шаблонов между другими несвязанными форматами изображений. Именно поэтому обнаружение и арбитраж являются процессом, сооснованным на двух стадиях. Всегда проверяйте, что поток изображения, переданный в [**куерикапабилити**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) , действительно является допустимым экземпляром собственного формата изображения. Кроме того, если кодек декодирует формат изображения, для которого вы не владеете спецификацией, ваша реализация **куерикапабилити** должна проверить наличие любой функции, которая может быть допустимой в соответствии со спецификацией формата изображения, которую кодек не реализует. Это гарантирует, что пользователи не будут испытывать ненужные ошибки декодирования или получить непредвиденные результаты с помощью кодека.

Перед выполнением какой бы то ни было операции с изображением необходимо сохранить текущее расположение потока, чтобы его можно было восстановить в исходное расположение перед возвратом из метода. Перечисление [**викбитмапдекодеркапабилитиес**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) , указывающее возможности, определяется следующим образом:

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

Следует объявлять **викбитмапдекодеркапабилитисаминкодер** , только если кодировщик использовал тот, который кодирует изображение. После проверки возможности декодирования каждого кадра в контейнере следует объявить **викбитмапдекодеркапабилитикандекодесомеимажес** , если вы можете декодировать некоторые, но не все фреймы, **викбитмапдекодеркапабилитикандекодеаллимажес** , если вы можете декодировать все кадры, или ни одного, если вы не можете декодировать их. (Эти два перечисления являются взаимоисключающими; если возвращается **викбитмапдекодеркапабилитикандекодеаллимажес**, **викбитмапдекодеркапабилитикандекодесомеимажес** будет игнорироваться.) Объявите **викбитмапдекодеркапабилитиканенумератеметадата** после проверки, что можно перечислить блоки метаданных в контейнере Image. Не нужно проверять эскиз в каждом кадре. Если имеется глобальный эскиз, который можно декодировать, можно объявить **викбитмапдекодеркапабилитикандекодесумбнаил**. Если глобальный эскиз отсутствует, попытайтесь декодировать эскиз для кадра 0. Если в любом из этих мест нет эскиза, не объявляйте эту возможность.

Определив возможности декодера по отношению к потоку изображения, переданному этому методу, выполните операцию или с [**викбитмапдекодеркапабилитиес**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) , проверив, что этот декодер может выполняться на этом изображении, и возвратит результат. Не забудьте восстановить исходное расположение потока перед возвратом.

### <a name="initialize"></a>Инициализация

[**Инициализация**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) вызывается приложением после выбора декодера для декодирования определенного изображения. Поток изображения передается декодеру, и вызывающий объект может дополнительно указать параметр кэша [**викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) для работы с метаданными в файле.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Некоторые приложения используют метаданные больше, чем другие. Большинству приложений не требуется доступ ко всем метаданным в файле изображения и запрос конкретных метаданных по мере необходимости. Другие приложения, скорее всего, будут кэшировать все метаданные заранее, чем удерживать файловый поток и выполнять операции дискового ввода-вывода каждый раз, когда им нужно получить доступ к метаданным. Если вызывающий объект не указывает параметр кэша метаданных, поведение кэширования по умолчанию должно кэшироваться по запросу. Это означает, что метаданные не должны загружаться в память до тех пор, пока приложение не выдает конкретный запрос для этих метаданных. Если приложение указывает **WICDecodeMetadataCacheOnLoad**, метаданные должны загружаться в память немедленно и в кэше. При кэшировании метаданных при загрузке файловый поток может быть освобожден после кэширования метаданных.

### <a name="getcontainerformat"></a>жетконтаинерформат

Чтобы реализовать [**жетконтаинерформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), просто ВОЗВРАТИТЕ идентификатор GUID формата изображения, для которого создается экземпляр декодера. Этот метод также реализован в [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) и [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).

### <a name="getdecoderinfo"></a>жетдекодеринфо

[**Жетдекодеринфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) возвращает объект [**ивикбитмапдекодеринфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) . Чтобы получить объект **ивикбитмапдекодеринфо** , просто передайте идентификатор GUID декодера в метод [**креатекомпонентинфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) в [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), а затем запросите в нем интерфейс **ивикбитмапдекодеринфо** , как показано в следующем примере.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>жетфрамекаунт

[**Жетфрамекаунт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) просто возвращает количество кадров в контейнере. Некоторые форматы контейнеров поддерживают несколько кадров, а другие поддерживают только один кадр на контейнер.

### <a name="getframe"></a>GetFrame

Метод noframes является важным методом в интерфейсе [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) , поскольку кадр содержит фактические биты изображения, а объект декодера кадров, возвращаемый этим методом [**, является объектом**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) , который выполняет фактическое декодирование запрошенного изображения. Это другой объект, который необходимо реализовать при написании декодера. Дополнительные сведения о декодерах кадров см. в разделе [Реализация IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).

### <a name="getpreview"></a>Предварительная версия

Функция [**OnPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) возвращает предварительный просмотр изображения. Подробное описание предварительных версий см. в разделе [Реализация метода ивикбитмапенкодер](-wic-imp-iwicbitmapencoder.md) в [реализующем](-wic-imp-iwicbitmapencoder.md) интерфейсе ивикбитмапенкодер.

Если формат изображения содержит внедренный предварительный просмотр JPEG, настоятельно рекомендуется, чтобы вместо написания декодера JPEG для его декодирования вы делегирулись к декодеру JPEG, который поставляется вместе с платформой WIC для расшифровки предварительных версий и эскизов. Для этого следует перейти к началу данных предварительного просмотра изображения в потоке и вызвать метод [**креатедекодерфромстреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) в [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Зрения**
</dt> <dt>

[Интерфейсы декодера](-wic-decoderinterfaces.md)
</dt> <dt>

[Реализация Ивикбитмапкодекпрогресснотификатион (декодер)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



