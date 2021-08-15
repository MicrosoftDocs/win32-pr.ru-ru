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
ms.openlocfilehash: 49416291293d621739ab7c721ca349f5d87bb4582d1289f431a8c443d3414da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353896"
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

## <a name="remarks"></a>Remarks

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

