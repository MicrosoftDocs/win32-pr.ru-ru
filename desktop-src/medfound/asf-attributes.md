---
description: Атрибуты ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Атрибуты ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692094"
---
# <a name="asf-attributes"></a>Атрибуты ASF

### <a name="profile-attributes"></a>Атрибуты профиля

К профилям ASF применяются следующие атрибуты.



| attribute                                                                      | Описание                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**MF \_ асфпрофиле \_ макспаккетсизе**](mf-asfprofile-maxpacketsize-attribute.md) | Указывает максимальный размер пакета для файла ASF в байтах. |
| [**MF \_ асфпрофиле \_ минпаккетсизе**](mf-asfprofile-minpacketsize-attribute.md) | Указывает минимальный размер пакета для файла ASF в байтах. |



 

### <a name="stream-configuration-attributes"></a>Атрибуты конфигурации потока

Следующие атрибуты применяются к объекту конфигурации потока ASF.



| attribute                                                                              | Описание                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) | Задает среднее значение параметра "сегмент утечки" для кодирования файла Windows Media. |
| [**MF \_ асфстреамконфиг \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) | Задает пиковый параметр "сегмент утечки" для кодирования файла Windows Media.    |



 

### <a name="media-buffer-attributes"></a>Атрибуты буфера мультимедиа

Следующие атрибуты применяются к буферам мультимедиа для пакетов ASF.



| attribute                                                                          | Описание                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_граница пакета \_ мфасфсплиттер**](mfasfsplitter-packet-boundary-attribute.md) | Указывает, содержит ли буфер начало пакета расширенного системного формата (ASF). |



 

### <a name="presentation-descriptor-attributes"></a>Атрибуты дескриптора представления

Список атрибутов, применяемых к дескрипторам представления ASF, см. в разделе [атрибуты дескриптора представления](presentation-descriptor-attributes.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



