---
title: Методы свойств Иадсднвисстринг (iAds. h)
description: Метод свойства интерфейса Иадсднвисстринг задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсднвисстринг ADSI
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa63a933a6a41eec9e6e55906a940cee650c87b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654622"
---
# <a name="iadsdnwithstring-property-methods"></a>Методы свойств Иадсднвисстринг

Метод свойства интерфейса [**иадсднвисстринг**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**днстринг**
</dt> <dd> <dl>

Строка различающегося имени, связанная со строковым значением.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

**StringValue**
</dt> <dd> <dl>

Строковое значение, связанное с DN объекта.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадсднвисстринг определен как 370DF02E-F934-11d2-BA96-00C04FB6D0D1<br/>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[**\_DN AD \_ со \_ строкой**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 





