---
title: Метод Чанжезонетипе класса MicrosoftDNS_Zone
description: Метод Чанжезонетипе изменяет тип зоны.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- DNS-метод Чанжезонетипе
- Чанжезонетипе метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Чанжезонетипе
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071502"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a>Метод Чанжезонетипе \_ класса зоны микрософтднс

Метод **чанжезонетипе** изменяет тип зоны.

## <a name="syntax"></a>Синтаксис


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ZoneType* \[ окне\]
</dt> <dd>

Тип зоны. Допустимы следующие значения.



| Значение                                                                        | Значение                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl> | Основная зона.<br/>   |
| <dl> <dt>1</dt> </dl> | Дополнительная зона.<br/> |
| <dl> <dt>2</dt> </dl> | Зона-заглушка.<br/>      |
| <dl> <dt>3</dt> </dl> | Сервер пересылки зоны.<br/> |



 

</dd> <dt>

*Имя файла* \[ в необязательное\]
</dt> <dd>

Имя файла данных, связанного с зоной.

</dd> <dt>

*Reduce* \[ в необязательное\]
</dt> <dd>

IP-адрес DNS-сервера главном для зоны.

</dd> <dt>

*Админемаилнаме* \[ в необязательное\]
</dt> <dd>

Адрес электронной почты администратора, ответственного за зону.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

RR типа **микрософтднс \_ Zone**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зона микрософтднс**](microsoftdns-zone.md)
</dt> <dt>

[**Метод Ажеаллрекордс \_ класса зоны микрософтднс**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Метод Креатезоне \_ класса зоны микрософтднс**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Метод Форцерефреш \_ класса зоны микрософтднс**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Метод Жетдистингуишеднаме \_ класса зоны микрософтднс**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Метод Паусезоне \_ класса зоны микрософтднс**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Метод Релоадзоне \_ класса зоны микрософтднс**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Метод Ресетсекондариес \_ класса зоны микрософтднс**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Метод Ресумезоне \_ класса зоны микрософтднс**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Метод Упдатефромдс \_ класса зоны микрософтднс**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Метод Вритебаккзоне \_ класса зоны микрософтднс**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





