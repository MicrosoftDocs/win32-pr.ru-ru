---
title: Метод Жетпротоколнаме класса Win32_TSGatewayServerSettings
description: Возвращает имя протокола для указанного индекса протокола.
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетпротоколнаме
- Службы удаленных рабочих столов метода Жетпротоколнаме, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Жетпротоколнаме
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81064581b209f047ac492faee6d442b082d038cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136334"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Жетпротоколнаме \_ класса Win32 тсгатевайсерверсеттингс

Возвращает имя протокола для указанного индекса протокола.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Протоколид* \[ окне\]
</dt> <dd>

Индекс идентификатора протокола. Значение должно быть в диапазоне от нуля до значения свойства **макспротоколс** .

</dd> <dt>

*ProtocolName* \[ заполняет\]
</dt> <dd>

Возвращает имя указанного протокола.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Поддерживается один протокол.

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

