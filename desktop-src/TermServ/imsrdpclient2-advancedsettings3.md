---
title: IMsRdpClient2 AdvancedSettings3, свойство
description: Получает указатель на интерфейс IMsRdpClientAdvancedSettings2. Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.
ms.assetid: 69353bfa-973e-4c6a-8f7e-1b9514be2539
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings3
- Службы удаленных рабочих столов свойства AdvancedSettings3, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство AdvancedSettings3
- Службы удаленных рабочих столов свойства AdvancedSettings3, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство AdvancedSettings3
- Службы удаленных рабочих столов свойства AdvancedSettings3, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство AdvancedSettings3
- Службы удаленных рабочих столов свойства AdvancedSettings3, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство AdvancedSettings3
- Службы удаленных рабочих столов свойства AdvancedSettings3, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство AdvancedSettings3
- Службы удаленных рабочих столов свойства AdvancedSettings3, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство AdvancedSettings3
- Службы удаленных рабочих столов свойства AdvancedSettings3, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings3
- Службы удаленных рабочих столов свойства AdvancedSettings3, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings3
- Службы удаленных рабочих столов свойства AdvancedSettings3, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient2.AdvancedSettings3
- IMsRdpClient2.get_AdvancedSettings3
- IMsRdpClient3.AdvancedSettings3
- IMsRdpClient3.get_AdvancedSettings3
- IMsRdpClient4.AdvancedSettings3
- IMsRdpClient4.get_AdvancedSettings3
- IMsRdpClient5.AdvancedSettings3
- IMsRdpClient5.get_AdvancedSettings3
- IMsRdpClient6.AdvancedSettings3
- IMsRdpClient6.get_AdvancedSettings3
- IMsRdpClient7.AdvancedSettings3
- IMsRdpClient7.get_AdvancedSettings3
- IMsRdpClient8.AdvancedSettings3
- IMsRdpClient8.get_AdvancedSettings3
- IMsRdpClient9.AdvancedSettings3
- IMsRdpClient9.get_AdvancedSettings3
- IMsRdpClient10.AdvancedSettings3
- IMsRdpClient10.get_AdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 527ed2338c07eb943e6e2a3ef1c6e5f4342f446f0b5eff6a67ff2e3c7035a456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059022"
---
# <a name="imsrdpclient2advancedsettings3-property"></a>Свойство IMsRdpClient2:: AdvancedSettings3

Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_AdvancedSettings3(
  [out] IMsRdpClientAdvancedSettings2 **ppAdvSettings
);
```



## <a name="property-value"></a>Значение свойства

Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="remarks"></a>Remarks

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient2 определен как e7e17dc4-3b71-4ba7-a8e6-281ffadca28f<br/>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





