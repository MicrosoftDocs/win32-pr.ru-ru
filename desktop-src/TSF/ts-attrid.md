---
title: TS_ATTRID (Текстстор. h)
description: '\_Тип данных TS ATTRID используется для задания текстового атрибута.'
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800988"
---
# <a name="ts_attrid"></a>\_ATTRID TS

Тип данных **TS \_ ATTRID** используется для задания текстового атрибута.


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a>Комментарии

Список стандартных идентификаторов GUID для TS \_ ATTRID находится в тсаттрс. h.

Идентификаторы GUID ТСАТТРИД \_ Text \_ ВЕРТИКАЛВРИТИНГ и тсаттрид \_ \_ полезны для того, чтобы приложения соответствовали вводимому тексту, который должен быть исправлен. Можно создать дополнительные идентификаторы GUID, определяемые пользователем.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Приложения Windows 2000 Professional \[ классические приложения \| UWP\]<br/>                       |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows 2000 \|\]<br/>                             |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                         |
| Header<br/>                   | <dl> <dt>Текстстор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Текстстор. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ITextStoreACP:: Финднекстаттртранситион**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[**ITextStoreACP:: Рекуестаттрсатпоситион**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[**ITextStoreACP:: Рекуестаттрстранситионингатпоситион**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreACP:: Рекуестсуппортедаттрс**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[**ITextStoreACPSink:: Онаттрсчанже**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[**Итекстстореанчор:: Финднекстаттртранситион**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[**Итекстстореанчор:: Рекуестаттрсатпоситион**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[**Итекстстореанчор:: Рекуестаттрстранситионингатпоситион**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[**Итекстстореанчор:: Рекуестсуппортедаттрс**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[**Итекстстореанчорсинк:: Онаттрсчанже**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[**\_АТТРВАЛ TS**](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





