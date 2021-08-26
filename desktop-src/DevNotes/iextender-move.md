---
description: Перемещает Мдиформ, форму или элемент управления.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: 'Метод Иекстендер:: Move'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender.Move
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: 13002457952490588fa9e9ad40e7f66e7d31465b74f9757a3193ccaed1e8bf7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002104"
---
# <a name="iextendermove-method"></a>Метод Иекстендер:: Move

Перемещает Мдиформ, форму или элемент управления.

## <a name="syntax"></a>Синтаксис


```C++
void Move(
  [in] object left,
  [in] object top,
  [in] object width,
  [in] object height
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

по *левому краю* \[ окне\]
</dt> <dd>

Левая граница формы или элемента управления.

</dd> <dt>

в *Начало* \[ окне\]
</dt> <dd>

Верхняя граница формы или элемента управления.

</dd> <dt>

*Ширина* \[ окне\]
</dt> <dd>

Ширина формы или элемента управления.

</dd> <dt>

*Высота* \[ окне\]
</dt> <dd>

Высота формы или элемента управления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иекстендер**](iextender.md)
</dt> </dl>

 

 




