---
title: Интерфейсы хранилища
description: Интерфейсы хранилища
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab06d8d0920ca7b29619df2173aaa0897c6eef6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533536"
---
# <a name="storage-interfaces"></a>Интерфейсы хранилища

Контейнеры элементов управления должны поддерживать элементы управления, реализующие [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)или [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). При необходимости контейнер может поддерживать любые другие интерфейсы сохраняемости, такие как [**иперсистмемори**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))и [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , для этих элементов управления, которые обеспечивают поддержку.

После того как контейнер элементов управления ActiveX выбрал и инициализировал интерфейс хранения для использования ([**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)и т. д.), этот интерфейс хранилища останется основным интерфейсом хранилища для жизненного цикла элемента управления, т. е. Этот элемент управления останется в хранилище. Это не исключает сохранение контейнера в других интерфейсах хранилища.

Контейнерам элементов управления ActiveX не требуется поддерживать механизм "Сохранить как текст", поэтому использование [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) и связанного с ним интерфейса [**ипропертибаг**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) не являются обязательными.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Контейнеры](containers.md)
</dt> </dl>

 

 