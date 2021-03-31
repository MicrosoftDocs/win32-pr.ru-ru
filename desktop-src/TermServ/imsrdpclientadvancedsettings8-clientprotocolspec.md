---
title: IMsRdpClientAdvancedSettings8 Клиентпротоколспек, свойство
description: Указывает протокол удаленного рабочего стола, используемый между клиентом и сервером.
ms.assetid: DD607D54-CAEA-43EE-94EB-F983AEA0CC1E
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Клиентпротоколспек
- Службы удаленных рабочих столов свойства Клиентпротоколспек, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Клиентпротоколспек
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8.ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.get_ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.put_ClientProtocolSpec
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e603f7587435b3701ec0511587286e1a38bcc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988340"
---
# <a name="imsrdpclientadvancedsettings8clientprotocolspec-property"></a>Свойство IMsRdpClientAdvancedSettings8:: Клиентпротоколспек

Указывает протокол удаленного рабочего стола, используемый между клиентом и сервером.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ClientProtocolSpec(
  [in]  ClientSpec ClientMode
);

HRESULT get_ClientProtocolSpec(
  [out] ClientSpec *pClientMode
);
```



## <a name="property-value"></a>Значение свойства

Значение перечисления [**клиентспек**](clientspec.md) , указывающее протокол удаленного рабочего стола, используемый между клиентом и сервером.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**клиентспек**](clientspec.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





