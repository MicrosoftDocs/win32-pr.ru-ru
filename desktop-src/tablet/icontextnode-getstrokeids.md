---
description: Извлекает массив идентификаторов для штрихов в объекте Иконтекстноде.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'Метод Иконтекстноде:: Жетстрокеидс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ebe66d514b20fc558adce39c013cf559fbc63bb38f772bff73b0819c10426960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967375"
---
# <a name="icontextnodegetstrokeids-method"></a>Метод Иконтекстноде:: Жетстрокеидс

Извлекает массив идентификаторов для штрихов в объекте [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулстрокеидскаунт* \[ в, out\]
</dt> <dd>

Число штрихов. Передаваемое значение не используется.

</dd> <dt>

*пплстрокес* \[ заполняет\]
</dt> <dd>

Указатель на массив идентификаторов Stroke для данного объекта [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *пплстрокес* , если эта информация больше не нужна.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Иконтекстноде:: Жетстрокеид**](icontextnode-getstrokeid.md)
</dt> <dt>

[**Иконтекстноде:: Жетстрокекаунт**](icontextnode-getstrokecount.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

