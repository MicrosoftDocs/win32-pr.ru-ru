---
title: Метод Куерйоффлинеинформатион класса Win32_TSVm
description: Извлекает свойства текущего сервера виртуальных рабочих столов (VDS), но только в том случае, если сервер находится в автономном режиме.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Куерйоффлинеинформатион
- Службы удаленных рабочих столов метода Куерйоффлинеинформатион, класс Win32_TSVm
- Класс Win32_TSVm службы удаленных рабочих столов, метод Куерйоффлинеинформатион
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892197"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a>Метод Куерйоффлинеинформатион \_ класса Win32 тсвм

Извлекает свойства текущего сервера виртуальных рабочих столов (VDS), но только в том случае, если сервер находится в автономном режиме.

## <a name="syntax"></a>Синтаксис


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сборка* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает версию сборки VDS.

</dd> <dt>

*CurrentVersion* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает текущую версию VDS.

</dd> <dt>

*Инсталлатионтипе* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает тип установки VDS.

</dd> <dt>

*EditionId* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает идентификатор выпуска VDS.

</dd> <dt>

*Сиспрепимажестате* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает состояние образа подготовки системы для службы VDS.

</dd> <dt>

*Сиспрепмоде* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает режим системной подготовки службы VDS.

</dd> <dt>

*Прокарч* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает значение, указывающее архитектуру процессора.

<dt>

0
</dt> <dd>

x86

</dd> <dt>

1
</dt> <dd>

amd64

</dd> </dl> </dd> <dt>

*фисвмбускапабле* \[ заполняет\]
</dt> <dd>

При успешном выполнении указывает, поддерживает ли система VMBus.

</dd> <dt>

*фисрдвиЦинсталлед* \[ заполняет\]
</dt> <dd>

При успешном выполнении указывает, установлен ли РДВИК.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                             |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                   |
| MOF<br/>                      | <dl> <dt>Тсвмхост. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсвм Win32**](win32-tsvm.md)
</dt> </dl>

 

 





