---
description: Реализация Ивикбитмапфраминкоде
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Реализация Ивикбитмапфраминкоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265863"
---
# <a name="implementing-iwicbitmapframeencode"></a>Реализация Ивикбитмапфраминкоде

## <a name="iwicbitmapframeencode"></a>ивикбитмапфраминкоде

[**Ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) — это аналог кодировщика для интерфейса [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . Этот интерфейс можно реализовать для класса кодирования на уровне кадров, который представляет собой класс, который выполняет фактическую кодировку битов изображения для каждого кадра.


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [Инициализация](#initialize)
-   [SetSize и Сетресолутион](#setsize-and-setresolution)
-   [сетпикселформат](#setpixelformat)
-   [сетколорконтекстс](#setcolorcontexts)
-   [жетметадатакуеривритер](#getmetadataquerywriter)
-   [сетсумбнаил](#setthumbnail)
-   [WritePixels](#writepixels)
-   [вритесаурце](#writesource)
-   [Фиксация](#commit)
-   [сетпалетте](#setpalette)

### <a name="initialize"></a>Инициализация

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) — это первый метод, вызываемый для объекта [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) после создания экземпляра. Этот метод имеет один параметр, который может иметь значение **null**. Этот параметр представляет параметры кодировщика и является тем же экземпляром [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , который был создан в методе [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) в декодере на уровне контейнера, и передается обратно вызывающему объекту в параметре пиенкодероптионс этого метода. В это время вы заполнили структуру IPropertyBag2 свойствами, которые представляют параметры кодирования, поддерживаемые кодировщиком на уровне кадров. Теперь вызывающий объект предоставил значения для этих свойств, чтобы указать определенные параметры параметров кодировки, и передает один и тот же объект обратно в инициализацию объекта **ивикбитмапфраминкоде** . При кодировании битов изображения следует применять указанные параметры.

### <a name="setsize-and-setresolution"></a>SetSize и Сетресолутион

[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) и [**сетресолутион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) говорят сами за себя. Вызывающий объект использует эти методы для указания размера и разрешения закодированного изображения.

### <a name="setpixelformat"></a>сетпикселформат

[**Сетпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) используется для запроса формата пикселей, в котором кодируется изображение. Если запрошенный формат пикселей не поддерживается, следует вернуть идентификатор GUID ближайшего формата пикселей, поддерживаемого в *ппикселформат*, который является параметром in/out.

### <a name="setcolorcontexts"></a>сетколорконтекстс

[**Сетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) используется для указания одного или нескольких допустимых контекстов цвета (также известных как цветовые профили) для этого изображения. Важно указать контексты цвета, поэтому приложение, которое будет декодировать образ в дальнейшем, может преобразовать исходный цветовой профиль в целевой профиль устройства, используемого для отображения или печати изображения. Без цветового профиля невозможно получить согласованные цвета на разных устройствах. Это может оказаться неприятной для конечных пользователей, когда фотографии выглядят по-разному на разных мониторах, и они не могут получить печать в соответствии с отображаемыми на экране.

### <a name="getmetadataquerywriter"></a>жетметадатакуеривритер

[**Жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) возвращает [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) , который приложение может использовать для вставки или изменения конкретных свойств метаданных в блоке метаданных в кадре изображения.

Создать экземпляр [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) из [**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) можно несколькими способами. Вы можете создать его из [**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), так же как [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) был создан из [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) в методе [**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) в интерфейсе [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



Его также можно создать из существующего [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), например, полученного с помощью предыдущего метода.


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



Параметр *пгуидвендор* позволяет указать конкретного поставщика, который должен использовать модуль записи запросов при создании экземпляра модуля записи метаданных. Например, при предоставлении собственных модулей записи метаданных может потребоваться указать собственный идентификатор GUID поставщика. Если у вас нет предпочтений, в этот параметр можно передать **значение NULL** .

### <a name="setthumbnail"></a>сетсумбнаил

[**Сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) используется для создания эскиза. Все изображения должны предоставлять эскизы глобально, в каждом фрейме или в обоих кадрах. Методы  WebMethod и **сетсумбнаил** являются необязательными на уровне контейнера, но, если кодек возвращает винкодек \_ Err \_ Кодекносумбнаил из метода, [](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) компонент Windows Imaging Component (WIC) вызовет метод для кадра 0 [](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) . Если в любом месте эскиз не найден, компонент WIC должен декодировать полное изображение и масштабировать его до размера эскиза, что может привести к значительному снижению производительности для больших изображений.

Эскиз должен иметь размер и разрешение, что позволяет быстро декодировать и отображать их. По этой причине эскизы — это наиболее распространенные изображения JPEG. Обратите внимание, что при использовании JPEG для эскизов вам не нужно писать кодировщик JPEG для их кодирования или декодер JPEG для декодирования. Всегда следует делегировать кодеку JPEG, поставляемому с платформой WIC, для кодирования и декодирования эскизов.

### <a name="writepixels"></a>WritePixels

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) — это метод, используемый для передачи строк просмотра из точечного рисунка в памяти для кодирования. Метод будет вызываться повторно до тех пор, пока не будут переданы все строки просмотра. Параметр *линекаунт* указывает, сколько строк проверки должно быть написано в этом вызове. Параметр *кбстриде* указывает число байтов на каждую строку развертки. *кббуфферсизе* указывает размер буфера, переданного в параметре пбпикселс, который содержит фактические биты изображения для кодирования. Если Объединенная высота строк просмотра из совокупных вызовов превышает высоту, указанную в методе [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , то возвращается винкодек \_ Err \_ туманисканлинес.

Если [**викбитмапенкодеркачеоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) имеет значение **викбитмапенкодеркачеинмемори**, строки просмотра должны быть помещены в кэш в памяти до тех пор, пока не будут переданы все строки проверки. Если параметр кэша кодировщика имеет значение **викбитмапенкодеркачетемпфиле**, строки просмотра должны кэшироваться во временном файле, созданном при инициализации объекта. В любом из этих случаев образ не должен кодироваться до тех пор, пока вызывающий объект не вызовет [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit). Если параметр Cache имеет значение **викбитмапенкодернокаче**, кодировщик должен по возможности кодировать строки сканирования по мере их получения. (В некоторых форматах это невозможно, и строки просмотра должны быть кэшированы до тех пор, пока не будет вызвана фиксация.)

Большинство необработанных кодеков не реализуют [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), так как они не поддерживают изменение битов изображения в необработанном файле. Однако необработанные кодеки должны по-прежнему реализовывать **WritePixels**, но, поскольку при добавлении метаданных размер файла может увеличиться, при этом файл должен быть переписан на диске. В этом случае необходимо иметь возможность копировать существующие биты образа, что делает метод **WritePixels** .

### <a name="writesource"></a>вритесаурце

[**Вритесаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) используется для кодирования объекта [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) . Первый параметр является указателем на объект **IWICBitmapSource** . Второй параметр — это Викрект, указывающий интересующую область. Этот метод может вызываться несколько раз подряд, если ширина каждого прямоугольника равна ширине окончательного изображения для кодирования. Если ширина прямоугольника, переданного в параметре PRC, отличается от ширины, указанной в методе SetSize, то возвращается ВИНКОДЕК \_ Err \_ саурцеректдоеснотматчдименсионс. Если Объединенная высота строк просмотра из совокупных вызовов превышает высоту, указанную в методе SetSize, то возвращается ВИНКОДЕК \_ Err \_ туманисканлинес.

Параметры кэширования работают так же, как и метод [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) , описанный ранее.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) — это метод, который сериализует закодированные биты изображения в файловый поток и выполняет перебор всех модулей записи метаданных для фрейма, запрашивающего их, для сериализации своих метаданных в поток. В случае, когда параметр кэша кодировщика имеет значение Викбитмапенкодеркачеинмемори или Викбитмапенкодеркачетемпфиле, этот метод также отвечает за кодирование изображения, а если параметр Cache имеет значение Викбитмапенкодеркачетемпфиле, то метод **commit** также должен удалить временный файл, используемый для кэширования данных изображения перед кодированием.

Этот метод всегда вызывается после передачи всех строк просмотра или прямоугольников, составляющих изображение, с помощью метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) или [**вритесаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) . Размер завершающего прямоугольника, состоящего из накопленных вызовов WritePixels или Вритесаурце, должен иметь тот же размер, что и в методе SetSize. Если размер не соответствует ожидаемому размеру, этот метод должен возвращать ВИНКОДЕЦЕРРОР \_ унекспектедсизе.

Чтобы выполнить итерацию модулей записи метаданных и сообщить каждому модулю записи метаданных о необходимости сериализации своих метаданных, необходимо вызвать Жетвритербиндекс для прохода по модулям записи для каждого блока и вызвать Ивикперсистстреам. Save в каждом модуле записи метаданных.


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a>сетпалетте

Только кодеки, имеющие Индексированные форматы, должны реализовывать метод [**сетпалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) . Если изображение использует индексированный формат, используйте этот метод для указания палитры цветов, используемых в изображении. Если у кодека нет индексированного формата, возвратите ВИНКОДЕК \_ Err \_ палеттеунаваилабле из этого метода.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Реализация Ивикбитмапкодекпрогресснотификатион (кодировщик)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Реализация Ивикметадатаблокквритер](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
