---
title: Асинхронные и синхронные моникеры
description: Асинхронные и синхронные моникеры
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c631c669d73796d1596f52ab2ec6e724829ea80e6873523c1e9bd4f8ad567f09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071120"
---
# <a name="asynchronous-and-synchronous-monikers"></a>Асинхронные и синхронные моникеры

Клиент стандартного, синхронного моникера OLE обычно создает и содержит ссылку на моникер, а также контекст привязки, используемый во время привязки. Компоненты, участвующие в использовании традиционных моникеров, показаны на следующей схеме.

![Схема, на которой показан клиент, подключенный к контексту привязки или любому моникеру, предоставляемому системой.](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

Обычно клиенты создают стандартные специальные имена, вызывая такие функции, как [**креатефилемоникер**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker), [**креатеитеммоникер**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)или [**креатепоинтермоникер**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) , так как они могут быть сохранены в постоянное хранилище с помощью [**олесаветостреам**](/windows/desktop/api/ole/nf-ole-olesavetostream) и [**олелоадфромстреам**](/windows/desktop/api/ole/nf-ole-oleloadfromstream). Моникеры также можно получить из объекта-контейнера, вызвав метод [**ибиндхост:: креатемоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) . Клиенты создают контексты привязки путем вызова функции [**креатебиндкткс**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) , а затем передают контекст привязки моникеру с вызовами [**IMoniker:: биндтостораже**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) или [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).

Как показано на следующей схеме, клиент асинхронного моникера также создает и хранит ссылку на моникер и контекст привязки, используемые во время привязки.

![Схема, на которой показаны подключения между предоставленными клиентом, Монкер и предоставляемыми системой.](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

Чтобы получить асинхронное поведение, клиент реализует интерфейс [**метода интерфейса IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) в объекте обратного вызова состояния привязки и вызывает функцию [**Регистербиндстатускаллбакк**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) или функцию [**креатеасинкбиндкткс**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) для регистрации этого интерфейса в контексте привязки. Моникер передает указатель на свой интерфейс [**ибиндинг**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) в вызове метода [**метода интерфейса IBindStatusCallback:: онстартбиндинг**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) . Клиент сообщает асинхронному моникеру, как он хочет выполнить привязку при возврате из вызова метода [**метода интерфейса IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) в моникере.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Асинхронные моникеры](asynchronous-monikers.md)
</dt> </dl>

 

 