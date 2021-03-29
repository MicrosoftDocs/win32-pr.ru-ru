---
description: Уведомляет объект о том, что он должен отобразить его построитель для указанного свойства.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'Метод Ипровидепропертибуилдер:: Ексекутебуилдер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648001"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>Метод Ипровидепропертибуилдер:: Ексекутебуилдер

Уведомляет объект о том, что он должен отобразить его построитель для указанного свойства.

## <a name="syntax"></a>Синтаксис


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор DISPID* \[ окне\]
</dt> <dd>

DISPID свойства, для которого отображается конструктор.

</dd> <dt>

*бстргуидблдр* \[ окне\]
</dt> <dd>

Значение **BSTR** СОЗДАВАЕМОГО идентификатора GUID построителя. Возвращается из [**маптопропертибуилдер**](iprovidepropertybuilder-mappropertytobuilder.md).

</dd> <dt>

*пдиспапп* \[ окне\]
</dt> <dd>

Задайте **значение NULL**.

</dd> <dt>

*хвндблдровнер* \[ окне\]
</dt> <dd>

Маркер родительского всплывающего окна построителя.

</dd> <dt>

*сервер* \[ в, out\]
</dt> <dd>

Текущее значение свойства. Это значение может быть изменено объектом и меняется на новое значение, если *пбактионкоммиттед* имеет **значение true**.

</dd> <dt>

*пбактионкоммиттед* \[ out, retval\]
</dt> <dd>

Значение, указывающее, выполнил ли построитель действие над объектом. Может использоваться, когда пользователь изменяет что-либо, а затем нажимает кнопку ОК во всплывающем диалоговом окне построителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ипровидепропертибуилдер**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




