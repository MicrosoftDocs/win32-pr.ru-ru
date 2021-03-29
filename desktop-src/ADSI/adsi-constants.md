---
title: Константы ADSI
description: В следующей таблице перечислены константы, определенные и используемые в Active Directory интерфейсах служб (ADSI).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773022"
---
# <a name="adsi-constants"></a>Константы ADSI

В следующей таблице перечислены константы, определенные и используемые в Active Directory интерфейсах служб (ADSI).



| Константа ADSI                      | Значение                                   | Описание                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Реклама \_ ext \_ иниткредентиалс**      | 1                                       | Управляющий код, указывающий, что пользовательские данные, передаваемые в метод [**иадсекстенсион:: оперирует**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) , содержат учетные данные пользователя.                                                     |
| **\_ \_ Инициализация ext AD \_ завершена** | 2                                       | Управляющий код, используемый с [**иадсекстенсион:: работают**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) , чтобы указать, что расширения могут выполнять необходимую инициализацию в зависимости от возможностей, поддерживаемых родительским объектом. |
| **Реклама \_ ext \_ максекстдиспид**         | 16777215                                | Самый высокий идентификатор DISPID, который объект расширения может использовать для своих методов и свойств.                                                                                                                                   |
| **Реклама \_ ext \_ минекстдиспид**         | 1                                       | Самый низкий идентификатор DISPID, который объект расширения может использовать для своих методов и свойств.                                                                                                                                    |
| **\_ответ VLV \_ ADS**             | L "fc8cb04d-311d-406c-8cb9-1ae8b843b419" | Используется с методом [**IDirectorySearch:: DataColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) для получения МЕТАДАННЫХ поиска VLV. Дополнительные сведения см. [в разделе Поиск с помощью VLV](how-to-search-using-vlv.md).        |
| **DBPROPFLAGS \_ адсисеарч**        | 0x0000C000                              | Используется для работы с поставщиком OLE DB.                                                                                                                                                                           |



 

 

 




