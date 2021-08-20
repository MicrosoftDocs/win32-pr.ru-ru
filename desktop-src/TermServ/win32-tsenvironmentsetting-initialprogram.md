---
title: Метод Инитиалпрограм класса Win32_TSEnvironmentSetting
description: Метод Инитиалпрограм задает свойства программы запуска, такие как имя, Рабочий каталог и путь программы, которые должны запускаться сразу после входа на сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Инитиалпрограм
- Службы удаленных рабочих столов метода Инитиалпрограм, класс Win32_TSEnvironmentSetting
- Класс Win32_TSEnvironmentSetting службы удаленных рабочих столов, метод Инитиалпрограм
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d13aaa0e4dfb4e0d16bea89bf871a7a890c0f375fd928e70fd99aed20c003be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127007"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>Метод Инитиалпрограм \_ класса Win32 тсенвиронментсеттинг

Метод **инитиалпрограм** задает свойства программы запуска, такие как имя, Рабочий каталог и путь программы, которые должны запускаться сразу после входа на сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Инитиалпрогрампас* \[ окне\]
</dt> <dd>

Имя и путь к программе запуска.

</dd> <dt>

*Запуск* \[ окне\]
</dt> <dd>

Путь к рабочему каталогу программы запуска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсенвиронментсеттинг Win32**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

