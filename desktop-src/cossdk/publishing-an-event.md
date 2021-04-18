---
description: Публикация события
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Публикация события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701226"
---
# <a name="publishing-an-event"></a>Публикация события

Чтобы опубликовать событие, просто создайте экземпляр объекта события, вызвав [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) или метод Microsoft Visual Basic **CreateObject** , используя евентклассид или евенткласснаме в качестве аргумента. Издатель вызывает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на объекте события для получения интерфейсов, поддерживаемых объектом класса событий, и вызывает метод для объекта события через интерфейс для публикации события. Затем система событий публикует события в классе событий CLSID \_ евентобжектчанже с ИД интерфейса IID \_ иевентобжектчанже.

Для поддержки доставки событий нескольким подписчикам методы класса событий должны содержать только параметры in.

С помощью свойства Фиреинпараллел объекта [класса событий](the-com--event-class-object.md) издатели могут запросить, чтобы система событий использовала несколько потоков для доставки события нескольким подписчикам. Выбор параллельного механизма доставки не гарантирует одновременной доставки события нескольким подписчикам, но он указывает службе событий COM+ сделать это.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Публикация и доставка событий в COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
