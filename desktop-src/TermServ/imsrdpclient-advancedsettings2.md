---
title: Имсрдпклиент AdvancedSettings2, свойство
description: Получает указатель на интерфейс Имсрдпклиентадванцедсеттингс. Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.
ms.assetid: 207b625c-fc2b-41ad-9339-9f3c3b8eeab7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.AdvancedSettings2
- IMsRdpClient.get_AdvancedSettings2
- IMsRdpClient2.AdvancedSettings2
- IMsRdpClient2.get_AdvancedSettings2
- IMsRdpClient3.AdvancedSettings2
- IMsRdpClient3.get_AdvancedSettings2
- IMsRdpClient4.AdvancedSettings2
- IMsRdpClient4.get_AdvancedSettings2
- IMsRdpClient5.AdvancedSettings2
- IMsRdpClient5.get_AdvancedSettings2
- IMsRdpClient6.AdvancedSettings2
- IMsRdpClient6.get_AdvancedSettings2
- IMsRdpClient7.AdvancedSettings2
- IMsRdpClient7.get_AdvancedSettings2
- IMsRdpClient8.AdvancedSettings2
- IMsRdpClient8.get_AdvancedSettings2
- IMsRdpClient9.AdvancedSettings2
- IMsRdpClient9.get_AdvancedSettings2
- IMsRdpClient10.AdvancedSettings2
- IMsRdpClient10.get_AdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569813dd0f836b74f998e6cad716170e3d6e95464712201c8fa14c98f06fd3d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475854"
---
# <a name="imsrdpclientadvancedsettings2-property"></a>Свойство Имсрдпклиент:: AdvancedSettings2

Получает указатель на интерфейс [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md) . Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_AdvancedSettings2(
  [out] IMsRdpClientAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a>Значение свойства

Указатель на интерфейс [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md) . Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.

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
| IID<br/>                      | IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиент**](imsrdpclient-interface.md)
</dt> <dt>

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

 

 





