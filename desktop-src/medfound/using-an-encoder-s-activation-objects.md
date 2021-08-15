---
description: для преобразования файлов мультимедиа в формат ASF можно использовать Windows кодировщики мультимедиа. Сведения об использовании объектов активации кодировщика.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Использование объектов активации кодировщиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24915020c1b888be6a1aeaca1e21af95d11cfc181a5c00a91c8359c3f780fa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972743"
---
# <a name="using-an-encoders-activation-objects"></a>Использование объектов активации кодировщика

для преобразования файлов мультимедиа в формат ASF можно использовать Windows кодировщики мультимедиа. Чтобы использовать эти кодировщики, они должны быть зарегистрированы в системе.

Дополнительные сведения о регистрации кодировщика см. [в разделе Создание экземпляра MFT кодировщика](instantiating-the-encoder-mft.md).

-   [Использование объектов активации кодировщика](#using-an-encoders-activation-objects)
-   [перечисление кодировщиков в Windows 7 и более поздних версиях](#encoder-enumeration-in-windows-7-and-later)
-   [Связанные темы](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Использование объектов активации кодировщика

В качестве альтернативы использованию интерфейса [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) кодировщика (описанного в разделе [Создание кодировщика с помощью CoCreateInstance](using-an-encoder-s-imftransform--interface.md)) можно создать экземпляр объекта активации для кодировщика. Объекты активации упрощают создание кодировщика и Media Foundation предоставляют следующие две функции для этого подхода:

-   [**мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) для создания экземпляра кодировщика Windows Media audio.
-   [**мфкреатевмвенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) для создания экземпляра кодировщика видео мультимедиа Windows.

Для обоих этих функций требуется создать целевой тип носителя и задать свойства кодировки перед вызовом этих функций. Если приложение использует [компоненты ASF уровня конвейера](pipeline-layer-asf-components.md) для кодирования файла в формат ASF и уже создали и настроили [приемники мультимедиа ASF](asf-media-sinks.md), вы можете получить этот набор сведений из приемника ASF Media.

[**Мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) и [**мфкреатевмвенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) устанавливают тип выходных данных кодировщика в тип мультимедиа, заданный приложением.

**Примечание**  .  Если вы используете [**мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) и [**мфкреатевмвенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) , можно активировать кодировщик, вызвав [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) , но нельзя изменить входные и выходные типы выходных данных кодировщика, а также не изменять свойства кодировки.

Дополнительные сведения о создании объектов Media Foundation с помощью объектов активации см. в разделе [объекты активации](activation-objects.md).

**Получение типа целевого носителя из приемника ASF Media**

1.  Получите указатель на указатель [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) приемника мультимедиа ASF, вызвав **Имфмедиасинк:: QueryInterface** в приемнике ASF Media и передав идентификатор **IID \_ имфасфконтентинфо** в качестве идентификатора интерфейса.
2.  Получите объект профиля ASF, связанный с объектом Контентинфо.
3.  Перечислите потоки в профиле, чтобы получить тип носителя потока.

**Получение свойств кодировки из приемника мультимедиа ASF**

1.  Если вы настроили [Свойства кодировки](configuring-the-encoder.md) в приемнике мультимедиа (см. описание в разделе [Установка свойств в приемнике файлов](setting-properties-in-the-file-sink.md)), можно получить ссылку на хранилище свойств приемника, вызвав **имфмедиасинк:: QueryInterface** в приемнике ASF Media и передав **IID \_ ипропертисторе** в качестве идентификатора интерфейса.
2.  Если у вас есть указатель на объект Контентинфо приемника, можно вызвать [**имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) , чтобы получить ссылку на хранилище свойств приемника мультимедиа.

    Убедитесь, что все свойства кодировки, заданные для приемника мультимедиа ASF, отражены в хранилище свойств, переданном в [**мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) и [**мфкреатевмвенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). Кодировщик настраивается автоматически на основе параметров, заданных приложением.

При создании узла преобразования в топологии кодирования можно задать тип объекта как указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученный в этих двух вызовах. При разрешении топологии сеанс мультимедиа использует объект активации для создания экземпляра файла MFT кодировщика.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>перечисление кодировщиков в Windows 7 и более поздних версиях

для приложений, выполняющихся в Windows 7, в дополнение к [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) можно перечислить кодировщик мфтс, вызвав [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Эта функция возвращает указатель на объект активации MFT для кодировщика. Структура функции очень похожа на **мфтенум** , описанную выше, за исключением того, что **мфтенумекс** возвращает массив указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) для кодировщика МФТС, соответствующих условиям поиска.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание экземпляра MFT для кодировщика](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Кодировщики мультимедиа](windows-media-encoders.md)
</dt> <dt>

[Объекты активации](activation-objects.md)
</dt> </dl>

 

 



