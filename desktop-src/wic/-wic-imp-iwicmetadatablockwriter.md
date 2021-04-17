---
description: Реализация Ивикметадатаблокквритер
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Реализация Ивикметадатаблокквритер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547050"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Реализация Ивикметадатаблокквритер

## <a name="iwicmetadatablockwriter"></a>ивикметадатаблокквритер

-   [инитиализефромблоккреадер](#initializefromblockreader)
-   [жетвритербиндекс](#getwriterbyindex)
-   [аддвритер](#addwriter)
-   [сетвритербиндекс](#setwriterbyindex)
-   [ремовевритербиндекс](#removewriterbyindex)

Класс кодирования на уровне кадров реализует этот интерфейс для предоставления всех блоков метаданных и запроса соответствующего модуля записи метаданных для каждого блока. Если формат изображения поддерживает глобальные метаданные вне отдельных фреймов, следует также реализовать этот интерфейс в классе кодировщика уровня контейнера. Более подробное описание обработчиков метаданных см. в разделе [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) в разделе Реализация декодера WIC-Enabled.

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a>инитиализефромблоккреадер

[**Инитиализефромблоккреадер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) использует [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) для инициализации модуля записи блока. **Ивикметадатаблоккреадер** можно получить из декодера, который декодирует образ.


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



Поскольку инициализация [**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) с помощью [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) создает экземпляр модуля записи метаданных для каждого модуля чтения метаданных, предоставляемого объектом **ивикметадатаблоккреадер** , приложению не нужно явным образом запрашивать модуль записи для каждого блока метаданных.

### <a name="getwriterbyindex"></a>жетвритербиндекс

[**Жетвритербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) возвращает объект [**ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) для n-го блока метаданных, где n — это значение, передаваемое в параметре *ниндекс* . Если нет зарегистрированного модуля записи метаданных, который может обрабатывать тип метаданных в блоке n, фабрика компонентов вернет неизвестный обработчик метаданных, который будет обрабатывать блок метаданных как большой двоичный объект (BLOB). Она будет сериализована как битовый поток без попытки его анализа.

### <a name="addwriter"></a>аддвритер

[**Аддвритер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) позволяет вызывающему объекту добавить новый модуль записи метаданных. Это необходимо, если приложению требуется добавить метаданные другого формата, чем любой из существующих блоков метаданных. Например, приложению может потребоваться добавить некоторые метаданные XMP. Если существующего блока метаданных XMP нет, приложение должно создать экземпляр модуля записи метаданных XMP и использовать метод **аддвритер** , чтобы включить его в коллекцию модулей записи метаданных.

### <a name="setwriterbyindex"></a>сетвритербиндекс

[**Сетвритербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) используется для добавления модуля записи метаданных в указанный индекс в коллекции. Если в этом индексе уже существует модуль записи метаданных, новый элемент должен заменить его.

### <a name="removewriterbyindex"></a>ремовевритербиндекс

[**Ремовевритербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) используется для удаления модуля записи метаданных из коллекции.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Реализация Ивикбитмапфраминкоде](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Установка и регистрация КОДЕка](-wic-codecinstallandreg.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



