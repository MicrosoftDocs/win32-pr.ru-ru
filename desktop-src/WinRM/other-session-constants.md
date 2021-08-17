---
title: Другие константы сеанса (Всмандисп. h)
description: Укажите кодировку, шифрование и порт имени субъекта-службы.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcd9d2cf44063dfb1a7ec1bfcbb0fe785d1747d34e84ef2c2d8c78598e6e6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743329"
---
# <a name="other-session-constants"></a>Другие константы сеанса

Константы, перечисленные в следующем списке, в перечислении **\_ \_ всмансессионфлагс** , в которых указываются кодировка, шифрование и порт имени субъекта-службы.

<dl> <dt>

<span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Отправляет запрос в кодировке UTF8, а не в UTF16.

Связанный метод создания скриптов — это [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) , а метод C++ — [**ивсманекс. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**всманфлагноенкриптион**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Не шифровать сообщения, отправляемые по сети. Этот параметр разрешается, только если [*прослушиватель*](windows-remote-management-glossary.md) настроен таким образом, чтобы **алловуненкриптед** было установлено значение **true**.

Связанный метод создания скриптов — это [**WSMan. сессионфлагноенкриптион**](wsman-sessionflagnoencryption.md) , а метод C++ — [**ивсманекс. сессионфлагноенкриптион**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**всманфлаженаблеспнсерверпорт**
</dt> <dd> <dl> <dt>

4194304 (0x400000)
</dt> <dt>



Укажите порт имени субъекта-службы (SPN) при подключении непосредственно к удаленному оборудованию BMC, также известному как подключение по внешнему [*каналу*](windows-remote-management-glossary.md) . Поскольку как компьютер сервера WinRM, так и оборудование BMC могут совместно использовать один и тот же IP-адрес, этот флаг указывает на то, что для определения того, подключено ли соединение к службе или напрямую к BMC, должен использоваться номер порта SPN. Дополнительные сведения см. в разделе [форматы имен для уникальных имен участников-служб](/windows/desktop/AD/name-formats-for-unique-spns).

Связанный метод создания скриптов — это [**WSMan. сессионфлаженаблеспнсерверпорт**](wsman-sessionflagenablespnserverport.md) , а метод C++ — [**ивсманекс. сессионфлаженаблеспнсерверпорт**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**
</dt> <dd> <dl> <dt>

0x800000
</dt> <dt>



Отправляет запрос в UTF16.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы сеанса](session-constants.md)
</dt> </dl>

 

