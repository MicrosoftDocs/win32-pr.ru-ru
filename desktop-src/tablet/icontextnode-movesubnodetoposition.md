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
ms.openlocfilehash: 8d48876be10a2c45daca62b3175a358d31ed128ddd3bcb045c052e2d51308c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773824"
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

## <a name="remarks"></a>Remarks

Возвращает **E \_ INVALIDARG** , если *псубнодетомове* не является дочерним узлом этого [**иконтекстноде**](icontextnode.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Иконтекстноде:: Креатесубноде**](icontextnode-createsubnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




