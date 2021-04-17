---
title: IMsRdpClientAdvancedSettings2 Енаблеаутореконнект, свойство
description: Указывает, следует ли включить клиентский элемент управления для автоматического подключения к сеансу в случае отключения от сети.
ms.assetid: 9d820f78-bf7f-479a-ae6f-be0f0abe549c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Енаблеаутореконнект
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.put_EnableAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8d4a1345395b5b5843872df256fe7a113094e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681977"
---
# <a name="imsrdpclientadvancedsettings2enableautoreconnect-property"></a>Свойство IMsRdpClientAdvancedSettings2:: Енаблеаутореконнект

Указывает, следует ли включить клиентский элемент управления для автоматического подключения к сеансу в случае отключения от сети.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_EnableAutoReconnect(
  [in]  VARIANT_BOOL fEnableAutoReconnect
);

HRESULT get_EnableAutoReconnect(
  [out] VARIANT_BOOL *pfEnableAutoReconnect
);
```



## <a name="property-value"></a>Значение свойства

Задайте значение **\_ true** , чтобы включить автоматическое повторное подключение, и выберите **вариант \_ false** , чтобы отключить его. Значение по умолчанию — **Variant \_ true**.

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Это свойство не может быть задано, если элемент управления подключен.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 определен как 9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





