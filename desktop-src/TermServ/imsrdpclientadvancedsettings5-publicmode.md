---
title: IMsRdpClientAdvancedSettings5 Публикмоде, свойство
description: Задает или получает конфигурацию для общедоступного режима. Общедоступный режим не позволяет клиенту кэшировать данные пользователя в локальной системе.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Публикмоде
- Службы удаленных рабочих столов свойства Публикмоде, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Публикмоде
- Службы удаленных рабочих столов свойства Публикмоде, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Публикмоде
- Службы удаленных рабочих столов свойства Публикмоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Публикмоде
- Службы удаленных рабочих столов свойства Публикмоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Публикмоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672574"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a>IMsRdpClientAdvancedSettings5: свойство Убликмоде:P

Задает или получает конфигурацию для общедоступного режима. Общедоступный режим не позволяет клиенту кэшировать данные пользователя в локальной системе.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a>Значение свойства

Задает для параметра общего режима значение **Variant \_ true** или **Variant \_ false**. Если задано **значение \_ true**, параметр общего режима включен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





