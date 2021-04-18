---
description: Метод RegistryValue объекта Installer считывает сведения об указанном разделе реестра value.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Метод Installer. RegistryValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651982"
---
# <a name="installerregistryvalue-method"></a>Метод Installer. RegistryValue

Метод **RegistryValue** объекта [**Installer**](installer-object.md) считывает сведения об указанном разделе реестра value. Если указанный раздел или значение не существует, метод возвращает ошибку 9, «индекс вне диапазона».

## <a name="syntax"></a>Синтаксис


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*root* 
</dt> <dd>

В Windows NT 4,0 корень реестра — это либо числовой корневой ключ, либо имя компьютера в виде строки. Имена компьютеров всегда являются строками. В Windows 95, Windows 98 или Windows Me корень реестра является только числовым корневым ключом. Доступ к разделу HKLM можно получить только на удаленном компьютере.



| Root                                                                                                                                                                                   | Значение      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <dt>**\_корневой узел классов hKey \_**</dt> </dl>             | 0<br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <dt>**HKEY \_ текущего \_ пользователя**</dt> </dl>             | 1<br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <dt>**HKEY \_ локальный \_ компьютер**</dt> </dl>          | 2<br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <dt>**\_Пользователи hKey**</dt> </dl>                                   | 3<br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <dt>**\_данные о производительности hKey \_**</dt> </dl> | 4<br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <dt>**\_Текущая \_ Конфигурация hKey**</dt> </dl>       | 5<br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <dt>**\_данные hKey Дин \_**</dt> </dl>                         | 6<br/> |



 

</dd> <dt>

*key* 
</dt> <dd>

Строка, содержащая полный путь к ключу из корня.

</dd> <dt>

*value* 
</dt> <dd>

Этот необязательный параметр определяет связанное значение, возвращаемое для указанного ключа. Значением является одно из значений, приведенных в следующей таблице.



| Значение                                                                                                                                                                                                    | Значение                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <dt>**Отсутствует или пусто**</dt> </dl> | Возвращает логическое значение, определяющее, существует ли ключ.<br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**Строка**</dt> </dl>                                         | Возвращает данные, связанные с именованным значением, завершается ошибкой, если имя значения не существует.<br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <dt>**Положительное целое число**</dt> </dl> | Возвращает имя перечислимого значения, основанного на 1, оно пустое, если оно не существует. Этот параметр использует функцию [**реженумвалуе**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) .<br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <dt>**Отрицательное целое число**</dt> </dl> | Возвращает имя подраздела с именем, основанное на 1, пустое, если оно не существует. Этот параметр использует функцию [**реженумкэй**](/windows/win32/api/winreg/nf-winreg-regenumkeya) .<br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <dt>**Нулевое целое число**</dt> </dl>                 | Возвращает имя класса String для назначенного ключа.<br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <dt>**Пустая строка ""**</dt> </dl> | Возвращает значение по умолчанию для раздела реестра.<br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 
