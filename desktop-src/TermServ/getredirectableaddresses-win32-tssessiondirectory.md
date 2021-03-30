---
title: Метод Жетредиректаблеаддрессес класса Win32_TSSessionDirectory
description: Получает полный список доступных адресов DNS.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетредиректаблеаддрессес
- Службы удаленных рабочих столов метода Жетредиректаблеаддрессес, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Жетредиректаблеаддрессес
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071142"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Метод Жетредиректаблеаддрессес \_ класса Win32 тссессиондиректори

Получает полный список доступных адресов DNS.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фтокенредиректион* \[ окне\]
</dt> <dd>

Тип: **UInt32**

Флаг, указывающий, следует ли использовать перенаправление токенов.

</dd> <dt>

*Ipaddresses* \[ заполняет\]
</dt> <dd>

Тип: **строка \[ \]**

Полный список IP-адресов, доступных для перенаправления.

</dd> <dt>

*Адаптернамес* \[ заполняет\]
</dt> <dd>

Тип: **строка \[ \]**

Список имен сетевых адаптеров, связанных с адресами, доступными для перенаправления.

</dd> <dt>

*Нетконнаме* \[ заполняет\]
</dt> <dd>

Тип: **строка \[ \]**

Список имен сетевых подключений, связанных с адресами, доступными для перенаправления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тссессиондиректори Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

