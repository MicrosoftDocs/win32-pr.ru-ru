---
title: Имстсксекуредсеттингс, свойство полноэкранного режима
description: Задает полноэкранное состояние клиентского элемента управления.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства во весь экран
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс Имстсксекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имстсксекуредсеттингс, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, свойство "во весь экран"
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672833"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a>Свойство Имстсксекуредсеттингс:: полноэкранного режима

Задает полноэкранное состояние клиентского элемента управления.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a>Значение свойства

Задайте для этого параметра **значение true** , если элемент управления должен использовать полноэкранный режим, и **false** в противном случае.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Дополнительные сведения об этом методе см. в разделе [предоставление для безопасности клиента RDP](providing-for-rdp-client-security.md).

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

Обратите внимание, что несмотря на то, что использование этого свойства ограничено разрешенными зонами безопасности URL-адресов Internet Explorer, пользователь всегда может перейти в полноэкранный режим после установки подключения, нажав [сочетание клавиш в полноэкранном режиме (](terminal-services-shortcut-keys.md) Ctrl + Alt + Break).

Этот метод может быть вызван во время установки клиентского соединения.

Необходимо вызвать метод [**IMsRdpClientNonScriptable3::p UT \_ коннектионбартекст**](imsrdpclientnonscriptable3-connectionbartext.md) перед вызовом метода **имстсксекуредсеттингс::p UT \_** , а также метода [**имсрдпклиент::p UT \_**](imsrdpclient-fullscreen.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ имстсксекуредсеттингс определен как c9d65442-a0f9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





