---
title: DRM_DRMHeader_ContentDistributor
description: Атрибут DRM \_ дрмхеадер \_ контентдистрибутор содержит строку идентифийинг распространителя содержимого.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor формат Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a82e570c43acbe065ec20e1d7296cff701853591759e9187e2b9329ffed8efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586464"
---
# <a name="drm_drmheader_contentdistributor"></a>\_Дрмхеадер \_ контентдистрибутор DRM

Атрибут **DRM \_ дрмхеадер \_ контентдистрибутор** содержит строку идентифийинг распространителя содержимого.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмдрм \_ дрмхеадер \_ контентдистрибутор

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Remarks

ИДЕНТИФИКАТОР содержимого является необязательным и определяется исключительно создателем содержимого. Объект модуля записи не выполняет никаких действий с этим атрибутом. Этот атрибут имеется только в содержимом DRM версии 7. Его можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , и его можно получить при помощи [**Ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>См. также

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




