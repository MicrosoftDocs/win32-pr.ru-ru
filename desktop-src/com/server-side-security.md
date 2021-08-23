---
title: Безопасность Server-Side
description: Безопасность Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7349b318361cfd27969817ec6be9d16accacd29dce625f572a51a7b3bc8082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611014"
---
# <a name="server-side-security"></a>Безопасность Server-Side

Сервер может получать сведения о безопасности вызывающего объекта или олицетворять вызывающий объект с помощью методов [**исерверсекурити**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity). Реализация **исерверсекурити** предоставляется COM в объекте контекста для текущего вызова при использовании стандартного маршалирования. Однако этот интерфейс может отсутствовать для некоторых пользовательских интерфейсов, которые маршалируются.

При поступлении вызова на сервер сервер может вызвать [**кожеткаллконтекст**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) , чтобы получить указатель на интерфейс [**исерверсекурити**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) . С помощью этого указателя методы **исерверсекурити** могут вызываться сервером для определения параметров проверки подлинности клиента и олицетворения клиента при необходимости. Объект **исерверсекурити** действителен в любом потоке в подразделении до тех пор, пока не завершится вызов, представленный параметром **исерверсекурити** . Дополнительные сведения об олицетворении см. в разделе [олицетворение](impersonation.md) и [маскировка](cloaking.md).

Также доступны следующие вспомогательные функции, зависящие от реализации интерфейса [**исерверсекурити**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) в объекте контекста вызова.

-   [**кокуериклиентбланкет**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**коимперсонатеклиент**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**кореверттоселф**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Безопасность в COM](security-in-com.md)
</dt> </dl>

 

 