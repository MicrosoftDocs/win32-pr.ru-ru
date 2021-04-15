---
title: Методы свойств Иадсемаил (iAds. h)
description: Метод свойства интерфейса Иадсемаил задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсемаил ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415944"
---
# <a name="iadsemail-property-methods"></a>Методы свойств Иадсемаил

Метод свойства интерфейса [**иадсемаил**](/windows/desktop/api/Iads/nn-iads-iadsemail) задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Адрес**
</dt> <dd> <dl>

Адрес электронной почты пользователя.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

**Тип**
</dt> <dd> <dl>

Тип сообщения электронной почты.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
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
| IID<br/>                      | IID \_ иадсемаил определен как 97AF011A-478E-11D1-A3B4-00C04FB950DC<br/>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[**\_Электронная почта ADS**](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 





