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
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681967"
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

## <a name="remarks"></a>Комментарии

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
</dt> <dt>

[**жетложевентнаме**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

