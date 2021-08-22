---
title: Предоставление сведений о классе
description: Предоставление сведений о классе
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a042283ca9ba6eb29bceeacef2c32f9bd401ef09e92eafbc737711d0d930336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500124"
---
# <a name="providing-class-information"></a>Предоставление сведений о классе

Часто бывает полезно, чтобы клиент объекта просматривает сведения о типе объекта. При наличии идентификатора CLSID объекта клиент может найти библиотеку типов объекта с помощью записей реестра, а затем может проверить библиотеку типов для записи coclass в библиотеке, соответствующей идентификатору CLSID.

Однако не все объекты имеют CLSID, хотя им по-прежнему требуется предоставить информацию о типе. Кроме того, удобно, чтобы клиент имел способ просто запросить объект для получения сведений о его типе, вместо того чтобы использовать все долгой для извлечения той же информации из записей реестра. Эта возможность важна при работе с исходящими интерфейсами на подключаемых объектах. (Дополнительные сведения о том, как подключаемые объекты обеспечивают такую возможность, см. в разделе [Использование IProvideClassInfo](using-iprovideclassinfo.md) .)

В таких случаях клиент может запросить объект для [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) или [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). Если эти интерфейсы существуют, клиент вызывает метод [**жетклассинфо**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) для получения сведений о типе для интерфейса.

При реализации интерфейса [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) или [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)объект указывает, что он может предоставлять сведения о типе для всего класса; Это значит, что оно будет описывать в разделе его класса Library, если таковой имеется. [**Жетклассинфо**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) возвращает указатель **ITypeInfo** , соответствующий сведениям о соклассах объекта. С помощью этого указателя **ITypeInfo** клиент может изучить все входящие и исходящие определения интерфейса объекта.

Объект также может предоставлять [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). Интерфейс **IProvideClassInfo2** — это простое расширение для интерфейса [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) , которое позволяет быстро и легко извлекать исходящие идентификаторы интерфейса объекта для набора событий по умолчанию. **IProvideClassInfo2** является производным от **IProvideClassInfo**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[COM-клиенты и серверы](com-clients-and-servers.md)
</dt> </dl>

 

 




