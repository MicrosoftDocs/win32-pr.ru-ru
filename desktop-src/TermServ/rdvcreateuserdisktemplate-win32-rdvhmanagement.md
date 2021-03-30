---
title: Метод Рдвкреатеусердисктемплате класса Win32_RdvhManagement
description: Создает пользовательский шаблон диска с указанным максимальным размером в указанном расположении.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рдвкреатеусердисктемплате
- Службы удаленных рабочих столов метода Рдвкреатеусердисктемплате, класс Win32_RdvhManagement
- Класс Win32_RdvhManagement службы удаленных рабочих столов, метод Рдвкреатеусердисктемплате
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803616"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a>Метод Рдвкреатеусердисктемплате \_ класса Win32 рдвхманажемент

Создает пользовательский шаблон диска с указанным максимальным размером в указанном расположении.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Усердискссторажеурл* \[ окне\]
</dt> <dd>

Расположение дискового пространства пользователя.

</dd> <dt>

*Усердискмакссизеингб* \[ окне\]
</dt> <dd>

Максимальный размер диска пользователя в ГБ.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Комментарии

Все диски пользователей, созданные с помощью этого шаблона, будут иметь тот же максимальный размер, что и шаблон.

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

[**\_Рдвхманажемент Win32**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





