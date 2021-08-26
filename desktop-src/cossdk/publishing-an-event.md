---
description: Публикация события
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Публикация события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724dc94ddf9cc25ec3b11cc31376805241e9d6d67250f8a494f8b417b9d201a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990504"
---
# <a name="publishing-an-event"></a>Публикация события

чтобы опубликовать событие, просто создайте экземпляр объекта события, вызвав [**cocreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) или метод Microsoft Visual Basic **CreateObject** , используя евентклассид или евенткласснаме в качестве аргумента. Издатель вызывает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на объекте события для получения интерфейсов, поддерживаемых объектом класса событий, и вызывает метод для объекта события через интерфейс для публикации события. Затем система событий публикует события в классе событий CLSID \_ евентобжектчанже с ИД интерфейса IID \_ иевентобжектчанже.

Для поддержки доставки событий нескольким подписчикам методы класса событий должны содержать только параметры in.

С помощью свойства Фиреинпараллел объекта [класса событий](the-com--event-class-object.md) издатели могут запросить, чтобы система событий использовала несколько потоков для доставки события нескольким подписчикам. Выбор параллельного механизма доставки не гарантирует одновременной доставки события нескольким подписчикам, но он указывает службе событий COM+ сделать это.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Публикация и доставка событий в COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
