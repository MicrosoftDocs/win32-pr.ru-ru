---
description: Перемещает этот объект Иконтекстноде из коллекции дочерних узлов родительского узла в указанную коллекцию подузлов узла контекста.
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'Метод Иконтекстноде:: reparent (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072782"
---
# <a name="icontextnodereparent-method"></a>Метод Иконтекстноде:: reparent

Перемещает этот объект [**иконтекстноде**](icontextnode.md) из коллекции дочерних узлов родительского узла в указанную коллекцию подузлов узла контекста.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пневпарент* \[ окне\]
</dt> <dd>

Новый родительский узел для этого объекта [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

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

[**Иконтекстноде:: Жетпарентноде**](icontextnode-getparentnode.md)
</dt> <dt>

[**Иконтекстноде:: Жетсубнодес**](icontextnode-getsubnodes.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




