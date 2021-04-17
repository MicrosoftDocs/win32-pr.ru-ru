---
description: Содержит заголовок глобального списка отзыва (GRL).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Структура GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656093"
---
# <a name="grl_header-structure"></a>\_Структура заголовка GRL

Содержит заголовок глобального списка отзыва (GRL).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**всзидентифиер**
</dt> <dd>

Идентификатор GRL. Значение всегда равно L "МСГРЛ".

</dd> <dt>

**вформатмажор**
</dt> <dd>

Основной номер версии. В настоящее время значение должно быть равно 1.

</dd> <dt>

**вформатминор**
</dt> <dd>

Дополнительный номер версии. В настоящее время значение должно быть равно нулю.

</dd> <dt>

**CreationTime**
</dt> <dd>

Значение **fileTime** , указывающее, когда был создан файл.

</dd> <dt>

**двсекуенценумбер**
</dt> <dd>

Номер версии GRL. В настоящее время значение должно быть не меньше 3

</dd> <dt>

**двфорцеребутверсион**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**двфорцепроцессрестартверсион**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**кбревокатионсектионоффсет**
</dt> <dd>

Смещение в байтах от начала GRL до основного раздела.

</dd> <dt>

**кревокедкернелбинариес**
</dt> <dd>

Число отозванных двоичных файлов ядра, перечисленных в GRL.

</dd> <dt>

**кревокедусербинариес**
</dt> <dd>

Число отозванных двоичных файлов пользовательского режима, указанных в GRL.

</dd> <dt>

**кревокедцертификатес**
</dt> <dd>

Число отозванных сертификатов, перечисленных в GRL.

</dd> <dt>

**ктрустедрутс**
</dt> <dd>

Число доверенных корней, перечисленных в GRL.

</dd> <dt>

**кбекстенсиблесектионоффсет**
</dt> <dd>

Смещение в байтах от начала GRL до расширяемого раздела.

</dd> <dt>

**цекстенсиблинтриес**
</dt> <dd>

Число записей в расширяемом разделе.

</dd> <dt>

**кбреневалсектионоффсет**
</dt> <dd>

Смещение в байтах от начала GRL до раздела продления.

</dd> <dt>

**кревокедкернелбинариреневалс**
</dt> <dd>

Число двоичных продлений ядра, перечисленных в GRL.

</dd> <dt>

**кревокедусербинариреневалс**
</dt> <dd>

Число двоичных продлений пользовательского режима, перечисленных в GRL.

</dd> <dt>

**кревокедцертификатереневалс**
</dt> <dd>

Число продлений сертификатов, перечисленных в GRL.

</dd> <dt>

**кбсигнатурекореоффсет**
</dt> <dd>

Смещение в байтах от начала GRL до базовой сигнатуры раздела.

</dd> <dt>

**кбсигнатурикстоффсет**
</dt> <dd>

Смещение в байтах от начала GRL до сигнатуры расширяемого раздела.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Все целочисленные значения в GRL имеют прямой порядок байтов. Все структуры вычисляются по 1 байтам.

Эта структура не объявлена в заголовке пакета SDK. Чтобы использовать эту структуру, добавьте приведенное здесь объявление в исходный код.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Отзыв сертификата ОПМ](opm-certificate-revocation.md)
</dt> <dt>

[Структуры ОПМ](opm-structures.md)
</dt> </dl>

 

 




