---
title: Методы свойств Иадшолд (iAds. h)
description: Метод свойства интерфейса Иадшолд задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадшолд ADSI
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fae4d5f5a83577d297bfea6e109d78ad3d8bd2291cfa028f37fb8ab1a4f825b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179562"
---
# <a name="iadshold-property-methods"></a>Методы свойств Иадшолд

Метод свойства интерфейса [**иадшолд**](/windows/desktop/api/Iads/nn-iads-iadshold) задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Сумма**
</dt> <dd> <dl>

Сумма расходов, взимаемых по отношению к пользователю за период удержания, в то время как сервер проверяет баланс учетной записи пользователя.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

**ObjectName**
</dt> <dd> <dl>

Имя объекта, представляющего пользователя при удержании.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадшолд определен как B3EB3B37-4080-11D1-A3AC-00C04FB950DC<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





