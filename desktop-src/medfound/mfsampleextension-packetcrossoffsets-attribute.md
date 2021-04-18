---
description: Задает смещение для границ полезных данных в кадре для защищенных выборок.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: Атрибут MFSampleExtension_PacketCrossOffsets (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719423"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a>Мфсампликстенсион \_ паккеткроссоффсетс, атрибут

Задает смещение для границ полезных данных в кадре для защищенных выборок.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к примерам мультимедиа, защищенным цифровыми Rights Management Windows Media (DRM). Значение атрибута является массивом **DWORD** s. Каждая запись в массиве является смещением границы полезной нагрузки относительно начала кадра. Приложение может использовать эти значения при расшифровке и перестроении кадров.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Разделитель ASF](asf-splitter.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> </dl>

 

 




