---
description: Переупорядочивает указанный дочерний объект Иконтекстноде по указанному индексу.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'Метод Иконтекстноде:: Мовесубнодетопоситион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692435"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>Метод Иконтекстноде:: Мовесубнодетопоситион

Переупорядочивает указанный дочерний объект [**иконтекстноде**](icontextnode.md) по указанному индексу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псубнодетомове* \[ окне\]
</dt> <dd>

Перемещаемый объект [**иконтекстноде**](icontextnode.md) .

</dd> <dt>

*улневиндекс* \[ окне\]
</dt> <dd>

Индекс для новой позиции подузла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Возвращает **E \_ INVALIDARG** , если *псубнодетомове* не является дочерним узлом этого [**иконтекстноде**](icontextnode.md).

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

 

 




