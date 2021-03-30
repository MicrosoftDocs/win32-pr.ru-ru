---
title: Методы свойств Иадсднвисбинари (iAds. h)
description: Метод свойства интерфейса Иадсднвисбинари задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсднвисбинари ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf0398a141596de677d7d1739e84ff7525da9a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136878"
---
# <a name="iadsdnwithbinary-property-methods"></a>Методы свойств Иадсднвисбинари

Метод свойства интерфейса [**иадсднвисбинари**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**бинаривалуе**
</dt> <dd> <dl>

Идентификатор GUID объекта, связанного с различающимся именем.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

**днстринг**
</dt> <dd> <dl>

Строка различающегося имени, связанная с идентификатором GUID объекта.

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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадсднвисбинари определен как 7E99C0A2-F935-11d2-BA96-00C04FB6D0D1<br/>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[**\_DN AD \_ с \_ двоичными данными**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 





