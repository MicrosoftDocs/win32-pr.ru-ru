---
description: Интерфейс Ицертвиев используется надлежащими клиентами для просмотра базы данных служб сертификации.
ms.assetid: c8f316dd-186b-4e4a-b0ce-561a23b266cb
title: Просмотр базы данных служб сертификации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c553cee2f64c3096e733d588c9e0ad3d08ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156570"
---
# <a name="viewing-the-certificate-services-database"></a>Просмотр базы данных служб сертификации

Интерфейс [**ицертвиев**](/windows/desktop/api/Certview/nn-certview-icertview) используется надлежащими клиентами для просмотра базы данных служб сертификации. Следует отметить, что в составе поставляемого продукта оснастка MMC центра сертификации может использоваться для просмотра базы данных служб сертификации. [**Ицертвиев**](/windows/desktop/api/Certview/nn-certview-icertview) предоставляется для программного просмотра базы данных. Поддержка интерфейса **ицертвиев** начинается с Windows XP.

Полномочный клиент означает, что пользователь предоставил разрешение на просмотр базы данных служб сертификатов; оснастку MMC "центр сертификации" можно использовать для предоставления или ограничения доступа для просмотра базы данных (в разделе **Свойства** [*центра сертификации*](../secgloss/c-gly.md)перейдите на вкладку **Безопасность** ). Кроме того, чтобы использовать объект [**ицертвиев**](/windows/desktop/api/Certview/nn-certview-icertview) , клиентская рабочая станция должна установить клиентские компоненты служб сертификации.

Хотя существуют различные сценарии для использования [**ицертвиев**](/windows/desktop/api/Certview/nn-certview-icertview) и связанных с ним интерфейсов, на следующем изображена одна возможная последовательность для разработки клиентского приложения на основе **ицертвиев**:

**Просмотр базы данных служб сертификации**

1.  После получения экземпляра объекта [**ицертвиев**](/windows/desktop/api/Certview/nn-certview-icertview) вызовите [**Ицертвиев:: OpenConnection**](/windows/desktop/api/Certview/nf-certview-icertview-openconnection) для взаимодействия с [*центром сертификации*](../secgloss/c-gly.md) на определенном компьютере.
2.  Вызовите метод [**ицертвиев:: сетресултколумнкаунт**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) , чтобы указать число столбцов в представлении. Этот вызов также используется для указания представления по умолчанию. Если в вызове не указано представление по умолчанию, вызывающий объект должен вызвать [**ицертвиев:: сетресултколумн**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn) для каждого столбца, который должен содержаться в представлении.
3.  Необязательный элемент. Укажите критерии сортировки и (или) критерии соответствия для запроса к базе данных, вызвав функцию [**ицертвиев:: сетрестриктион**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) . Квалифицированные критерии состоят из представления для получения данных на основе квалификаторов, таких как «больше», «меньше», «равно» и т. д.
4.  Вызовите метод [**ицертвиев:: OpenView**](/windows/desktop/api/Certview/nf-certview-icertview-openview) , чтобы получить данные в представлении. данные представления будут состоять из столбцов, запрошенных с помощью [**ицертвиев:: сетресултколумнкаунт**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) (и если не указано представление по умолчанию, [**Ицертвиев:: сетресултколумн**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn)). Если был вызван метод [**ицертвиев:: сетрестриктион**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) , то данные в столбцах будут отсортированы и (или) определены. **Ицертвиев:: OpenView** создает объект [**иенумцертвиевров**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) , который может использоваться для перечисления строк представления.
5.  Используйте методы [**Иенумцертвиевров**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) [**Иенумцертвиевров:: енумцертвиеваттрибуте**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewattribute), [**Иенумцертвиевров:: Енумцертвиевколумн**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewcolumn)и [**IEnumCERTVIEWROW:: EnumCertViewExtension**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewextension) для получения данных атрибута, столбца и расширения по мере необходимости.

 

 
