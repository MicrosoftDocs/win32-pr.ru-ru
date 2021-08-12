---
title: Метод Исложевентенаблед класса Win32_TSGatewayServerSettings
description: Указывает, включен ли указанный тип журнала событий.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Исложевентенаблед
- Службы удаленных рабочих столов метода Исложевентенаблед, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Исложевентенаблед
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7130578287e313e03caf8b63c2e187f401608ad1cdbd575ae9e6bb6450e1adf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606063"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Исложевентенаблед \_ класса Win32 тсгатевайсерверсеттингс

Указывает, включен ли указанный тип журнала событий.

## <a name="syntax"></a>Синтаксис


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*EventName* \[ окне\]
</dt> <dd>

Имя типа журнала событий. Это значение должно быть получено с помощью метода [**жетложевентнаме**](getlogeventname-win32-tsgatewayserversettings.md) .

<dt>

логчаннелдисконнект
</dt> <dd>

Пользователь успешно отключился от ресурса.

</dd> <dt>

логфаиледчаннелконнект
</dt> <dd>

Пользователю не удалось подключиться к ресурсу.

</dd> <dt>

логфаилуренетворкакцессчекк
</dt> <dd>

Пользователь не прошел авторизацию подключения.

</dd> <dt>

логфаилурересаурцеакцессчекк
</dt> <dd>

Пользователь не прошел авторизацию ресурсов.

</dd> <dt>

логсукцессчаннелконнект
</dt> <dd>

Пользователь успешно подключился к ресурсу.

</dd> <dt>

логсукцессфулнетворкакцессчекк
</dt> <dd>

Пользователь успешно прошел авторизацию подключения.

</dd> <dt>

логсукцессфулресаурцеакцессчекк
</dt> <dd>

Пользователь успешно прошел авторизацию ресурсов.

</dd> </dl> </dd> <dt>

*Включено* \[ заполняет\]
</dt> <dd>

Указывает, включен ли указанный тип журнала событий.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

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

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**жетложевентнаме**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

