---
title: Метод Креатеселфсигнедцертификате класса Win32_TSGatewayServer
description: Создает самозаверяющий сертификат и возвращает хэш сертификата в виде \ 0034; out \ 0034; параметр.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Креатеселфсигнедцертификате
- Службы удаленных рабочих столов метода Креатеселфсигнедцертификате, класс Win32_TSGatewayServer
- Класс Win32_TSGatewayServer службы удаленных рабочих столов, метод Креатеселфсигнедцертификате
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200b08da8d5eea9f31405a357650384081c407df4eb76820cd47a111e6b66aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139057"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>Метод Креатеселфсигнедцертификате \_ класса Win32 тсгатевайсервер

Создает самозаверяющий сертификат и возвращает хэш сертификата как параметр "out". Кроме того, добавляет текст " \_ самозаверяющий сертификат шлюза TS \_ \_ \_ " в свойство контекста сертификата, чтобы сертификат был распознан как сертификат шлюза удаленный рабочий стол шлюза. Этот метод использует контейнер ключей для конкретного шлюза удаленных рабочих столов, чтобы создать сертификат.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SubjectName* \[ окне\]
</dt> <dd>

Имя субъекта самозаверяющего сертификата.

</dd> <dt>

*CertHash* \[ заполняет\]
</dt> <dd>

Хэш сертификата.

</dd> </dl>

## <a name="remarks"></a>Remarks

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_Тсгатевайсервер Win32**](win32-tsgatewayserver.md)
</dt> </dl>

 

