---
title: DRM_Flags
description: '\_Свойство Flags DRM используется с содержимым DRM версии 1 только для указания прав, которые будут содержаться в локальной лицензии.'
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags формат Windows Media
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf4f1b2065eb1b251f0c555f8c33e424e43aefd04377ed894edb90c121aacb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086015"
---
# <a name="drm_flags"></a>\_Флаги DRM

Свойство **\_ flags DRM** используется с содержимым DRM версии 1 только для указания прав, которые будут содержаться в локальной лицензии. Права указываются со значениями, определенными типом перечисления **\_ Rights ВМТ** . Можно выбрать более одного значения, объединив их с оператором побитового **или** .

## <a name="global-constant"></a>Глобальная константа

\_всзвмдрм \_ Флаги g

## <a name="data-type"></a>Тип данных

**ВМТ, \_ тип \_ DWORD**

## <a name="remarks"></a>Remarks

При доступе к интерфейсу **IWMHeaderInfo3** объекта Writer можно добавить или изменить это значение. В других объектах (редактор метаданных, читатель и синхронное средство чтения) это значение доступно только для чтения. Используйте [**ивмхеадеринфо:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , чтобы задать это свойство при создании содержимого DRM версии 1.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства DRM**](drm-properties.md)
</dt> </dl>

 

 




