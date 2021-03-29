---
description: Создает новый дочерний объект Иконтекстноде.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'Метод Иконтекстноде:: Креатесубноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897489"
---
# <a name="icontextnodecreatesubnode-method"></a>Метод Иконтекстноде:: Креатесубноде

Создает новый дочерний объект [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнодетипе* \[ окне\]
</dt> <dd>

**Идентификатор GUID** , представляющий тип создаваемого [**иконтекстноде**](icontextnode.md) .

</dd> <dt>

*ппконтекстнодекреатед* \[ заполняет\]
</dt> <dd>

Указатель на новый [**иконтекстноде**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстнодекреатед* , когда больше не нужно использовать контекстный узел.

 

Новый [**иконтекстноде**](icontextnode.md) добавляется в коллекцию дочерних узлов этого узла контекста (см. раздел [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)). При наличии существующих дочерних узлов вновь созданный **иконтекстноде** добавляется в качестве последнего дочернего узла.

Список типов узлов контекста см. в разделе [типы узлов контекста](context-node-types.md).

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

[**Иконтекстноде::D Елетесубноде**](icontextnode-deletesubnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

