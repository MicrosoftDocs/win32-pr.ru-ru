---
description: Удаляет дочерний элемент Иконтекстноде.
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: 'Иконтекстноде: метод:D Елетесубноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ffcec19e13a3ad885b3b497f80322caf9365c91a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542066"
---
# <a name="icontextnodedeletesubnode-method"></a>Иконтекстноде: метод:D Елетесубноде

Удаляет дочерний элемент [**иконтекстноде**](icontextnode.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекстнодетоделете* \[ окне\]
</dt> <dd>

Удаляемый [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

E \_ INVALIDARG возвращается, если параметр *пконтекстнодетоделете* не является дочерним для этого объекта [**иконтекстноде**](icontextnode.md) .

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

[**Иконтекстноде:: Креатесубноде**](icontextnode-createsubnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




