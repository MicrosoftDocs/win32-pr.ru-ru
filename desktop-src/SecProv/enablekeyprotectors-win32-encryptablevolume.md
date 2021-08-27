---
description: Включает или возобновляет все отключенные или приостановленные предохранители ключей.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Метод Енаблекэйпротекторс класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d90e37f800a9c224abefb21253f7e74c2bc08401
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474930"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Метод Енаблекэйпротекторс \_ класса Win32 енкриптаблеволуме

Метод **енаблекэйпротекторс** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) включает или возобновляет все отключенные или приостановленные предохранители ключей. Этот метод можно использовать для повторного включения или возобновления защиты BitLocker на зашифрованном томе. Этот метод гарантирует, что ключ шифрования тома не будет предоставлен на очистку на жестком диске.

> [!Note]  
> Если диск поддерживает аппаратное шифрование, состояние полосы изменится на "Разблокировано" из "всегда разблокировано".

 

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

При сбое этот метод возвращает один из следующих кодов или другой код ошибки.

Если предохранители ключа уже включены и другие ошибки не возникают, этот метод возвращает ноль.




| Возвращаемый код и значение | Описание | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | Метод успешно выполнен.<br /> | 
| <dl><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt><dt>2150694919 (0x80310007)</dt></dl> | На томе не существует предохранителей ключа. Чтобы указать предохранители ключа для тома, используйте один из следующих методов.<br /><ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>протекткэйвисцертификатефиле</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>протекткэйвисцертификатесумбпринт</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>протекткэйвисекстерналкэй</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>протекткэйвиспассфрасе</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>протекткэйвистпм</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>протекткэйвистпмандпин</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандпинандстартупкэй</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандстартупкэй</strong></a></li></ul> | 
| <dl><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt><dt>2150694920 (0x80310008)</dt></dl> | Средство BitLocker не включено в томе. Добавьте предохранитель ключа, чтобы включить BitLocker. <br /> | 




 

## <a name="remarks"></a>Комментарии

Если том полностью зашифрован, успешное выполнение этого метода обеспечит защиту тома. Если том является частично зашифрованным, то успешное выполнение этого метода означает, что том будет защищен, когда он станет полностью зашифрован. Дополнительные сведения см. в описании метода [**жетпротектионстатус**](getprotectionstatus-win32-encryptablevolume.md) .

Если для тома существуют предохранители ключей на основе доверенного платформенного модуля, успешное выполнение этого метода также обновляет эти предохранители, чтобы доверенный платформенный модуль проверял соответствие текущим службам запуска на платформе. Иными словами, вы утверждаете, что текущее состояние компьютера является верным состоянием, на которое проверяется доверенный платформенный модуль на будущих перезапусках компьютера.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе Windows SDK. Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows vista Enterprise, \[ только для настольных приложений Windows vista Ultimate\]<br/>                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                    |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ енкриптаблеволуме. mof</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Енкриптаблеволуме Win32**](win32-encryptablevolume.md)
</dt> <dt>

[**дисаблекэйпротекторс**](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[**протекткэйвисцертификатефиле**](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[**протекткэйвисцертификатесумбпринт**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[**протекткэйвиснумерикалпассворд**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[**протекткэйвиспассфрасе**](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[**протекткэйвистпм**](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[**протекткэйвистпмандпин**](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[**протекткэйвистпмандпинандстартупкэй**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[**протекткэйвистпмандстартупкэй**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
