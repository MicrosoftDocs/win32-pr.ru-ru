---
title: Метод Сетколордепсполици класса Win32_TSClientSetting
description: Метод Сетколордепсполици задает свойство Колордепсполици для класса.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетколордепсполици
- Службы удаленных рабочих столов метода Сетколордепсполици, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетколордепсполици
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d47280ce303e7eeba401e0eb34c7f7fa5a7bec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415412"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a>Метод Сетколордепсполици \_ класса Win32 тсклиентсеттинг

Метод **сетколордепсполици** задает свойство **колордепсполици** для класса.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Колордепсполици* \[ окне\]
</dt> <dd>

Флаг отключения или включения свойства **сетколордепсполици** , которое указывает, следует ли переопределять максимальное значение цвета пользователя.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Включите свойство.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Отключите свойство.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает успешное завершение, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсклиентсеттинг Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

