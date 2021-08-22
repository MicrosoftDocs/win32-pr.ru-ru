---
title: Делегирование QueryInterface
description: Делегирование QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c63a9eb336bcf049877957bd55523ee70de489263bd19e0ebece8b65fbdd0ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501214"
---
# <a name="delegation-of-queryinterface"></a>Делегирование QueryInterface

Обработчики, которым требуется доступ к некоторым внутренним интерфейсам в диспетчере прокси-сервера, должны проходить через интерфейс [**иинтерналункновн**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) . Это предотвращает появление обработчиками скрытого делегирования и доступа к внутренним интерфейсам агрегата за пределами статистической функции. К этим интерфейсам относятся [**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) и [**имултики**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi). Если обработчик хочет предоставить **иклиентсекурити** или **имултики**, он должен реализовать их сами.

В случае с [**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), если клиент пытается установить безопасность интерфейса, предоставленного обработчиком, обработчик должен установить безопасность на базовом прокси-сервере сетевого интерфейса.

В случае с [**имултики**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi)обработчик должен заполнить интерфейсы, о которых он знает, а затем перенаправить вызов диспетчеру прокси-сервера для получения остальных интерфейсов, заполненных.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Упрощенный обработчик Client-Side](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 