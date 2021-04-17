---
title: Метод EnvironmentVariables класса Win32_TSExpandEnvironmentVariables
description: Расширяет переменные среды, определенные системой. | Метод EnvironmentVariables класса Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода EnvironmentVariables
- Службы удаленных рабочих столов метода EnvironmentVariables, класс Win32_TSExpandEnvironmentVariables
- Класс Win32_TSExpandEnvironmentVariables службы удаленных рабочих столов, метод EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674591"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a>Метод EnvironmentVariables \_ класса Win32 тсекспанденвиронментвариаблес

Расширяет переменные среды, определенные системой.

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*OriginalString* \[ окне\]
</dt> <dd>

Строка, содержащая переменные среды для расширения.

</dd> <dt>

*Експандедстринг* \[ заполняет\]
</dt> <dd>

Строка с развернутыми переменными среды.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тсаллов. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсекспанденвиронментвариаблес Win32**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

