---
title: Метод Реактиватесервераутоматик класса Win32_TSLicenseServer
description: Повторно активирует сервер лицензий удаленный рабочий стол, используя автоматическое подключение к Интернету.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Реактиватесервераутоматик
- Службы удаленных рабочих столов метода Реактиватесервераутоматик, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Реактиватесервераутоматик
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e822c441410ae3757f7cdb0a4a714b435facbb20e171646c889e2ea53ec82b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866044"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Метод Реактиватесервераутоматик \_ класса Win32 тслиценсесервер

Повторно активирует сервер лицензий удаленный рабочий стол, используя автоматическое подключение к Интернету.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Причина* \[ окне\]
</dt> <dd>

Причина активации. Может быть одним из указанных далее.

<dt>

0
</dt> <dd>

Сервер был повторно развернут.

</dd> <dt>

1
</dt> <dd>

Сертификат поврежден.

</dd> <dt>

2
</dt> <dd>

Закрытый ключ скомпрометирован.

</dd> <dt>

3
</dt> <dd>

Срок действия ключа активации истек.

</dd> <dt>

4
</dt> <dd>

Сервер был обновлен.

</dd> </dl> </dd> <dt>

*ActivationStatus* \[ заполняет\]
</dt> <dd>

Возвращенное состояние активации может иметь одно из следующих значений.

<dt>

0
</dt> <dd>

Сервер лицензий удаленный рабочий стол активирован.

</dd> <dt>

1
</dt> <dd>

Сервер лицензирования удаленный рабочий стол не активирован.

</dd> <dt>

2
</dt> <dd>

Произошла неизвестная ошибка. Неизвестно, активирован ли сервер лицензий удаленный рабочий стол.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тслиценсесервер Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

