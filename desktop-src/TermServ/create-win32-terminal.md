---
title: Метод Create класса Win32_Terminal
description: Создает терминал с параметрами по умолчанию, которые можно настроить с помощью свойств и методов \_ классов Win32 терминалсеттинг.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Create
- Создание службы удаленных рабочих столов метода, Win32_Terminal класса
- Класс Win32_Terminal службы удаленных рабочих столов, метод Create
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489534"
---
# <a name="create-method-of-the-win32_terminal-class"></a>Метод Create \_ класса терминала Win32

Метод **CREATE** создает терминал с параметрами по умолчанию, которые можно настроить с помощью свойств и методов классов [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md) . Функция возвращает ноль в случае успеха и ошибку при сбое.

## <a name="syntax"></a>Синтаксис


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Невтерминалнаме* \[ окне\]
</dt> <dd>

Имя терминала.

</dd> <dt>

*Передача* \[ окне\]
</dt> <dd>

Транспорт для терминала. Это свойство класса [**Win32 \_ тсженералсеттинг**](win32-tsgeneralsetting.md) .

</dd> <dt>

*Терминалпротокол* \[ окне\]
</dt> <dd>

Протокол для терминала. Это свойство класса [**Win32 \_ тсженералсеттинг**](win32-tsgeneralsetting.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

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

[**\_Терминал Win32**](win32-terminal.md)
</dt> </dl>

 

