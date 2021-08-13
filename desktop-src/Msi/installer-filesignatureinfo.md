---
description: Метод Филесигнатуреинфо объекта Installer принимает путь к файлу и возвращает SAFEARRAY байтов, представляющих хэш-код или закодированный сертификат.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Метод Installer. Филесигнатуреинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 670b5ba6deb4a53429180e832c2a49e4968c53efbe7c54cdf50e62e20bf5503b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630785"
---
# <a name="installerfilesignatureinfo-method"></a>Метод Installer. Филесигнатуреинфо

Метод **филесигнатуреинфо** объекта [**Installer**](installer-object.md) принимает путь к файлу и возвращает SAFEARRAY байтов, представляющих хэш-код или закодированный сертификат. Затем значения можно использовать для заполнения таблиц [мсидигиталсигнатуре](msidigitalsignature-table.md), [мсипатчцертификате](msipatchcertificate-table.md)и [мсидигиталцертификате](msidigitalcertificate-table.md) .

Дополнительные сведения см. в разделе [**тип данных SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).

## <a name="syntax"></a>Синтаксис


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Равно* 
</dt> <dd>

Полный путь к файлу с цифровой подписью.

При заполнении таблиц [мсидигиталсигнатуре](msidigitalsignature-table.md) и [мсидигиталцертификате](msidigitalcertificate-table.md) *FilePath* указывает на CAB-файл с цифровой подписью. При заполнении таблиц [мсипатчцертификате](msipatchcertificate-table.md) и мсидигиталцертификате *FilePath* указывает на исправление с цифровой подписью.

</dd> <dt>

*Параметры* 
</dt> <dd>

Специальные флаги регистра ошибок.



| Флаг                                                                                                                                                                                                                                                                                                                                    | Значение                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**мсисигнатуреоптионинвалидхашфатал**</dt> <dt>1</dt> </dl> | Если *параметр* with имеет значение Мсисигнатуреоптионинвалидхашфатал, **филесигнатуреинфо** всегда возвращает неустранимую ошибку для недопустимого хэша. <br/> Если для *параметров* не задано значение мсисигнатуреоптионинвалидхашфатал, а параметр *Format* имеет значение мсисигнатуреинфоцертификате, **филесигнатуреинфо** не возвращает ошибку для недопустимого хэша.<br/> |



 

</dd> <dt>

*Формат* 
</dt> <dd>

Запрошенные сведения о подписи.



| Флаг                                                                                                                                                                                                                                                                                                        | Значение                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**мсисигнатуреинфоцертификате**</dt> <dt>0</dt> </dl> | Возвращает SAFEARRAY байт, представляющих закодированный сертификат.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**мсисигнатуреинфохаш**</dt> <dt>1</dt> </dl>                             | Возвращает SAFEARRAY байтов, представляющих хэш.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения метод возвращает [массив SafeArray](/windows/win32/api/oaidl/ns-oaidl-safearray) байтов, который содержит хэш-или закодированный сертификат.

## <a name="remarks"></a>Remarks

Чтобы создать полностью проверенную установку с помощью автоматизации, используйте метод **филесигнатуреинфо** для заполнения таблиц [мсидигиталцертификате](msidigitalcertificate-table.md), [мсипатчцертификате](msipatchcertificate-table.md)и [мсидигиталсигнатуре](msidigitalsignature-table.md) . Дополнительные сведения см. [в статье Создание полностью проверенной подписанной установки с помощью службы автоматизации](authoring-a-fully-verified-signed-installation-using-automation.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание полностью проверенной подписанной установки с помощью службы автоматизации](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[цифровые подписи и установщик Windows](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**мсижетфилесигнатуреинформатион**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
