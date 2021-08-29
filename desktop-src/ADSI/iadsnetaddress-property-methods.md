---
title: Методы свойств Иадснетаддресс (iAds. h)
description: Метод свойства интерфейса Иадснетаддресс задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадснетаддресс ADSI
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b3a6d7076350df339df9c3657635af8aed9ca0ad0dd21638155ff074efca312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961913"
---
# <a name="iadsnetaddress-property-methods"></a>Методы свойств Иадснетаддресс

Метод свойства интерфейса [**иадснетаддресс**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Адрес**
</dt> <dd> <dl>

Сетевой адрес.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

**AddressType**
</dt> <dd> <dl>

Тип протоколов связи.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадснетаддресс определен как B21A50A9-4080-11D1-A3AC-00C04FB950DC<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[**ADS \_ нетаддресс**](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 





