---
title: Интерфейсы хранилища
description: Интерфейсы хранилища
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549269"
---
# <a name="storage-interfaces"></a>Интерфейсы хранилища

Контейнеры элементов управления должны поддерживать элементы управления, реализующие [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)или [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). При необходимости контейнер может поддерживать любые другие интерфейсы сохраняемости, такие как [**иперсистмемори**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)и [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , для этих элементов управления, которые обеспечивают поддержку.

После того как контейнер элементов управления ActiveX выбрал и инициализировал интерфейс хранения для использования ([**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)и т. д.), этот интерфейс хранилища останется основным интерфейсом хранилища для жизненного цикла элемента управления, т. е. Этот элемент управления останется в хранилище. Это не исключает сохранение контейнера в других интерфейсах хранилища.

Контейнерам элементов управления ActiveX не требуется поддерживать механизм "Сохранить как текст", поэтому использование [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) и связанного с ним интерфейса [**ипропертибаг**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) не являются обязательными.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Контейнеры](containers.md)
</dt> </dl>

 

 