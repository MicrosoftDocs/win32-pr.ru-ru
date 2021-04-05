---
description: Задание типа выходных данных для кодировщика WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Задание типа выходных данных для кодировщика WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143219"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Задание типа выходных данных для кодировщика WMA

Чтобы создать допустимый тип выходных данных для кодировщика Windows Media Audio (WMA), необходимо иметь следующие сведения:

-   Подтип Audio, репесентс закодированный формат WMA. См. раздел [идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md).
-   Свойства конфигурации, заданные для кодировщика.

    Свойства конфигурации описаны в документации по API-интерфейсам аудио-и видеокодеков Windows Media и DSP. Дополнительные сведения см. в разделе "свойства аудиопотока в [свойствах кодировки](configuring-the-encoder.md)".

### <a name="windows-vista-or-later"></a>Windows Vista или более поздней версии

Чтобы получить допустимый тип выходных данных для кодировщика, выполните следующие действия.

1.  Используйте функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) или [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) для создания экземпляра кодировщика.
2.  Запросите кодировщик для интерфейса **ипропертисторе** .
3.  Используйте интерфейс **ипропертисторе** для настройки кодировщика.
4.  Получите Поддерживаемые типы выходных данных, вызвав [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) в цикле до тех пор, пока кодировщик **не возвратит MF \_ E больше \_ \_ \_ типов** и вы выбираете тип целевого носителя. I
5.  Вызовите [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , чтобы задать тип сжатия мультимедиа для кодировщика.

### <a name="windows-7"></a>Windows 7

Чтобы получить допустимый тип выходных данных кодировщика в Windows 7, Media Foundation предоставляет функцию [**мфтранскодежетаудиуутпутаваилаблетипес**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) . Приложение должно пройти обязательное аудио подтип, репесентс закодированный WMA и свойства кодировки. Свойства являются обязательными, так как кодировщик изменяет Поддерживаемые типы вывода в зависимости от набора режимов.

> [!Note]  
> [**Мфтранскодежетаудиуутпутаваилаблетипес**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)поддерживается только для [кодирования с постоянной скоростью потока](constant-bit-rate-encoding.md).

 

Если вызов будет выполнен, приложение получит список указателей IUnknown поддерживаемых типов выходных данных в объекте [**имфколлектион**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) . Чтобы задать тип выходного носителя, найдите тот, который соответствует типу целевого объекта, и вызовите [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , чтобы задать тип мультимедиа сжатия в кодировщике.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание экземпляра MFT для кодировщика](instantiating-the-encoder-mft.md)
</dt> <dt>

[Кодировщики Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



