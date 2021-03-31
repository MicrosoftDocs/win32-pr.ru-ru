---
title: Метод Сетсекуритилайер класса Win32_TSGeneralSetting
description: Метод Сетсекуритилайер задает уровень безопасности.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсекуритилайер
- Службы удаленных рабочих столов метода Сетсекуритилайер, класс Win32_TSGeneralSetting
- Класс Win32_TSGeneralSetting службы удаленных рабочих столов, метод Сетсекуритилайер
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988754"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>Метод Сетсекуритилайер \_ класса Win32 тсженералсеттинг

Метод **сетсекуритилайер** задает уровень безопасности.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Секуритилайер* \[ окне\]
</dt> <dd>

Устанавливаемый уровень безопасности. Если текущий уровень шифрования равен 1, то недопустимо значение 2 для *секуритилайер* .

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Уровень безопасности RDP** (0)


</dt> <dd>

Связь между сервером и клиентом будет использовать собственное шифрование RDP.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Согласование** (1)


</dt> <dd>

Будет использоваться наиболее безопасный уровень, поддерживаемый клиентом. Если поддерживается, будет использоваться протокол SSL (TLS 1,0).

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (2)


</dt> <dd>

Протокол SSL (TLS 1,0) будет использоваться для проверки подлинности сервера, а также для шифрования всех данных, передаваемых между сервером и клиентом. Для этого параметра требуется, чтобы сервер имел сертификат, совместимый с SSL. Этот параметр несовместим со значением **миненкриптионлевел** , равное 1.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает успешное завершение, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

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

[**\_Тсженералсеттинг Win32**](win32-tsgeneralsetting.md)
</dt> <dt>

[**сетенкриптионлевел**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

