---
title: Метод Сетсессиондиректоряктиве класса Win32_TSSessionDirectory
description: Метод Сетсессиондиректоряктиве задает свойство Сессиондиректоряктиве.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсессиондиректоряктиве
- Службы удаленных рабочих столов метода Сетсессиондиректоряктиве, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Сетсессиондиректоряктиве
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ae44c471c653a3fcdfbab33ab70178b53c95715cce7cfba63defa9c96c1ab23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769354"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a>Метод Сетсессиондиректоряктиве \_ класса Win32 тссессиондиректори

Метод **сетсессиондиректоряктиве** задает свойство **сессиондиректоряктиве** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сессиондиректоряктиве* \[ окне\]
</dt> <dd>

Тип: **UInt32**

Флаг отключения или включения службы каталогов сеансов.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Отключите службу каталогов сеансов.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Включите службу каталогов сеансов.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

