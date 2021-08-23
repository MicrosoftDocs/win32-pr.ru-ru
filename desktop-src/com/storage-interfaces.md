---
title: служба хранилища Интерфейс
description: служба хранилища Интерфейс
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c378b37c020f15e0fe497249b2834faffefc232bc184564f80fdb247550033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129706"
---
# <a name="storage-interfaces"></a>служба хранилища Интерфейс

Контейнеры элементов управления должны поддерживать элементы управления, реализующие [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)или [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). При необходимости контейнер может поддерживать любые другие интерфейсы сохраняемости, такие как [**иперсистмемори**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)и [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , для этих элементов управления, которые обеспечивают поддержку.

после того как контейнер элемента управления ActiveX выбрал и инициализировал интерфейс хранения для использования ([**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)и т. д.), этот интерфейс хранения будет оставаться основным интерфейсом хранилища для жизненного цикла элемента управления, т. е. этот элемент управления будет оставаться в доступном хранилище. Это не исключает сохранение контейнера в других интерфейсах хранилища.

контейнерам элементов управления ActiveX не требуется поддерживать механизм "сохранить как текст", поэтому использование [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) и связанного с ним интерфейса [**ипропертибаг**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) не являются обязательными.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Контейнеры](containers.md)
</dt> </dl>

 

 