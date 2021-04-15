---
title: Имсрдпклиентсекуредсеттингс Аудиоредиректионмоде, свойство
description: Задает параметры перенаправления звука, указывающие, следует ли перенаправлять звуки или воспроизводить звуки на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Аудиоредиректионмоде
- Службы удаленных рабочих столов свойства Аудиоредиректионмоде, интерфейс Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, свойство Аудиоредиректионмоде
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535570"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a>Свойство Имсрдпклиентсекуредсеттингс:: Аудиоредиректионмоде

Задает параметры перенаправления звука, указывающие, следует ли перенаправлять звуки или воспроизводить звуки на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a>Значение свойства

Новые параметры. Этот параметр может принимать одно из указанных ниже значений.

<dt>

0
</dt> <dd>

Перенаправлять звуки на клиент. Это значение по умолчанию.

</dd> <dt>

1
</dt> <dd>

Воспроизводить звуки на удаленном компьютере.

</dd> <dt>

2
</dt> <dd>

Отключить перенаправление звука; не воспроизводить звуки на сервере.

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

 

 





