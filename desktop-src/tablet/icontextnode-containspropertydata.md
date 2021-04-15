---
description: Определяет, содержит ли объект Иконтекстноде данные, хранящиеся по указанному идентификатору.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'Метод Иконтекстноде:: Контаинспропертидата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497589"
---
# <a name="icontextnodecontainspropertydata-method"></a>Метод Иконтекстноде:: Контаинспропертидата

Определяет, содержит ли объект [**иконтекстноде**](icontextnode.md) данные, хранящиеся по указанному идентификатору.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппропертидатаид* \[ окне\]
</dt> <dd>

Идентификатор данных.

</dd> <dt>

*пбконтаинс* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если объект [**иконтекстноде**](icontextnode.md) содержит данные, хранящиеся по указанному идентификатору; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Кроме данных, относящихся к конкретному приложению, этот метод можно использовать для определения того, содержит ли [**иконтекстноде**](icontextnode.md) другие внутренние данные (см. раздел свойства указания по [анализу](analysis-hint-properties.md) и [Свойства узла контекста](context-node-properties.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Иконтекстноде:: Аддпропертидата**](icontextnode-addpropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидата**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидатаидс**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Иконтекстноде:: Лоадпропертиесдата**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**Иконтекстноде:: Ремовепропертидата**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Савепропертиесдата**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




