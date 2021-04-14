---
title: Имсрдпклиентсекуредсеттингс Кэйбоардхукмоде, свойство
description: Задает параметры перенаправления клавиатуры, определяющие способ и время применения сочетания клавиш Windows (например, ALT + TAB).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Кэйбоардхукмоде
- Службы удаленных рабочих столов свойства Кэйбоардхукмоде, интерфейс Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, свойство Кэйбоардхукмоде
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415169"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>Свойство Имсрдпклиентсекуредсеттингс:: Кэйбоардхукмоде

Задает параметры перенаправления клавиатуры, определяющие способ и время применения сочетания клавиш Windows (например, ALT + TAB).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a>Значение свойства

Новые параметры. Этот параметр может принимать одно из указанных ниже значений.

<dt>

0
</dt> <dd>

Применение сочетаний клавиш только локально на клиентском компьютере.

</dd> <dt>

1
</dt> <dd>

Применение сочетаний клавиш на удаленном сервере.

</dd> <dt>

2
</dt> <dd>

Сочетания клавиш применяются к удаленному серверу только в том случае, если клиент работает в полноэкранном режиме. Это значение по умолчанию.

</dd> </dl>

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Эти свойства не могут быть заданы при соединении элемента управления.

Дополнительные сведения см. в руководстве [по обеспечению безопасности клиента RDP](providing-for-rdp-client-security.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                 |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ имсрдпклиентсекуредсеттингс определен как 605befcf-39c1-45cc-A811-068fb7be346d<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





