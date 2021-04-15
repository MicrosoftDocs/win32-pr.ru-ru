---
title: Метод Ажеаллрекордс класса MicrosoftDNS_Zone
description: Метод Ажеаллрекордс включает устаревание для некоторых или всех записей, отличных от NS и не являющихся SOA, в зоне.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- DNS-метод Ажеаллрекордс
- Ажеаллрекордс метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Ажеаллрекордс
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492369"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a>Метод Ажеаллрекордс \_ класса зоны микрософтднс

Метод **ажеаллрекордс** включает устаревание для некоторых или всех записей, отличных от NS и не являющихся SOA, в зоне.

## <a name="syntax"></a>Синтаксис


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*NodeName* \[ в необязательное\]
</dt> <dd>

Имя узла, которому будет присвоено значение Age.

</dd> <dt>

*Апплитосубтри* \[ в необязательное\]
</dt> <dd>

Указывает, следует ли применять устаревание ко всем записям в поддереве. Задайте значение TRUE, чтобы применить устаревание ко всем записям в поддереве, начиная с NodeName.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Ошибка \_ указывает, что устаревание успешно завершено. Любое другое значение является кодом ошибки.

## <a name="remarks"></a>Комментарии

Если значение *nodeName* не указано, все записи будут подвергаться старению и очистке.

Если указан параметр *nodeName* и параметр *апплитосубтри* не задан или равен нулю, записи на указанном узле будут подвергаться старению и очистке.

Если задан параметр *nodeName* и для *апплитосубтри* задано значение 1, то все записи поддерева, начинающиеся с *nodeName* , будут подвергаться старению и очистке. В качестве метки времени задано текущее время для всех записей, не являющихся записями NS и не являющихся SOA, с именами владельцев, определяемыми входными параметрами.

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

[**Метод Чанжезонетипе \_ класса зоны микрософтднс**](microsoftdns-zone-changezonetype.md)
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

 

 





