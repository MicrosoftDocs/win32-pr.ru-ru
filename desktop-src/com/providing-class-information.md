---
title: Предоставление сведений о классе
description: Предоставление сведений о классе
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132931"
---
# <a name="providing-class-information"></a>Предоставление сведений о классе

Часто бывает полезно, чтобы клиент объекта просматривает сведения о типе объекта. При наличии идентификатора CLSID объекта клиент может найти библиотеку типов объекта с помощью записей реестра, а затем может проверить библиотеку типов для записи coclass в библиотеке, соответствующей идентификатору CLSID.

Однако не все объекты имеют CLSID, хотя им по-прежнему требуется предоставить информацию о типе. Кроме того, удобно, чтобы клиент имел способ просто запросить объект для получения сведений о его типе, вместо того чтобы использовать все долгой для извлечения той же информации из записей реестра. Эта возможность важна при работе с исходящими интерфейсами на подключаемых объектах. (Дополнительные сведения о том, как подключаемые объекты обеспечивают такую возможность, см. в разделе [Использование IProvideClassInfo](using-iprovideclassinfo.md) .)

В таких случаях клиент может запросить объект для [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) или [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). Если эти интерфейсы существуют, клиент вызывает метод [**жетклассинфо**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) для получения сведений о типе для интерфейса.

При реализации интерфейса [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) или [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)объект указывает, что он может предоставлять сведения о типе для всего класса; Это значит, что оно будет описывать в разделе его класса Library, если таковой имеется. [**Жетклассинфо**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) возвращает указатель **ITypeInfo** , соответствующий сведениям о соклассах объекта. С помощью этого указателя **ITypeInfo** клиент может изучить все входящие и исходящие определения интерфейса объекта.

Объект также может предоставлять [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). Интерфейс **IProvideClassInfo2** — это простое расширение для интерфейса [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) , которое позволяет быстро и легко извлекать исходящие идентификаторы интерфейса объекта для набора событий по умолчанию. **IProvideClassInfo2** является производным от **IProvideClassInfo**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[COM-клиенты и серверы](com-clients-and-servers.md)
</dt> </dl>

 

 




