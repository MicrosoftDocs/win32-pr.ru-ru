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
ms.openlocfilehash: 6ca2a6b7eae4550f4bbd4c8c8373d63c9bdd121e6561f08e591cb6a943d309f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023922"
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



 

 

 




