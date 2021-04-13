---
description: Задайте в качестве атрибута для объекта Имфаутпутсчема.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: Атрибут MFPROTECTIONATTRIBUTE_BEST_EFFORT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263898"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a>МФПРОТЕКТИОНАТТРИБУТЕный \_ атрибут с наилучшими \_ усилиями

Задайте в качестве атрибута для объекта [**имфаутпутсчема**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) . Если этот атрибут имеется, неудачная попытка применения защиты игнорируется. Если значение связанного атрибута равно **true**, следует применить схему защиты с атрибутом [мфпротектионаттрибуте \_ отработки отказа \_](mfprotectionattribute-fail-over.md) .

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

Если **значение — true**, принудительно Примените схему защиты с атрибутом [мфпротектионаттрибуте \_ \_ отработки отказа](mfprotectionattribute-fail-over.md) , если установить эту защиту не удается.

Задайте в качестве атрибута для объекта [**имфаутпутсчема**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только приложения UWP Windows 8\]<br/>                                             |
| Минимальная версия сервера<br/> | Только приложения UWP для Windows Server 2012 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




