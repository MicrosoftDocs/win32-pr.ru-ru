---
title: Метод Енаблеонликонсенткапаблеклиентс класса Win32_TSGatewayServerSettings
description: Задает свойство Онликонсенткапаблеклиентс.
ms.assetid: abc91ea8-0f3c-4b7c-9091-3c8193e610da
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблеонликонсенткапаблеклиентс
- Службы удаленных рабочих столов метода Енаблеонликонсенткапаблеклиентс, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Енаблеонликонсенткапаблеклиентс
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableOnlyConsentCapableClients
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb671ccefe98cdc1b569bcde155071ef7cc0d9ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071350"
---
# <a name="enableonlyconsentcapableclients-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Енаблеонликонсенткапаблеклиентс \_ класса Win32 тсгатевайсерверсеттингс

Задает свойство **онликонсенткапаблеклиентс** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnableOnlyConsentCapableClients(
  [in] boolean OnlyConsentCapableClients
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Онликонсенткапаблеклиентс* \[ окне\]
</dt> <dd>

Тип: **Boolean**

Указывает новое значение для свойства **онликонсенткапаблеклиентс** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                        |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

