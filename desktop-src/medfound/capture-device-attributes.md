---
description: Запись атрибутов устройства
ms.assetid: dd24671a-0689-4490-8d18-2a33ed461e9d
title: Запись атрибутов устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dd8dbcdf0a441ddb8a5ef2794526e961c22033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692086"
---
# <a name="capture-device-attributes"></a>Запись атрибутов устройства

Следующие атрибуты связаны с устройствами записи.



| attribute                                                                                                                     | Описание                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [\_ \_ \_ понятное имя атрибута MF девсаурце \_](mf-devsource-attribute-friendly-name.md)                                          | Отображаемое имя устройства.                                                          |
| [\_ \_ \_ тип носителя атрибута MF \_ девсаурце](mf-devsource-attribute-media-type.md)                                                | Формат вывода устройства.                                                         |
| [\_ \_ \_ тип источника атрибута MF \_ девсаурце](mf-devsource-attribute-source-type.md)                                              | Тип устройства, например запись звука или запись видео.                         |
| [\_ДЕВСАУРЦЕ MF \_ \_ тип источника \_ атрибута \_ аудкап \_ идентификатор конечной точки \_](mf-devsource-attribute-source-type-audcap-endpoint-id.md)     | Идентификатор конечной точки для устройства записи звука.                                        |
| [\_роль девсаурце \_ \_ типа источника атрибута MF \_ \_ аудкап \_](mf-devsource-attribute-source-type-audcap-role.md)                    | Роль устройства для устройства записи звука.                                        |
| [\_Категория ДЕВСАУРЦЕ \_ MF \_ тип источника атрибута \_ \_ видкап \_](mf-devsource-attribute-source-type-vidcap-category.md)            | Категория устройства для видеоустройства.                                             |
| [\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ \_ источник оборудования](mf-devsource-attribute-source-type-vidcap-hw-source.md)         | Указывает, является ли источник видеозаписи аппаратным устройством или программным устройством. |
| [\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ Максимальное число \_ буферов](mf-devsource-attribute-source-type-vidcap-max-buffers.md)     | Указывает максимальное число кадров, которые будут помещены в буфер источника видеозаписи видео.   |
| [\_ДЕВСАУРЦЕ MF \_ \_ тип источника \_ атрибута \_ видкап \_ символьная \_ ссылка](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) | Символьная ссылка для драйвера видеозаписи.                                       |
| [\_ \_ Метка времени в MFT HW \_ с \_ \_ атрибутом QPC](mft-hw-timestamp-with-qpc-attribute.md)                                           | Указывает, использует ли источник устройства Системное время для меток времени.           |



 

Эти атрибуты используются со следующими функциями:

-   [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



