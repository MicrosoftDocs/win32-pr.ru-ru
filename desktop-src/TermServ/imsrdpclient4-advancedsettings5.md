---
title: IMsRdpClient4 AdvancedSettings5, свойство
description: Получает указатель на интерфейс IMsRdpClientAdvancedSettings4.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings5
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb8efd8fae25be768a1b758389b5ca7c20a9f3f8b414e62acb865fecf83eeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138957"
---
# <a name="imsrdpclient4advancedsettings5-property"></a>Свойство IMsRdpClient4:: AdvancedSettings5

Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a>Значение свойства

Указатель на интерфейс [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) . Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="remarks"></a>Remarks

Это свойство не может быть задано, если элемент управления подключен.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows сервер 2008, Windows server 2008 с пакетом обновления 1<br/>                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClient4 определяется как 095E0738-D97D-488b-B9F6-DD0E8D66C0DE<br/>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

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

 

 





