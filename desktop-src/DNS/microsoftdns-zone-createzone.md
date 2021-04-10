---
title: Метод Креатезоне класса MicrosoftDNS_Zone
description: Метод Креатезоне создает зону DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- DNS-метод Креатезоне
- Креатезоне метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Креатезоне
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071800"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a>Метод Креатезоне \_ класса зоны микрософтднс

Метод **креатезоне** создает зону DNS.

## <a name="syntax"></a>Синтаксис


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя_зоны* \[ окне\]
</dt> <dd>

Строка, представляющая имя зоны.

</dd> <dt>

*ZoneType* \[ окне\]
</dt> <dd>

Тип зоны. Допустимы следующие значения.



| Значение                                                                        | Значение                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>1</dt> </dl> | Интегрированная служба AD.<br/>                                                                                           |
| <dl> <dt>2</dt> </dl> | Дополнительная зона.<br/>                                                                                          |
| <dl> <dt>3</dt> </dl> | Зона-заглушка.<br/> **Windows Server 2003:** Этот тип зоны появился в Windows Server 2003.<br/>      |
| <dl> <dt>4</dt> </dl> | Сервер пересылки зоны.<br/> **Windows Server 2003:** Этот тип зоны появился в Windows Server 2003.<br/> |



 

</dd> <dt>

*Дсинтегратед* \[ окне\]
</dt> <dd>

Указывает, хранятся ли данные зоны в Active Directory или в файлах. Если значение — TRUE, данные хранятся в Active Directory; Если значение равно FALSE, данные хранятся в файлах.

</dd> <dt>

*Имя файла* \[ в необязательное\]
</dt> <dd>

Имя файла данных, связанного с зоной.

</dd> <dt>

*Reduce* \[ в необязательное\]
</dt> <dd>

IP-адрес главного DNS-сервера зоны.

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

[**Метод Чанжезонетипе \_ класса зоны микрософтднс**](microsoftdns-zone-changezonetype.md)
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

 

 





