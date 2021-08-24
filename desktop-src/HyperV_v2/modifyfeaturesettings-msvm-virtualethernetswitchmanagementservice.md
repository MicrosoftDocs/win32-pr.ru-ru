---
description: Изменяет настройки компонентов порта коммутатора Ethernet.
ms.assetid: 8c21a932-fffb-40fd-9166-d7e351329217
title: Метод Модифифеатуресеттингс класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f400ec4ef7318a51fde09defee96112bf2247c897a323509084731974af88d9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694204"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Метод Модифифеатуресеттингс \_ класса Виртуалесернетсвитчманажементсервице мсвм

Изменяет настройки компонентов порта коммутатора Ethernet.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ModifyFeatureSettings(
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Феатуресеттингс* \[ окне\]
</dt> <dd>

Массив строк, содержащий встроенный экземпляр класса, производного от класса [**мсвм \_ феатуресеттингдата**](msvm-featuresettingdata.md) , который описывает изменяемые параметры функции порта коммутатора.

</dd> <dt>

*Ресултингфеатуресеттингс* \[ заполняет\]
</dt> <dd>

Массив ссылок на экземпляры класса [**мсвм \_ феатуресеттингдата**](msvm-featuresettingdata.md) , представляющие измененные параметры функции.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Сбой** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Недопустимый параметр** (4)
</dt> <dt>

**Недопустимое состояние** (5)
</dt> <dt>

**Несовместимые параметры** (6)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**аддфеатуресеттингс**](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**ремовефеатуресеттингс**](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**Мсвм \_ виртуалесернетсвитчманажементсервице**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

