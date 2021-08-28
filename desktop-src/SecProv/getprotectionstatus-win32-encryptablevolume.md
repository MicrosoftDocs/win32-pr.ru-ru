---
description: Указывает, защищен ли том и его ключ шифрования.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Метод Жетпротектионстатус класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 66fcbcfc4c5f228fde786a6b9d8913cc69c0d341
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471510"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Метод Жетпротектионстатус \_ класса Win32 енкриптаблеволуме

Метод **жетпротектионстатус** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает, защищен ли том и его ключ шифрования (если он есть).

Защита отключена, если том не зашифрован или частично зашифрован, или если ключ шифрования тома доступен на жестком диске в открытом состоянии.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Состояние защиты* \[ заполняет\]
</dt> <dd>

Тип: **UInt32**

Указывает, защищен ли том и ключ шифрования (если он есть).




| Значение | Значение | 
|-------|---------|
| <span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl><dt><strong>Незащищенный</strong></dt><dt>0</dt></dl> | ЗАЩИТА ОТКЛЮЧЕНА<br /> Для стандартного жесткого диска:<br /> Том не зашифрован, частично зашифрован, или ключ шифрования тома доступен в CLEAR на жестком диске. Ключ шифрования можно очистить на жестком диске, если предохранители ключа были отключены с помощью метода <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>дисаблекэйпротекторс</strong></a> или если предохранители ключа не были указаны с помощью следующих методов.<ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>протекткэйвисцертификатефиле</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>протекткэйвисцертификатесумбпринт</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>протекткэйвисекстерналкэй</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>протекткэйвиснумерикалпассворд</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>протекткэйвиспассфрасе</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>протекткэйвистпм</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>протекткэйвистпмандпин</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандпинандстартупкэй</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>протекткэйвистпмандстартупкэй</strong></a></li></ul><br /> Для ЕХДД:<br /> Полоса для тома бессрочно разблокирована, не имеет диспетчера ключей или управляется сторонним диспетчером ключей.<br /> Это также может означать, что Управление полосой осуществляется с помощью BitLocker, но был вызван метод <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>дисаблекэйпротекторс</strong></a> и диск приостановлен.<br /> | 
| <span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl><dt><strong>Защищено</strong></dt><dt>1</dt></dl> | ЗАЩИТА ВКЛЮЧЕНА<br /> Для стандартного жесткого диска:<br /> Том полностью зашифрован, а ключ шифрования для тома недоступен на жестком диске.<br /> Для ЕХДД:<br /> BitLocker является диспетчером ключей для полосы. Диск может быть заблокирован или разблокирован, но не может быть бессрочно разблокирован.<br /> | 
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl><dt><strong>Неизвестно</strong></dt><dt>2</dt></dl> | Невозможно определить состояние защиты тома. Это может быть вызвано тем, что том находится в заблокированном состоянии.<br /><strong>Windows vista Ultimate, Windows vista Enterprise и Windows Server 2008:</strong> Это значение не поддерживается. это значение поддерживается начиная с Windows 7 и Windows Server 2008 R2.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

При сбое этот метод возвращает один из следующих кодов или другой код ошибки.



| Возвращаемый код и значение                                                                                                                                 | Описание                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt> </dl> | Метод успешно выполнен.<br/> |



 

## <a name="remarks"></a>Комментарии

Шифрование тома возможно только в том случае, если вы либо вызываете [**дисаблекэйпротекторс**](disablekeyprotectors-win32-encryptablevolume.md) , либо используете один из следующих методов:

-   [**протекткэйвисцертификатефиле**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**протекткэйвисцертификатесумбпринт**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**протекткэйвиснумерикалпассворд**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**протекткэйвиспассфрасе**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**протекткэйвистпм**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**протекткэйвистпмандпин**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**протекткэйвистпмандпинандстартупкэй**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**протекткэйвистпмандстартупкэй**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Поэтому, если диск зашифрован и *состояние защиты* возвращает ноль (защита отключена), ключи отключаются.

Используйте [**жеткэйпротекторс**](getkeyprotectors-win32-encryptablevolume.md) , чтобы получить список предохранителей ключей, которые были указаны для защиты ключа шифрования тома. Если предохранители ключа существуют, но защита равна нулю (защита ОТКЛЮЧЕНа), используйте [**енаблекэйпротекторс**](enablekeyprotectors-win32-encryptablevolume.md) , чтобы включить защиту тома.

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
</dt> </dl>

 

 
