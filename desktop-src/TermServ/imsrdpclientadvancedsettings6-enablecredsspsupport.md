---
title: IMsRdpClientAdvancedSettings6 Енаблекредсспсуппорт, свойство
description: Указывает, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.
ms.assetid: 3BC8A265-7AEA-4C9C-9730-7710E1A3159D
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Енаблекредсспсуппорт
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.put_EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73ad2b024cd0f8bbcafd6ba05be093c5953d54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534142"
---
# <a name="imsrdpclientadvancedsettings6enablecredsspsupport-property"></a>Свойство IMsRdpClientAdvancedSettings6:: Енаблекредсспсуппорт

Указывает, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a>Значение свойства

Указывает, включен ли CredSSP для этого соединения. Установите значение **\_ true** , чтобы включить CredSSP или **вариант \_ false** в противном случае.

## <a name="remarks"></a>Комментарии

Это свойство поддерживается только клиентами подключение к удаленному рабочему столу 6,1 и 7,0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





