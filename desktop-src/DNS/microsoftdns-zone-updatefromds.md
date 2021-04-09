---
title: Метод Упдатефромдс класса MicrosoftDNS_Zone
description: Метод Упдатефромдс принудительно обновляет зону из службы каталогов (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- DNS-метод Упдатефромдс
- Упдатефромдс метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Упдатефромдс
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137826"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a>Метод Упдатефромдс \_ класса зоны микрософтднс

Метод **упдатефромдс** принудительно обновляет зону из службы каталогов (DS).

## <a name="syntax"></a>Синтаксис


```mof
void UpdateFromDS();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Для успешного выполнения этого метода ZoneType должен быть равен нулю, а зона должна храниться в DS.

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

[**Метод Вритебаккзоне \_ класса зоны микрософтднс**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





