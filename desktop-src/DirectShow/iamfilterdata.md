---
description: Примечание. Этот интерфейс не рекомендуется к использованию.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Интерфейс Иамфилтердата (данные о фай \_ . h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675298"
---
# <a name="iamfilterdata-interface"></a>Интерфейс Иамфилтердата

> [!Note]  
> Этот интерфейс не рекомендуется к использованию. В новых приложениях вместо этого следует использовать интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

 

`IAMFilterData`Интерфейс преобразует сведения о фильтре в Упакованные двоичные данные, которые могут храниться в реестре. Объект сопоставителя фильтров предоставляет этот интерфейс.

## <a name="members"></a>Элементы

Интерфейс **иамфилтердата** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иамфилтердата** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иамфилтердата** содержит следующие методы.



| Метод                                                     | Описание                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**креатефилтердата**](iamfilterdata-createfilterdata.md) | Создает двоичные данные реестра для фильтра.<br/>     |
| [**парсефилтердата**](iamfilterdata-parsefilterdata.md)   | Распаковать двоичные данные реестра для фильтра.<br/> |



 

## <a name="remarks"></a>Комментарии

> [!Note]  
> Заголовок Headers \_ Data. h находится в каталоге с [образцом модуля сопоставления](mapper-sample.md) в Windows SDK.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>\_Данные о данных. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Устаревшие интерфейсы](deprecated-interfaces.md)
</dt> </dl>

 

 
