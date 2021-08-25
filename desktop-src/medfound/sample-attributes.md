---
description: Примеры атрибутов
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Примеры атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56593978a411b314e6e988c031ee36869c4ea44212fd7f154e3ba18478400b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776984"
---
# <a name="sample-attributes"></a>Примеры атрибутов

К [примерам носителей](media-samples.md)применяются следующие атрибуты. Чтобы получить атрибуты из примера носителя, используйте интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| attribute                                                                                                      | Описание                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Мфсампликстенсион \_ 3DVideo](mfsampleextension-3dvideo.md)                                                    | Указывает, содержит ли образец носителя трехмерный видеокадр.                                                                                                                                                                                        |
| [Мфсампликстенсион \_ 3DVideo \_ самплеформат](mfsampleextension-3dvideo-sampleformat.md)                         | Указывает, как трехмерный видеокадр хранится в примере носителя.                                                                                                                                                                                        |
| [**Мфсампликстенсион \_ боттомфиелдфирст**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Задает поле превосходство для чередующихся видеокадров.                                                                                                                                                                                       |
| [Мфсампликстенсион \_ камераекстринсикс](mfsampleextension-cameraextrinsics.md)                                  | Внешние камеры для образца.                                                                                                                                                                                                              |
| [Мфсампликстенсион \_ каптуреметадата](mfsampleextension-capturemetadata.md)                                    | Хранилище [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для всех метаданных, связанных с конвейером захвата.                                                                                                                                             |
| [**Мфсампликстенсион \_ клеанпоинт**](mfsampleextension-cleanpoint-attribute.md)                                | Указывает, является ли образец видео ключевым кадром.                                                                                                                                                                                                   |
| [\_KeyID содержимого \_ мфсампликстенсион](mfsampleextension-content-keyid.md)                                       | Задает идентификатор ключа для образца.                                                                                                                                                                                                                    |
| [**Мфсампликстенсион \_ дериведфромтопфиелд**](mfsampleextension-derivedfromtopfield-attribute.md)              | Указывает, был ли извлеченный видеокадр получен из верхнего или нижнего поля.                                                                                                                                                  |
| [Мфсампликстенсион \_ DeviceTimestamp](mfsampleextension-devicetimestamp.md)                                    | Метка времени из драйвера устройства.                                                                                                                                                                                                             |
| [**Мфсампликстенсион \_ прекращение**](mfsampleextension-discontinuity-attribute.md)                          | Указывает, является ли образец носителя первым примером после разрыва в потоке.                                                                                                                                                                    |
| [\_Криптбитеблокк шифрования \_ мфсампликстенсион](mfsampleextension-encryption-cryptbyteblock.md)               | Задает размер зашифрованного блока байтов для шифрования шаблона на основе образца.                                                                                                                                                                       |
| [\_Протектионсчеме шифрования \_ мфсампликстенсион](mfsampleextension-encryption-protectionscheme.md)           | Указывает схему защиты для зашифрованных образцов.                                                                                                                                                                                             |
| [\_Самплеид шифрования \_ мфсампликстенсион](mfsampleextension-encryption-sampleid.md)                           | Указывает идентификатор зашифрованного примера.                                                                                                                                                                                                           |
| [\_Скипбитеблокк шифрования \_ мфсампликстенсион](mfsampleextension-encryption-skipbyteblock.md)                 | Задает размер блока Clear (незашифрованный) байт для шифрования шаблона на основе образца.                                                                                                                                                           |
| [\_Субсамплемаппингсплит шифрования \_ мфсампликстенсион](mfsampleextension-encryption-subsamplemappingsplit.md) | Задает сопоставление подобразца для образца, указывающего очищенные и зашифрованные байты в образце данных.                                                                                                                                            |
| [Мфсампликстенсион \_ фрамекорруптион](mfsampleextension-framecorruption.md)                                    | Указывает, поврежден ли кадр видео.                                                                                                                                                                                                      |
| [Мфсампликстенсион \_ форвардеддекодеунитс](mfsampleextension-forwardeddecodeunits.md)                          | Возвращает объект типа [**имфколлектион**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) , содержащий объекты [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , которые содержат единицы уровня абстракции сети (налус) и дополнительные модули сведений об улучшении (SEI), перенаправляемые декодером. |
| [Мфсампликстенсион \_ форвардеддекодеуниттипе](mfsampleextension-forwardeddecodeunittype.md)                    | Указывает тип (НАЛУ или SEI) единицы, присоединенной к [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) в коллекции [мфсампликстенсион \_ форвардеддекодеунитс](mfsampleextension-forwardeddecodeunits.md) .                                                    |
| [**Мфсампликстенсион с \_ чередованием**](mfsampleextension-interlaced-attribute.md)                                | Указывает, находится ли кадр видео с чередованием или с последовательной разверткой.                                                                                                                                                                                      |
| [Мфсампликстенсион \_ лонгтермреференцефрамеинфо](mfsampleextension-longtermreferenceframeinfo.md)              | Указывает сведения о кадре длинных ссылок (LTR) и возвращается в образце выходных данных.                                                                                                                                                               |
| [Мфсампликстенсион \_ меанабсолутедифференце](mfsampleextension-meanabsolutedifference.md)                      | Этот атрибут возвращает среднее абсолютное различие (MAD) во всех блоках макросов на плоскости Y.                                                                                                                                                  |
| [**Мфсампликстенсион \_ паккеткроссоффсетс**](mfsampleextension-packetcrossoffsets-attribute.md)                | Задает границы полезных данных для кадра. Это относится к зашифрованным примерам.                                                                                                                                                                   |
| [Мфсампликстенсион \_ ФотоЭскизы](mfsampleextension-photothumbnail.md)                                      | Содержит эскиз фотографии [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).                                                                                                                                                                                  |
| [Мфсампликстенсион \_ фотосумбнаилмедиатипе](mfsampleextension-photothumbnailmediatype.md)                    | Содержит [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , описывающий тип формата изображения, который содержится в атрибуте [мфсампликстенсион \_ thumbnail](mfsampleextension-photothumbnail.md) .                                                      |
| [Мфсампликстенсион \_ пинхолекамераинтринсикс](mfsampleextension-pinholecameraintrinsics.md)                    | Встроенные функции камеры пинхоле для образца.                                                                                                                                                                                                      |
| [**Мфсампликстенсион \_ репеатфирстфиелд**](mfsampleextension-repeatfirstfield-attribute.md)                    | Указывает, следует ли повторять первое поле в чередовании кадров.                                                                                                                                                                                |
| [Мфсампликстенсион \_ роиректангле](mfsampleextension-roirectangle.md)                                          | Задает границы интересующей области, указывающие регион кадра, для которого требуется другое качество.                                                                                                                            |
| [**Мфсампликстенсион \_ синглефиелд**](mfsampleextension-singlefield-attribute.md)                              | Указывает, содержит ли образец видео одно поле или два поля с чередованием                                                                                                                                                                 |
| [Мфсампликстенсион \_ таржетглобаллуминанце](mfsampleextension-targetgloballuminance.md)                        | Значение в НИТС, указывающее целевую яркость для связанного видеокадра.                                                                                                                                           |
| [**\_Токен мфсампликстенсион**](mfsampleextension-token-attribute.md)                                          | Содержит указатель на маркер, предоставленный методу [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .                                                                                                             |
| [Мфсампликстенсион \_ видеоенкодепиктуретипе](mfsampleextension-videoencodepicturetype.md)                      | Задает границы интересующей области, указывающие регион кадра, для которого требуется другое качество.                                                                                                                            |
| [Мфсампликстенсион \_ видеоенкодекп](mfsampleextension-videoencodeqp.md)                                        | Указывает параметр дискретизация (QP), который использовался для кодирования примера видео.                                                                                                                                                                  |



 

Не каждый пример носителя содержит все перечисленные здесь атрибуты. В некоторых случаях атрибут применяется только к определенным типам данных. Например, некоторые атрибуты применяются только к образцам видео и не должны отображаться в образцах аудио. В других случаях атрибут имеет значение по умолчанию, которое применяется, если атрибут не задан.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> </dl>

 

 



