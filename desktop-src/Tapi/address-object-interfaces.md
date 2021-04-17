---
description: Объекты Address — это сущности, которые могут принимать или принимать вызовы. Связанные интерфейсы и методы позволяют приложению получать и задавать сведения об адресе, например, поддерживает ли адрес вызывающий объект.
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: Интерфейсы объекта Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef19db02123e10e839906a00931ef246d19d2c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683804"
---
# <a name="address-object-interfaces"></a>Интерфейсы объекта Address

[Объекты Address](address-object.md) — это сущности, которые могут принимать или принимать вызовы. Связанные интерфейсы и методы позволяют приложению получать и задавать сведения об адресе, например, поддерживает ли адрес вызывающий объект.

Интерфейсы [**итаддрессевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent), [**итаддресстранслатионинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo), [**иткаллингкард**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard), [**итфорвардинформатион**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation), [**итлокатионинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)и [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress) не предоставляются напрямую в объект Address, но тесно связаны с ним и перечислены здесь для удобства.



| Интерфейс                                                            | Описание                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**итаддресс**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | Выступает в качестве базового интерфейса для объекта Address.                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | Является производным от [**итаддресс**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress); предоставляет дополнительные методы, поддерживающие телефонные устройства.                                            |
| [**итаддресскапабилитиес**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | Возвращает сведения о возможностях адреса.                                                                                          |
| [**итаддрессевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | Предоставляет сведения о событиях адресации.                                                                                                 |
| [**итаддресстранслатион**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | Выполняет преобразование адресов.                                                                                                                   |
| [**итаддресстранслатионинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | Возвращает сведения о преобразовании адреса.                                                                                                           |
| [**иткаллингкард**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | Предоставляет методы для получения сведений о вызывающей карточке.                                                                                          |
| [**итфорвардинформатион**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | Предоставляет методы для настройки и реализации переадресации вызовов.                                                                               |
| [**итлегациаддрессмедиаконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | Поддерживает устаревшие приложения, требующие прямого доступа к устройству и его конфигурации.                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | Расширяет [**итлегациаддрессмедиаконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) , разрешая настройку параметров, относящихся к линейным устройствам. |
| [**итлокатионинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | Возвращает сведения, относящиеся к расположению вызывающей стороны.                                                                                  |
| [**итмедиасуппорт**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | Возвращает сведения о возможностях поддержки мультимедиа адреса.                                                                            |
| [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | Получает сведения о доступных терминалах и предоставляет метод для создания дополнительных терминалов.                                                   |
| [**иенумаддресс**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | Перечисляет [**итаддресс**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress).                                                                                                      |
| [**иенумкаллингкард**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | Перечисляет [**иткаллингкард**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard).                                                                                              |



 

Если адрес является адресом [WAV](wave-msp.md) , интерфейс [**итлегацивавесуппорт**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) также предоставляется в объекте Address.

 

 
