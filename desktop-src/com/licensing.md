---
title: Лицензирование
description: Лицензирование
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3058bd6bb543f2f3fc97f2e6a851b456638128c6e731050237aa0d36b12d681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567744"
---
# <a name="licensing"></a>Лицензирование

для успешного внедрения лицензированных элементов управления ActiveX контейнеры элементов управления должны использовать [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) вместо [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). некоторые вспомогательные функции создания и загрузки OLE ([**олелоад**](/windows/desktop/api/Ole2/nf-ole2-oleload) и [**cocreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) явно вызывают **IClassFactory** , а не **IClassFactory2**, и поэтому не могут использоваться для создания или загрузки лицензированных ActiveX элементов управления. контейнеры элементов управления ActiveX должны явно создавать и загружать ActiveX элементы управления с помощью **IClassFactory2**.

 

 